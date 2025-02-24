# Hướng Dẫn Phát Triển Ứng Dụng Trắc Nghiệm

## Mô Tả Ứng Dụng

Ứng dụng này quản lý và xử lý các đề thi trắc nghiệm. Mỗi câu hỏi trong đề thi bao gồm các thành phần:
- **Nội dung câu hỏi**
- **Nội dung đáp án A**
- **Nội dung đáp án B**
- **Đáp án đúng** (A hoặc B)

Ứng dụng có các chức năng chính như sau:
1. **Tạo đề thi trắc nghiệm** gồm nhiều câu hỏi, nhập từ bàn phím và lưu vào file định dạng `*.TTN`.
2. **Đọc nội dung file `*.TTN`** để cho người dùng thi.
3. **Đọc một file `*.TTN`** và xóa khoảng trống thừa ở các câu hỏi và đáp án, sau đó lưu đè lên file cũ.
4. **Kiểm tra xem hai câu hỏi có trùng nhau hay không.**

## Các Phương Thức và Chức Năng

### 1. **Lớp `CauhoiTN`**

Lớp `CauhoiTN` có các thuộc tính và phương thức như sau:

#### Thuộc tính
- **noidung**: Nội dung câu hỏi.
- **dapAnA**: Nội dung đáp án A.
- **dapAnB**: Nội dung đáp án B.
- **dapAnDung**: Đáp án đúng (A hoặc B).

#### Phương thức
- **`nhap()`**: Nhập liệu câu hỏi từ bàn phím, bao gồm nội dung câu hỏi, đáp án A, đáp án B và đáp án đúng.
- **`docfile(ifstream& f)`**: Đọc câu hỏi từ file stream `f` và lưu vào các thuộc tính tương ứng.
- **`ghifile(ofstream& f)`**: Ghi nội dung câu hỏi vào file stream `f`.
- **`kiemtra()`**: Hiển thị câu hỏi và cho phép người dùng nhập câu trả lời. Phương thức kiểm tra xem câu trả lời có đúng không và thông báo kết quả.
- **`xuat()`**: Xuất câu hỏi ra màn hình, bao gồm nội dung câu hỏi, đáp án A, B và đáp án đúng.
- **`giongnhau(CauhoiTN cau1, CauhoiTN cau2)`**: Hàm kiểm tra xem hai câu hỏi có giống nhau hay không, sử dụng từ khoá `friend`.

### 2. **Thực Đơn (Menu)**
Ứng dụng sẽ có một thực đơn để người dùng lựa chọn các chức năng sau:
- Tạo đề thi trắc nghiệm mới từ bàn phím và lưu vào file.
- Đọc đề thi từ file và cho người dùng thi.
- Đọc và chỉnh sửa file để xóa khoảng trống thừa.
- Kiểm tra câu hỏi có trùng nhau hay không.
- Thoát chương trình.

### 3. **Các Chức Năng Chính**
1. **Tạo đề thi trắc nghiệm:**
   - Người dùng có thể nhập các câu hỏi trắc nghiệm từ bàn phím. Mỗi câu hỏi sẽ bao gồm nội dung câu hỏi, nội dung đáp án A, B và đáp án đúng.
   - Các câu hỏi này sẽ được lưu vào file có định dạng `*.TTN`.

2. **Đọc nội dung từ file và thi:**
   - Người dùng có thể chọn một đề thi có sẵn từ file `*.TTN`. Các câu hỏi sẽ được đọc và hiển thị cho người dùng để thi.
   - Người dùng sẽ nhập câu trả lời và ứng dụng sẽ kiểm tra đáp án của họ.
   
3. **Chỉnh sửa file đề thi:**
   - Chức năng này cho phép người dùng đọc một file `*.TTN` và xóa khoảng trống thừa ở các câu hỏi và đáp án.
   - Sau khi loại bỏ khoảng trống thừa, file sẽ được lưu đè lại với nội dung mới.

4. **Kiểm tra câu hỏi trùng nhau:**
   - Hàm `giongnhau()` sẽ kiểm tra xem hai câu hỏi có trùng nhau hay không, dựa trên nội dung câu hỏi, đáp án A, đáp án B và đáp án đúng.

## Yêu Cầu Phát Triển

1. **Tạo lớp `CauhoiTN`** với các thuộc tính và phương thức đã mô tả ở trên.
2. **Xây dựng menu** cho phép người dùng lựa chọn chức năng, bao gồm:
   - Tạo đề thi mới.
   - Đọc file và thi.
   - Chỉnh sửa file (xóa khoảng trống thừa).
   - Kiểm tra câu hỏi trùng nhau.
   - Thoát chương trình.
3. **Viết hàm `giongnhau(CauhoiTN cau1, CauhoiTN cau2)`** để kiểm tra câu hỏi có giống nhau hay không, sử dụng từ khóa `friend`.

## Lưu Ý

- **Sinh viên cần nộp 2 file**:
  1. **File chụp màn hình** khi thực thi ứng dụng, hiển thị kết quả sau khi người dùng nhập câu hỏi, thi, và kiểm tra đáp án.
  2. **File nén source code** của dự án để gửi lại cho giảng viên.

- **Thông tin sinh viên**: Dòng đầu tiên của chương trình cần in ra thông tin của sinh viên (MSSV và Họ tên) khi bắt đầu chương trình.

## Các Bước Phát Triển Ứng Dụng

1. **Thiết kế lớp `CauhoiTN`**:
   - Các thuộc tính và phương thức của lớp sẽ giúp quản lý và xử lý câu hỏi trắc nghiệm.
   - Lớp này cần phải có các phương thức nhập liệu, đọc và ghi file, kiểm tra câu trả lời và xuất câu hỏi ra màn hình.

2. **Xây dựng menu**:
   - Menu sẽ bao gồm các chức năng cho người dùng lựa chọn như tạo đề thi, đọc và thi, chỉnh sửa file đề thi, và kiểm tra câu hỏi trùng nhau.

3. **Kiểm tra và chỉnh sửa file**:
   - Cần đảm bảo rằng các file `*.TTN` có thể được đọc, chỉnh sửa (loại bỏ khoảng trống thừa) và lưu lại đúng cách.

4. **Kiểm thử ứng dụng**:
   - Sau khi phát triển xong, cần kiểm thử ứng dụng để đảm bảo mọi chức năng hoạt động chính xác, bao gồm việc kiểm tra câu hỏi trùng nhau và kiểm tra câu trả lời đúng/sai.

5. **Chuẩn bị nộp bài**:
   - Chụp màn hình khi ứng dụng đang chạy, bao gồm quá trình nhập câu hỏi, thực hiện thi và kiểm tra kết quả.
   - Nén toàn bộ mã nguồn dự án vào một file và gửi kèm với file chụp màn hình.

## Kết Luận

Ứng dụng này sẽ giúp quản lý và xử lý các câu hỏi trắc nghiệm, cho phép người dùng tạo, chỉnh sửa và thi các câu hỏi một cách dễ dàng. Các chức năng như kiểm tra đáp án đúng/sai và kiểm tra câu hỏi trùng nhau sẽ giúp ứng dụng trở nên hữu ích và hiệu quả cho người dùng.
