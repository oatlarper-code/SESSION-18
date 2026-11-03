# 4.Yêu cầu đầu ra
1. Phần I. Phân tích
- Inspect -> Vào phần Computed lấy sơ đồ Box Model 
- Sửa đổi Sơ đồ Box Model:
  - Margin: 0px
  - Padding: 12px
  - Border: 1px solid 
  - Content: width 100%, height 200px
2. Phần II. Triển khai
- Đưa ra thông số CSS mới giúp sửa lỗi chồng lấn giao diện
  - `display: flex; flex-direction: column; gap: 16px; position: relative`
  -  `position: relative; margin-bottom: 20px; z-index: 10;` (Giữ lại khung thông tin tài xế)
3. Phần III. Kiểm thử
- Thuộc tính Position đang là absolute hoặc fixed cách khắc phục thay đổi position thành relative hoặc static, hoặc điều chỉnh tọa độ top, bottom
- Kiểu hiển thị display:inline không nhận khoảng cách margin-top và margin-bottom phải chuyển thuộc tính display:block vào phần tử
- Xung đột độ ưu tiên hoặc cờ !important trong file gốc bị ghi đè giá trị margin vừa nhập kiểm tra thuộc tính có bị gạch ngang hay không Nếu có thì thêm giá trị !important của bạn để ép Browser Engine ưu tiên thực hiện.
