# 4. Yêu cầu đầu ra
1. Phần I. Phân tích
- Input: Tên miền phong-dieu-phoi.grenlog.vn
- Output: Địa chỉ tìm kiếm lỗi tên miền (không tồn tại)
> Mô tả sơ đồ luồng dữ liệu DNS
- Browser Cache(Kiểm tra tên miền) -> Host file(Hệ điều hành sẽ kiểm tra xem tên miền có tồn tại hay không) -> DNS(Sẽ tra cứu trên hệ thống và gửi lại phản hồi) -> Root name Server(Tên gốc rễ của máy chủ) -> TLD name server(Máy chủ truy soát tìm thấy gốc rễ nên sẽ chuyển đổi định dạng URL để tiến tới trang web gốc) -> Authorize Name Server(Máy chủ phân giải và trả về kết quả trang web)
2. Phần II. Triển khai
- Cách sử dụng trình duyệt DevTools: Inspect(F12) -> chuyển sang Network -> Gõ lại địa chỉ chính xác và tải lại trang -> Kiểm tra cột Status nếu có những mã 404, 505 thì đã phân giải và đi tới trang web thành công
3. Phần III. Kiểm thử
- Giả sử Nam sửa đổi lại đúng tên miền mà vẫn bị lỗi 404 Not Found, có thể là do máy chủ bị lỗi sự cố hệ thống hoặc đường dẫn đó không còn tồn tại nữa.