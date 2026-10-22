# Báo cáo kiểm tra SEO: buivanvu.com (hướng LMS Next.js)

Ngày kiểm tra: 22/10/2026. Phạm vi: toàn site (trang chủ, 3 bài blog, trang danh mục, tag, sitemap, robots.txt, llms.txt).

**Giới hạn dữ liệu:** các công cụ SEO (Ahrefs, Similarweb, Supermetrics) không kết nối được trong phiên này, và tìm kiếm web không trả về số liệu lượng tìm kiếm tiếng Việt. Vì vậy cột "độ khó" và "nhu cầu" trong bảng từ khóa là **ước lượng định tính**, cần kiểm chứng bằng Google Search Console, Google Keyword Planner hoặc Ahrefs trước khi đầu tư lớn. Số đo tốc độ lấy từ môi trường máy chủ đám mây qua proxy, chỉ để tham khảo.

## Tóm tắt

Nền tảng kỹ thuật SEO của site tốt hơn mức thường thấy ở freelancer: HTTPS, sitemap, robots.txt, `llms.txt`, schema đầy đủ (FAQPage, BlogPosting, BreadcrumbList), thẻ OG, www chuyển về non-www đúng. Điểm mạnh lớn nhất là nội dung blog đã viết đúng giọng "giải thích rõ, không nói quá".

Ba ưu tiên lớn nhất:
1. **Site chưa nhắc LMS và Next.js ở bất kỳ đâu**, nên không thể xếp hạng cho từ khóa LMS dù đó là hướng bạn muốn bán.
2. **Chưa có trang dịch vụ riêng**, cả ba dịch vụ nằm chung trang chủ, và trang chủ có H1 là "Webapp & Automation" (không chứa từ khóa người dùng gõ).
3. **Chưa thấy theo dõi đo lường** (không phát hiện GA4 hoặc Search Console qua mã nguồn trang), nên chưa biết site đang có bao nhiêu traffic.

Đánh giá chung: **nền tảng tốt, thiếu nội dung và trang đích cho hướng LMS**.

## Bảng từ khóa cơ hội (ước lượng)

Ý định: I = thông tin, C = so sánh/thương mại, T = giao dịch. Độ khó và cơ hội là ước lượng định tính.

| # | Từ khóa | Độ khó (ước lượng) | Cơ hội | Xếp hạng hiện tại | Ý định | Loại nội dung |
|---|---------|--------------------|--------|-------------------|--------|---------------|
| 1 | thiết kế website LMS | Vừa | Cao | Chưa có | T | Trang dịch vụ `/lms-nextjs` |
| 2 | xây dựng hệ thống LMS | Vừa | Cao | Chưa có | T | Trang dịch vụ (cùng trang trên) |
| 3 | làm website bán khóa học online | Vừa | Cao | Chưa có | T | Landing page |
| 4 | phần mềm quản lý trung tâm đào tạo | Khó (nhiều SaaS) | Trung bình | Chưa có | C | Bài so sánh tự xây và mua |
| 5 | chi phí làm hệ thống LMS | Dễ-vừa | Cao | Chưa có | C | Bài hướng dẫn giá (khoảng giá, các khoản) |
| 6 | LMS là gì | Khó (từ chung) | Trung bình | Chưa có | I | Bài trụ cột (pillar) |
| 7 | LMS tự xây hay dùng Moodle | Dễ | Cao | Chưa có | C | Bài so sánh |
| 8 | Moodle hay LMS Next.js | Dễ | Cao | Chưa có | C | Bài so sánh |
| 9 | website bán khóa học thay Teachable/Udemy | Dễ | Trung bình | Chưa có | C | Bài so sánh |
| 10 | LMS cho trung tâm tiếng Anh | Dễ-vừa | Cao | Chưa có | T | Trang theo ngành |
| 11 | LMS cho doanh nghiệp đào tạo nội bộ | Vừa | Trung bình | Chưa có | T | Trang theo ngành |
| 12 | thi trắc nghiệm online cho trung tâm | Dễ | Trung bình | Chưa có | C | Bài hướng dẫn |
| 13 | cấp chứng chỉ khóa học tự động | Dễ | Trung bình | Chưa có | I | Bài hướng dẫn |
| 14 | tích hợp thanh toán vào website khóa học (VNPay, MoMo, PayOS) | Dễ | Cao | Chưa có | I | Bài kỹ thuật |
| 15 | chatbot AI hỗ trợ học viên | Dễ | Cao | Chưa có | C | Bài/Trang tính năng |
| 16 | tự động hóa quy trình trung tâm đào tạo | Dễ | Trung bình | Chưa có | I | Bài hướng dẫn |
| 17 | thuê lập trình viên freelance làm website | Khó | Thấp | Chưa có | T | Không ưu tiên |
| 18 | ERP là gì doanh nghiệp nhỏ | Khó | Thấp-trung bình | Có bài, chưa đo | I | Giữ, cập nhật |
| 19 | dịch vụ thiết kế website trọn gói | Rất khó (nhiều đối thủ) | Thấp | Có bài, chưa đo | C | Giữ, không đầu tư thêm |
| 20 | Next.js LMS | Dễ (thị trường quốc tế) | Thấp tại VN | Chưa có | I | Chỉ dùng như chủ đề phụ |

