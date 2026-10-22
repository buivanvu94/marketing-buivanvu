# Phân tích: trang công khai trả về `no-store` và phản hồi chậm

Ngày: 22/10/2026. Phạm vi: `buivanvu-web` (`src/app/(site)/layout.tsx`). Trạng thái: **chỉ phân tích, chưa sửa code**.

## Hiện trạng đo được

- Mọi trang HTML công khai trả `cache-control: private, no-cache, no-store, max-age=0, must-revalidate`.
- TTFB trang chủ khoảng 2,0 giây, đo từ máy chủ đám mây qua proxy (cần đo lại bằng PageSpeed Insights từ máy bạn để có số đáng tin).
- Mỗi phản hồi còn đặt cookie `__Host-authjs.csrf-token` và `__Secure-authjs.callback-url` cho cả khách chưa đăng nhập.

## Nguyên nhân (đã xác nhận bằng đọc code)

`SiteLayout` ở `src/app/(site)/layout.tsx` chạy cho mọi trang công khai và:

1. gọi `auth()` (đọc cookie phiên) cùng lúc với đọc cài đặt và menu;
2. gọi `(await headers()).get('x-current-path')` để quyết định ẩn header/footer theo từng trang;
3. dùng kết quả phiên cho: chuyển hướng chế độ bảo trì (`redirect('/maintenance')` với người không phải admin), thanh admin, truy vấn SQL `show_admin_bar`, quyền sửa menu (`canEditMenu`), và ngữ cảnh khu `header:actions` (biểu tượng người dùng, modal đăng nhập, liên kết tài khoản).

Đọc cookie hoặc header khiến Next.js render động cho toàn cây, nên không thể cache HTML dùng chung. Đây là hệ quả của thiết kế, không phải cấu hình sai.

## Vì sao tôi chưa sửa

Cách sửa đúng là tách mọi thứ phụ thuộc phiên khỏi layout để trang cho khách dùng được cache, và đẩy phần theo người dùng sang client hoặc phần dịch ra riêng. Việc này đụng tới đăng nhập, bảo trì, thanh admin và modal đăng nhập. Môi trường hiện tại không có database hay Redis để chạy và kiểm chứng, nên một thay đổi tại đây có thể làm hỏng đăng nhập hoặc chế độ bảo trì của site thật mà không phát hiện được. Merge vào `main` lại tự deploy.

## Phương án (từ an toàn đến sâu)

| # | Phương án | Rủi ro | Công sức | Hiệu quả |
|---|-----------|--------|----------|----------|
| A | **Cache ngắn ở nginx cho khách chưa đăng nhập** (bỏ qua khi có cookie phiên). Không đổi code | Thấp, nếu cấu hình bỏ qua đúng cookie | Vài giờ | Cao cho trang blog, trang chủ |
| B | Chuyển phần theo người dùng (thanh admin, biểu tượng tài khoản, modal đăng nhập) sang client component lấy phiên qua `/api/auth/session`; chuyển chế độ bảo trì sang middleware; thay `x-current-path` bằng cách khác | Trung bình đến cao (đụng auth) | 2–4 ngày + kiểm thử | Cao, bền vững, cho phép ISR |
| C | Giữ nguyên layout, chỉ tối ưu truy vấn (gộp truy vấn menu/cài đặt, thêm cache Redis) | Thấp | Nửa ngày | Vừa; vẫn `no-store` |

Khuyến nghị: làm **A** trước để có kết quả sớm, rồi **B** khi có môi trường staging có database.

### Gợi ý cấu hình cho phương án A (cần thử trên staging trước)

Ý tưởng, chưa kiểm chứng trên VPS của bạn:

- Chỉ cache `GET`/`HEAD` các đường dẫn công khai; không cache `/api/`, `/admin/`, `/mcp`, `/account`, `/dang-nhap`, `/dang-ky`, `/maintenance`.
- Bỏ qua cache nếu có cookie phiên Auth.js (tên có chứa `authjs.session-token`), để quản trị viên không bao giờ thấy trang của khách và ngược lại.
- Cache 60–300 giây; xóa khi deploy.
- Phải loại `Set-Cookie` (cookie csrf) khỏi phản hồi được lưu, và bỏ qua `Cache-Control: no-store` của Next bằng `proxy_ignore_headers`. Nếu bỏ sót, cookie của một khách có thể bị phát cho người khác.
- Chế độ bảo trì: khi bật phải xóa cache, nếu không khách vẫn thấy trang cũ trong vài phút.

Lưu ý: tôi chưa thấy cấu hình nginx của VPS trong repo (chỉ có `scripts/deploy-remote.sh` và workflow rsync), nên cần bạn cung cấp hoặc tự áp dụng.

## Việc cần bạn quyết

1. Bạn muốn làm phương án A (nginx) trước hay đi thẳng B?
2. Bạn có môi trường staging (cùng cấu hình nhưng database riêng) để thử không?
