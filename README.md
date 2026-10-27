# Portfolio CV - Vũ Bá Việt Anh

Trang portfolio cá nhân giới thiệu Vũ Bá Việt Anh, Frontend Developer. Dự án trình bày thông tin giới thiệu, kỹ năng, các dự án tiêu biểu và kênh liên hệ trong một giao diện web responsive.

## Chức năng

- Điều hướng nhanh đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Hiển thị ảnh đại diện, thông tin cá nhân và lời giới thiệu.
- Trình bày danh sách kỹ năng và các dự án mẫu: Landing Page, Todo List, Weather Dashboard và Blog cá nhân.
- Bố cục tự điều chỉnh theo màn hình điện thoại, máy tính bảng và máy tính.
- Cung cấp liên kết GitHub và TikTok.

> Các thẻ dự án hiện là nội dung minh họa; liên kết “Xem chi tiết” chưa trỏ đến trang dự án thật.

## Công nghệ

- HTML5: cấu trúc nội dung và các vùng ngữ nghĩa.
- CSS3: giao diện, Flexbox, CSS Grid và thiết kế responsive theo hướng mobile-first.
- Không cần framework, Node.js, trình biên dịch hay cài đặt thư viện.

JavaScript, Git/GitHub và Figma cũng được liệt kê trong phần kỹ năng của portfolio, nhưng trang hiện tại không cần JavaScript để hoạt động.

## Yêu cầu môi trường

- Trình duyệt hiện đại như Chrome, Firefox, Edge hoặc Safari.
- Để mở trực tiếp: không cần cài thêm phần mềm.
- Để chạy máy chủ cục bộ: Python 3 (tùy chọn).
- Để chạy bằng container: Docker Engine hoặc Docker Desktop đang hoạt động (tùy chọn).

## Cài đặt

Tải hoặc sao chép mã nguồn về máy, sau đó mở thư mục dự án. Cấu trúc chính:

```text
.
├── index.html
├── assets/
│   ├── css/
│   │   └── styles.css
│   └── img/
│       └── avatar.jpg
└── README.md
```

Nếu dùng Git:

```bash
git clone <URL-repository>
cd <thu-muc-repository>
```

Thay `<URL-repository>` bằng địa chỉ repository thực tế. Nếu đã tải mã nguồn, chỉ cần mở thư mục chứa `index.html`.

## Cấu hình và tùy chỉnh

- **Thông tin cá nhân, nội dung, dự án và liên kết:** chỉnh sửa trong `index.html`.
- **Ảnh đại diện:** thay `assets/img/avatar.jpg` hoặc cập nhật đường dẫn ảnh trong `index.html`.
- **Màu sắc, phông chữ, khoảng cách và bố cục:** tùy chỉnh các biến CSS ở đầu `assets/css/styles.css` (khối `:root`) cùng các quy tắc giao diện bên dưới.
- **Thông tin email:** mục Email hiện đang trỏ đến trang hộp thư Google, không phải địa chỉ email liên hệ. Hãy thay `href` bằng `mailto:dia-chi-email@example.com` và thay phần chữ hiển thị bằng địa chỉ email thực trước khi công bố.
- Thay các liên kết `href="#"` của dự án bằng URL tương ứng khi đã có trang chi tiết.

Không có tệp `.env` hay cấu hình bí mật cần thiết cho trang này.

## Chạy thử

### Cách nhanh: mở trực tiếp

Mở `index.html` bằng trình duyệt. Cách này phù hợp để xem giao diện cơ bản mà không cài đặt thêm công cụ.

### Chạy qua máy chủ cục bộ (tùy chọn)

Từ thư mục dự án, chạy lệnh phù hợp với hệ điều hành:

**Windows (PowerShell):**

```powershell
py -m http.server 8000
```

Nếu lệnh `py` không có sẵn, thử:

```powershell
python -m http.server 8000
```

**macOS:**

```bash
python3 -m http.server 8000
```

**Linux:**

```bash
python3 -m http.server 8000
```

Mở [http://localhost:8000](http://localhost:8000) trong trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

## Chạy bằng Docker (tùy chọn)

Không cần tạo Dockerfile: có thể phục vụ các tệp tĩnh bằng image Nginx chính thức, mount thư mục dự án ở chế độ chỉ đọc và ánh xạ cổng 8080 của máy vào cổng 80 của container. Chạy lệnh từ thư mục dự án.

**Windows (PowerShell):**

```powershell
docker run --name cv-portfolio --rm -d -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

**macOS hoặc Linux:**

```bash
docker run --name cv-portfolio --rm -d -p 8080:80 -v "$PWD:/usr/share/nginx/html:ro" nginx:alpine
```

Mở [http://localhost:8080](http://localhost:8080) để xem trang. Dừng container bằng:

```bash
docker stop cv-portfolio
```

Tùy chọn `--rm` tự xóa container sau khi dừng; image Nginx đã tải vẫn có thể được Docker tái sử dụng.

## Thông tin liên hệ

- **GitHub:** [vuvietanh2362008](https://github.com/vuvietanh2362008)
- **TikTok:** [@viah23.28](https://www.tiktok.com/@viah23.28)
- **Email:** chưa có địa chỉ email hợp lệ được cung cấp trong trang. Xem mục [Cấu hình và tùy chỉnh](#cấu-hình-và-tùy-chỉnh) để cập nhật.