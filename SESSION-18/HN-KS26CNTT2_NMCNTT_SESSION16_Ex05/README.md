# 4.Yêu cầu đầu ra
1. Phần I. Phân tích
- Vai trò của JSON Viewer trong việc gỡ lỗi dữ liệu API thô từ máy chủ: tự động phân tách các cặp giá trị theo dạng thư mục cây, cho phép ẩn bớt các nhánh dữ liệu không liên quan để tập trung vào luồng cần kiểm tra, Giúp định vị chính xác thông số thời gian thực mà không mất thời gian đọc thủ công chuỗi ký tự dài
2. Phần II. Triển khai
- Nhóm 1 (API): JSON Viewer, ModHeader
- Nhóm 2 (Extension personal): Color Eyedropper, Onetab
- Nhóm 3 (Security): uBlockOrigin
- Cách ghim ToolBar: Nhấn vào biểu tượng Extension -> Tìm đến tiện ích cần thiết -> Nhấn vào biểu tượng Ghim để đưa icon tiện ích ra bên ngoài 
3. Phần III. Kiểm thử
- Nhấn tổ hợp phím Shift + Esc để mở quản lý dữ liệu ở trên Chrome -> Quan sát cột Memory footprint để kiểm tra dung lượng bộ nhớ -> Khi phát hiện bộ nhớ chiếm nhiều RAM thì nhấn chuột phải vào extension và gỡ bỏ.