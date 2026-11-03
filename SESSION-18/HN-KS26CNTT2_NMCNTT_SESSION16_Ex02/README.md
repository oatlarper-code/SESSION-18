# 4. Yêu cầu đầu ra
1. Phần I. Phân tích

||Cache MB/GB|Cookies|
|-|-|-|
Dung lượng|Lớn|Nhỏ
Lưu trữ|Các tài nguyên tĩnh để tải trang nhanh hơn mà không cần phải tải lại cả server|Các thông tin định danh và dữ liệu thông tin người dùng|
Độ bảo mật|Dễ bị xung đột giữa dữ liệu cũ|Dễ bị xâm nhập và đánh cắp thông tin cá nhân

2. Phần II. Triển khai
- Cấu trúc mẩu tin của Cookies:
  - `Set-cookie: shipper_auth_token=abc123`(Giá trị token định danh duy nhất shipper khi đăng nhập)
  - `Max-Age=12000`(Thiết lập thời gian tồn tại của cookie là 86400s) tương đương 24h nhờ đó shipper khi tắt trình duyệt sẽ vẫn có đăng nhập lại và sử dụng tiếp mà không bị mất đi dữ liệu
  - `HttpOnly`(Ngăn chặn hoàn toàn các đoạn mã JavaScript từ phía khách hàng dữ liệu định danh được giữ an toàn tuyệt đối)
  - `Secure`(Đảm bảo cookie chỉ được truyền tải qua giao thức mã HTTPS, ngăn chặn bị bắt gói tin)
  - `SameSite=Strict`(Chống tấn công giả mạo yêu cầu liên trang bằng cách chỉ gửi cookie khi người dùng thực hiện thao tác trực tiếp trên trang quản trị)
3. Phần III. Kiểm thử
- Các thao tác Hard Reload để xóa Cache đệm:
  - Nhấn tổ hợp phím Ctrl + F5 (Hoặc mở công cụ Inspect để xóa thủ công nhấn chuột phải vào phần tải lại trang ở góc bên trái và chọn "Empty Cache and Hard Reload)