Lưu ý chiến lược: nhóm từ chung như "LMS là gì" có nhiều đơn vị lớn cạnh tranh. Nên ưu tiên cụm dài, theo ngành và so sánh (hàng 5, 7, 8, 10, 14), vì dễ lên hạng và khách đã gần quyết định mua.

## Lỗi on-page

| Trang | Vấn đề | Mức độ | Cách sửa |
|-------|--------|--------|----------|
| Trang chủ | H1 là "Webapp & Automation", không chứa từ khóa dịch vụ bằng tiếng Việt, không nhắc LMS | Cao | Đổi H1 hoặc thêm dòng phụ đầu trang: "Website bán khóa học và hệ thống LMS cho trung tâm đào tạo" |
| Toàn site | Không có trang nào nhắm LMS, Next.js, hay chatbot AI | Nghiêm trọng | Tạo trang dịch vụ riêng (xem kế hoạch) |
| `/tag/*` | Slug tag bị mất ký tự tiếng Việt (`chuyn-i-s`, `oanh-nghip-nh`, `ebsite-doanh-nghip`, `thit-k-website`, `o-gi-website`), trang tag vẫn `index, follow` và nằm trong sitemap | Cao | Sửa hàm tạo slug (giữ hoặc chuyển dấu thành ASCII đúng: `chuyen-doi-so`), chuyển hướng 301 slug cũ, và đặt `noindex` cho trang tag nếu mỗi tag chỉ có 1-2 bài |
| `/category/blog` | Không có meta description | Trung bình | Viết mô tả riêng 150-160 ký tự |
| Bài blog | Đã có khối CTA ở cột bên (link `/#lien-he`) nhưng chưa có kênh liên hệ trực tiếp (Zalo); cột bên nằm cuối trang trên điện thoại. Đính chính: bản đầu của báo cáo ghi nhầm là chưa có CTA | Trung bình | Thêm nút Zalo vào khối CTA (đã làm trong repo web), và chèn liên kết tới trang dịch vụ trong thân bài |
| Trang chủ | 1 ảnh có `alt=""` | Thấp | Thêm alt mô tả (hoặc để rỗng nếu là ảnh trang trí, có chủ đích) |
| Blog | Mới 3 bài, chưa có bài nào về LMS, chatbot, hay trung tâm đào tạo | Cao | Xem phần khoảng trống nội dung |
| Trang chủ | Title 45 ký tự, mô tả 123 ký tự (dưới mức tối ưu 150-160) | Thấp | Kéo dài mô tả, thêm cụm "LMS" và "khóa học online" |

## Khoảng trống nội dung

| Chủ đề | Vì sao quan trọng | Định dạng | Ưu tiên | Công sức |
|--------|-------------------|-----------|---------|----------|
| Trang dịch vụ LMS Next.js | Trang đích chính cho khách mua | Landing page | Cao | Đáng kể (nhiều ngày) |
| Chi phí làm hệ thống LMS | Khách hỏi giá trước khi liên hệ, ít đối thủ viết thẳng | Bài hướng dẫn | Cao | Vừa (nửa ngày) |
| LMS tự xây hay dùng Moodle/SaaS | Giai đoạn so sánh, khớp phong cách "tư vấn trung thực" của bạn | Bài so sánh | Cao | Vừa |
| Case study LMS | Bằng chứng đang thiếu (bạn đã có dự án) | Trang case study | Cao | Vừa |
| Tích hợp thanh toán VNPay/MoMo/PayOS cho website khóa học | Từ khóa dài, ít cạnh tranh, thể hiện chuyên môn | Bài kỹ thuật | Trung bình | Vừa |
| Chatbot AI hỗ trợ học viên | Điểm khác biệt so với LMS đóng gói | Trang tính năng + bài | Trung bình | Vừa |
| LMS cho trung tâm tiếng Anh/kỹ năng/nội bộ doanh nghiệp | Tách theo ngành để khớp ý định tìm kiếm | Trang theo ngành | Trung bình | Vừa |
| Bài trụ cột "LMS là gì" | Gom các bài con, tăng liên kết nội bộ | Pillar (khoảng 2.500 từ) | Trung bình | Đáng kể |
| Cập nhật bài ERP/Tự động hóa/Website trọn gói | Thêm liên kết sang dịch vụ và CTA | Chỉnh sửa | Thấp | Nhanh (1-2 giờ) |

## Danh sách kiểm tra kỹ thuật

