# Khầy Chùa Photo AI — PWA prototype

Bản web app thử nghiệm, ưu tiên dùng trên iPhone Safari. Không cần tài khoản Apple Developer và không cần IPA.

## Chạy thử
- Có thể mở `index.html` trên máy tính để xem giao diện, nhưng một số tính năng PWA/offline chỉ hoạt động khi chạy qua HTTPS hoặc localhost.
- Để cài lên iPhone: đưa toàn bộ thư mục này lên một dịch vụ hosting HTTPS (ví dụ GitHub Pages hoặc Netlify), mở địa chỉ HTTPS bằng Safari trên iPhone → nút Chia sẻ → **Thêm vào Màn hình chính**.
- Khi được host bằng HTTPS, Service Worker lưu bộ khung ứng dụng để mở lại khi offline.

## Có trong bản này
- Giao diện tối ưu cho màn hình iPhone.
- Chọn nhiều ảnh từ thư viện.
- Chọn từng ảnh để xem trước.
- Thay nền bằng màu hoặc một ảnh nền.
- Điều chỉnh độ sáng, bóng đổ và viền khung đơn giản.
- Xuất PNG từng ảnh hoặc lần lượt nhiều ảnh.
- Manifest và service worker cơ bản.

## Giới hạn cần biết
Đây là prototype xử lý ảnh cơ bản trên trình duyệt. Chưa có AI tách nền, tạo nền sinh ảnh, xóa vật thể, chọn/chỉnh sửa vùng chủ thể, đồng bộ dự án hoặc xử lý batch nâng cao. Thanh bóng và viền hiện là hiệu ứng đơn giản trên toàn ảnh, không phải bóng/viền thông minh quanh chủ thể. Xuất nhiều ảnh sẽ kích hoạt lượt tải xuống riêng cho từng ảnh; Safari có thể hỏi xác nhận.

## Cấu trúc
- `index.html`: giao diện
- `style.css`: kiểu dáng responsive
- `app.js`: chọn ảnh, canvas, hiệu ứng và xuất PNG
- `manifest.webmanifest`: cấu hình cài như PWA
- `sw.js`: cache tài nguyên cơ bản
- `icon.svg`: biểu tượng ứng dụng

## Ghi chú phát triển
Muốn thêm AI tách nền/xóa vật thể chất lượng cao, cần tích hợp mô hình chạy trên thiết bị hoặc dịch vụ xử lý ảnh có máy chủ/API. Không đặt API key bí mật trực tiếp trong JavaScript phía trình duyệt.
