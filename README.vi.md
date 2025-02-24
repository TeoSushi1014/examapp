# Ứng Dụng Thi Trắc Nghiệm

> **Ghi chú**: 
> - Để xem phiên bản tiếng Anh của README này, vui lòng tham khảo [README.md](README.md)
> - Để xem hướng dẫn phát triển chi tiết bằng tiếng Anh, xem [DEVELOPMENT.md](DEVELOPMENT.md)
> - Để xem hướng dẫn phát triển chi tiết bằng tiếng Việt, xem [DEVELOPMENT.vi.md](DEVELOPMENT.vi.md)

**Project Repository**: [@TeoSushi1014/examapp](https://github.com/TeoSushi1014/examapp)

## Mô Tả Dự Án

Ứng dụng này quản lý và xử lý các đề thi trắc nghiệm. Mỗi câu hỏi trong đề thi bao gồm:
- Nội dung câu hỏi
- Nội dung đáp án A
- Nội dung đáp án B
- Đáp án đúng (A hoặc B)

## Tính Năng Chính

1. **Tạo Đề Thi Trắc Nghiệm**
   - Tạo đề thi mới với nhiều câu hỏi
   - Nhập từ bàn phím
   - Lưu vào file định dạng `*.TTN`

2. **Đọc và Làm Bài Thi**
   - Đọc nội dung đề thi từ file `*.TTN`
   - Cho phép người dùng làm bài thi
   - Kiểm tra và hiển thị kết quả

3. **Xử Lý File**
   - Đọc file `*.TTN`
   - Xóa khoảng trống thừa ở câu hỏi và đáp án
   - Lưu thay đổi vào file gốc

4. **So Sánh Câu Hỏi**
   - Kiểm tra hai câu hỏi có trùng nhau không
   - So sánh dựa trên nội dung, đáp án và đáp án đúng

## Chi Tiết Kỹ Thuật

### Lớp `CauhoiTN`

#### Thuộc Tính
- `noidung`: Nội dung câu hỏi
- `dapAnA`: Nội dung đáp án A
- `dapAnB`: Nội dung đáp án B
- `dapAnDung`: Đáp án đúng (A hoặc B)

#### Phương Thức
- `nhap()`: Nhập câu hỏi từ bàn phím
- `docfile()`: Đọc câu hỏi từ file
- `ghifile()`: Ghi câu hỏi vào file
- `kiemtra()`: Kiểm tra câu trả lời của người dùng
- `xuat()`: Hiển thị câu hỏi
- `giongnhau()`: So sánh hai câu hỏi có giống nhau không

## Yêu Cầu Phát Triển

1. **File Cần Nộp**
   - File chụp màn hình khi thực thi ứng dụng
   - File nén source code

2. **Thông Tin Sinh Viên**
   - Hiển thị MSSV và họ tên khi bắt đầu chương trình

## Cách Sử Dụng

1. Chạy ứng dụng
2. Chọn từ menu các chức năng:
   - Tạo đề thi mới
   - Đọc và làm bài thi
   - Chỉnh sửa file đề thi (xóa khoảng trống thừa)
   - Kiểm tra câu hỏi trùng nhau
   - Thoát chương trình

## Hướng Dẫn Phát Triển

1. **Triển Khai Lớp**
   - Triển khai lớp `CauhoiTN` với đầy đủ thuộc tính và phương thức
   - Đảm bảo xử lý file định dạng `*.TTN` đúng cách

2. **Hệ Thống Menu**
   - Triển khai giao diện menu thân thiện với người dùng
   - Xử lý tất cả đầu vào của người dùng phù hợp

3. **Thao Tác File**
   - Triển khai đọc và ghi file đúng cách
   - Xử lý xóa khoảng trống chính xác

4. **Kiểm Thử**
   - Kiểm tra kỹ lưỡng tất cả tính năng
   - Xác minh việc kiểm tra đáp án đúng
   - Đảm bảo phát hiện câu hỏi trùng lặp chính xác 