| Kiểm tra | Trạng thái | Chi tiết |
|----------|-----------|----------|
| HTTPS, HSTS | Đạt | Có `strict-transport-security` |
| www chuyển về non-www | Đạt | `www.buivanvu.com` trả về 200 tại `https://buivanvu.com/` |
| robots.txt | Đạt | Chặn `/admin/`, `/api/`, `/_next/`, `/setup/`; có khai báo sitemap |
| Sitemap | Cảnh báo | Có 15 URL, nhưng gồm các tag lỗi slug và `lastmod` chỉ dùng được nếu cập nhật thật |
| llms.txt | Đạt | Có và đúng chuẩn, nhưng chỉ liệt kê trang chính, chưa liệt kê bài blog |
| Canonical | Đạt | Trang chủ có canonical đúng |
| Meta robots | Đạt | `index, follow` |
| Viewport/mobile | Đạt | Có `viewport` |
| Schema | Đạt | WebSite, Organization, FAQPage, BlogPosting, Person, BreadcrumbList |
| Thẻ OG | Đạt | Có ảnh OG và `og:image:alt` |
| Tốc độ phản hồi (TTFB) | Cảnh báo | Khoảng 2,0 giây đo từ máy chủ đám mây qua proxy; cần đo lại bằng PageSpeed Insights vì phép đo này có thể cao hơn thực tế |
| Số lượng script/font | Cảnh báo | Khoảng 43 thẻ script và khoảng 20 file font preload trên trang chủ; nên rà để chỉ tải các font thực sự dùng |
| Cache | Cảnh báo | `cache-control: no-store` trên trang HTML, nên cân nhắc cache cho trang tĩnh/blog (ISR) để giảm TTFB |
| Phân tích truy cập | Cảnh báo | Không phát hiện GA4/GTM/Plausible trong mã nguồn trang; cần xác nhận |
| Search Console | Chưa rõ | Không kiểm tra được từ bên ngoài |
| Liên kết hỏng | Không đo đầy đủ | Chỉ có 15 URL, các liên kết được thử đều trả 200 |
| Trang 404 | Đạt | URL không tồn tại trả về 404 đúng mã |

## So sánh đối thủ (định tính)

Tìm kiếm cho thấy khách tìm LMS sẽ gặp ba nhóm: SaaS trong nước (Bizfly LMS, VNPT LMS, Lạc Việt), nền tảng mã nguồn mở (Moodle, LearnPress) và freelancer quốc tế (Fiverr, Upwork). Chưa có đối thủ nào được xác nhận bằng dữ liệu xếp hạng.

| Khía cạnh | buivanvu.com | SaaS trong nước | Moodle/WordPress | Freelancer quốc tế |
|-----------|--------------|-----------------|-------------------|--------------------|
| Tùy biến theo quy trình riêng | Mạnh (tự code) | Hạn chế | Trung bình (plugin) | Trung bình |
| Giá | Theo phạm vi, minh bạch | Thuê bao hằng tháng | Phần mềm miễn phí, tốn công cấu hình | Rẻ, ít hỗ trợ tiếng Việt |
| Hỗ trợ tiếng Việt, thanh toán nội địa | Mạnh | Mạnh | Cần cấu hình | Yếu |
| Bằng chứng (case study, đánh giá) | **Yếu (chưa hiển thị)** | Mạnh | Mạnh (cộng đồng) | Mạnh (đánh giá) |
| Độ phủ nội dung SEO về LMS | **Chưa có** | Mạnh | Mạnh | Yếu về tiếng Việt |

Khoảng trống có thể khai thác: khách cần LMS **tùy biến**, **thanh toán nội địa**, **bàn giao mã nguồn** và **một người chịu trách nhiệm**. SaaS không đáp ứng tốt, Moodle thì nặng và khó tùy biến giao diện.

## Kế hoạch hành động

### Làm trong tuần này (nhanh)
1. Kết nối Google Search Console và GA4, gửi sitemap. Tác động cao, công sức 1-2 giờ.
2. Sửa slug tag lỗi, chuyển hướng 301, đặt `noindex` cho tag mỏng. Tác động trung bình, công sức nửa ngày.
3. Thêm CTA Zalo và liên kết dịch vụ vào cuối 3 bài blog hiện có. Tác động cao, công sức 1-2 giờ.
4. Thêm meta description cho `/category/blog`, kéo dài mô tả trang chủ. Tác động thấp, công sức 30 phút.
5. Cập nhật `llms.txt` để liệt kê các bài blog. Tác động thấp, công sức 30 phút.

### Đầu tư chiến lược (quý này)
1. Dựng trang `/lms-nextjs` (và trang theo ngành) với demo công khai, case study, bảng khoảng giá. Tác động cao, công sức nhiều ngày. Phụ thuộc: có demo và 1-2 case study.
2. Viết 6-8 bài theo cụm LMS (xem bảng khoảng trống). Tác động cao, công sức 2-3 tháng, mỗi tuần một bài.
3. Tối ưu hiệu năng (cache trang blog, giảm font/script). Tác động trung bình, công sức vài ngày. Đo lại bằng PageSpeed Insights trước và sau.
4. Xây liên kết từ các nguồn thật: giới thiệu trên cộng đồng dev/giáo dục, bài khách, hồ sơ doanh nghiệp. Tác động trung bình, công sức liên tục.
