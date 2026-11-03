# 4.Yêu cầu đầu ra
1. Phần I. Phân tích
- Inspect -> Chọn Network -> Tích chọn ô Disable Cache -> và tải lại trang
- Dựa trên các hiện tượng lỗi nút thắt cổ chai dựa theo 2 phần chính: file hình ảnh chứa dung lượng lớn, Các yêu cầu bị lỗi (Status 404)
2. Phần II. Triển khai
- Bước 1: Sửa đổi đứt link (Rà soát lại đường dẫn, loại bỏ hoàn toàn các request bị lỗi)
- Bước 2: Nén và chuyển đổi định dạng tài nguyên hình ảnh(chuyển đổi dung lượng định dạng ảnh)
- Bước 3: Thiết lập Browser Cache cho tài nguyên tĩnh(Cấu hình trên Web Server cho các file tĩnh với thời gian sống dài)
3. Phần III. Kiểm thử
- Mã trạng thái 304 Not Modified là một phản hồi giống như chuyển hướng, cho biết rằng máy chủ không cần phải truyền tài nguyên được yêu cầu vì máy khách đã có một phiên bản cập nhật trong bộ nhớ đệm cục bộ của nó. Giúp giảm băng thông truyền tải, cải thiện tốc độ tải trang, giảm tải cho máy chủ.