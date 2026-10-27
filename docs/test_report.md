# Báo cáo kiểm thử

## Thông tin chung

- **Dự án:** Portfolio CV - Vũ Bá Việt Anh
- **Ngày kiểm thử:** 27/10/2026
- **Phạm vi:** Kiểm tra trang HTML/CSS tĩnh trong trình duyệt, điều hướng nội trang, tài nguyên hình ảnh, bố cục responsive và rà soát mã nguồn ở mức thủ công.
- **Cách chạy:** Mở `index.html` trực tiếp trong trình duyệt.
- **Lưu ý:** Đây là kiểm thử thủ công, không thay thế kiểm thử tự động, rà soát bảo mật chuyên sâu hay kiểm thử trên nhiều trình duyệt/thiết bị thật.

## Tổng hợp kết quả

| Tiêu chí | Kết quả | Tóm tắt |
|---|---|---|
| Tính đúng đắn | Đạt một phần | Trang và các mục chính hiển thị; ảnh tải được và liên kết điều hướng nội trang hoạt động. Liên kết dự án và email còn hạn chế. |
| UI/UX | Đạt một phần | Bố cục thích ứng ở 390px; ở viewport cực hẹp 170px phát hiện tràn ngang. |
| Khả năng vận hành - xử lý lỗi | Đạt một phần | Trang tĩnh mở được trong trình duyệt; chưa có xử lý lỗi cho backend/API vì các chức năng này chưa được triển khai. |
| Bảo mật | Rà soát cơ bản | Không thấy luồng đăng nhập, xử lý dữ liệu người dùng hoặc bí mật phía client; chưa thực hiện quét/pentest. |
| Chất lượng mã nguồn | Đạt một phần | HTML và CSS được tách riêng, có cấu trúc ngữ nghĩa và breakpoint; chưa có lint, bộ test hay kiểm tra tự động. |
| Khả năng triển khai | Đạt một phần | Có thể phục vụ dưới dạng website tĩnh; chưa xác minh triển khai bằng Docker hoặc trên hosting. |

## 1. Tính đúng đắn

- **Kiểm tra:** Mở trang, kiểm tra tiêu đề và các khu vực Giới thiệu, Kỹ năng, Dự án, Liên hệ; kiểm tra ảnh; bấm điều hướng đến mục Kỹ năng.
- **Kết quả:** Đạt với nội dung và điều hướng cơ bản. Trình duyệt nhận diện đủ bốn khu vực; cả 5 ảnh đều tải thành công; liên kết điều hướng cập nhật đích `#skills`.
- **Hạn chế:** Có 4 liên kết “Xem chi tiết” đang dùng `href="#"`. Liên kết Email đang dùng URL hộp thư trong `mailto:` thay vì địa chỉ email thực. Các thẻ Todo List và Weather Dashboard chỉ là nội dung giới thiệu tĩnh, không phải ứng dụng có thể tương tác.
- **Minh chứng:** [Ảnh giao diện](screenshots/01-trang-web.png).

## 2. UI/UX

- **Kiểm tra:** Quan sát giao diện, điều hướng, ảnh đại diện, thẻ dự án và bố cục ở trình duyệt, viewport 390px và viewport cực hẹp 170px.
- **Kết quả:** Ở 390px, hero xếp dọc, danh sách dự án hiển thị một cột và không có tràn ngang. Ở 170px, nội dung rộng hơn viewport và xuất hiện tràn ngang; đây là độ rộng cực hẹp, thấp hơn kích thước điện thoại phổ biến. Bố cục và các liên kết chính vẫn hiển thị.
- **Minh chứng:** [Ảnh giao diện](screenshots/01-trang-web.png), [ảnh thử viewport 170px](screenshots/02-viewport-170px.png).

## 3. Khả năng vận hành - xử lý lỗi

- **Kiểm tra:** Mở trực tiếp `index.html` và quan sát việc hiển thị các thành phần, ảnh tĩnh.
- **Kết quả:** Trang tải và hiển thị trong trình duyệt; không cần backend hoặc bước biên dịch để xem portfolio.
- **Chưa kiểm tra:** Không có luồng gửi biểu mẫu, API thực tế hoặc dịch vụ backend để thử lỗi mạng, lỗi máy chủ hay dữ liệu không hợp lệ. Chưa xác minh cách chạy qua máy chủ HTTP.
- **Minh chứng:** [Ảnh giao diện](screenshots/01-trang-web.png).

## 4. Bảo mật

- **Kiểm tra:** Rà soát thủ công cấu trúc HTML/CSS và các chức năng đang hiện diện.
- **Kết quả:** Dự án hiện là trang tĩnh; trong phạm vi rà soát không thấy form thu thập dữ liệu, xác thực người dùng, lưu thông tin bí mật phía client hoặc mã JavaScript xử lý dữ liệu.
- **Lưu ý:** Đây không phải kết quả kiểm thử xâm nhập hay quét lỗ hổng. Các liên kết ngoài cần được kiểm tra khi cập nhật; liên kết Email hiện chưa hợp lệ và nên sửa trước khi công bố.
- **Minh chứng:** [Ảnh giao diện và khu vực liên hệ](screenshots/01-trang-web.png).

## 5. Chất lượng mã nguồn

- **Kiểm tra:** Rà soát thủ công `index.html` và `assets/css/styles.css`; xác nhận trình duyệt tải được trang cùng các tài nguyên.
- **Kết quả:** Cấu trúc nội dung dùng các phần HTML riêng biệt; CSS được tách thành tệp riêng, có biến màu/khoảng cách, Flexbox, Grid và media query cho tablet/desktop. Văn bản thay thế ảnh được khai báo.
- **Hạn chế:** Chưa có test tự động, formatter, linter hoặc bộ kiểm tra accessibility được chạy; chưa xác minh HTML bằng validator độc lập.
- **Minh chứng:** [Ảnh giao diện](screenshots/01-trang-web.png), [ảnh bố cục hẹp](screenshots/02-viewport-170px.png).

## 6. Khả năng triển khai

- **Kiểm tra:** Mở website từ tệp HTML cục bộ; đối chiếu cách chạy máy chủ tĩnh và Docker được mô tả trong README.
- **Kết quả:** Có thể triển khai như website tĩnh vì trang chỉ cần HTML, CSS và hình ảnh; mở trực tiếp trong trình duyệt đã được xác nhận.
- **Chưa kiểm tra:** Chưa chạy máy chủ HTTP, chưa build/chạy container Docker và chưa triển khai lên hosting. Vì vậy, các hướng dẫn triển khai này chưa được xác nhận thực tế trong lần kiểm thử.
- **Minh chứng:** [Ảnh trang chạy cục bộ](screenshots/01-trang-web.png).

## Khuyến nghị

1. Thay liên kết Email bằng địa chỉ liên hệ hợp lệ và sửa `mailto:`.
2. Thay các liên kết `href="#"` bằng URL dự án thật hoặc bỏ liên kết nếu chưa có trang chi tiết.
3. Kiểm tra và cải thiện tràn ngang ở viewport cực hẹp; kiểm tra thêm trên thiết bị và trình duyệt thực tế.
4. Bổ sung kiểm tra tự động HTML/CSS và accessibility nếu dự án tiếp tục phát triển.
5. Thực hiện kiểm thử máy chủ/Docker và xác nhận website sau khi triển khai trước khi phát hành.