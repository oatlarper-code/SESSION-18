# 4. Yêu cầu đầu ra
1. Phần I. Phân tích 

||Incognito Mode|Dedicated Profile
|-|-|-|
Bản chất|Lưu trữ tạm thời, toàn bộ dữ liệu trong cookies sẽ bị xóa sạch khi đóng trình duyệt|Lưu trữ lâu dài trên ổ cứng cục bộ và được đồng bộ cùng với máy tính|
Xử lý|tra cứu thông tin nhanh, kiểm tra giao diện ở chế độ khách, tránh lưu lịch sử tìm kiếm ngắn hạn|Quản lý đồng thời nhiều tài khoản cố định mà không lo bị văng

2. Phần II. Triển khai
- Mô tả quy trình tạo và đồng bộ hóa để bảo vệ BookMark khi đổi máy tính:
  - Mở trình duyệt chọn vào ảnh đại diện ở góc trên cùng bên phải -> chọn add -> Đặt tên lần lượt là Perosnal, Work, Sandbox -> Cấu hình bảo mật riêng biệt gắn tài khoản gmail vào person, gắn tài khoản email vào Work, để trống cho tài khoản Sandbox.
  - Đăng nhập tài khoản tương ứng với từng Profile -> Vào settings -> bật tính năng Sync -> tích chọn đồng bộ mục Bookmark
3. Phần III. Kiểm thử
- Mở trình duyệt -> Chọn mục sử dụng chế độ khách 
- Quy tắc bảo mật chế độ khách tạo ra một không gian độc lập, không lưu lịch sử, dữ liệu trong cookies khi đóng cửa sổ thì sẽ mất hết tất cả dữ liệu 

