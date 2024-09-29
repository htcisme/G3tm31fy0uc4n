# Hướng dẫn sử dụng G3tm31fy0uc4n

## Thống nhất khi làm việc

### Dữ liệu

- Quy tắc đặt tên file dữ liệu: [Tên]_[RAW/PR/EMB]_[Dùng cho] (RAW nguyên gốc, PR đang xử lý, EMB đã qua embedding)
  VD: APIMDS_RAW_BERT


- Đối với các file dữ liệu không rõ tên: [Tên tượng trưng]_[RAW/PR/EMB]_[Dùng cho] / [Tên tượng trưng]_[chỉ số]_[RAW/PR/EMB]\_[Dùng cho] (Đối với các file bị phân tách do lưu lượng quá lớn,...)
  VD: Data_ORI_BERTSMALL, DataSplit0_BERTBASE,...


- Các file khi được upload lên vui lòng kèm theo phần hướng dẫn sử dụng trong file "README.md" trong folder "Data" .
  VD: Data_EMBEDED_GATv2 sử dụng cho file GATv2.py -> Chạy như thế nào,...

### Model & Embedding

- Quy tắc đặt tên: [Tên Model/Embedding]


- Viết file "README.md" trong folder "Model/Embedding" giải thích cách chạy ra sao, sửa những gì nếu muốn chạy một file dữ liệu khác.

### Code

- Đối với tên hàm, tên biến:
  - Đặt tên theo [Động từ][Something], động từ sẽ ghi thường, Something ghi hoa chữ cái đầu (Ghi hoa hết nếu đó là một cụm)
    VD: createBERT, processData


- Vui lòng thêm comment trên mỗi đoạn code riêng biệt
  VD: Hàm createBERT để làm tạo embedding

### Task

- Các task sẽ được đặt trong phần Issue để dễ quản lý


- Title của Issue sẽ được đặt tên theo cách sau: [Tên người nhận]-[Create/Update]-[TASK] (trong đó "TASK" là đối tượng hướng tới)
  VD: Trung-Create-BERT


- Phần "Description" ghi rõ chi tiết muốn người đó thực hiện những gì, yêu cầu công việc ra sao


- Vui lòng Assign người nhận task vào issue


- Có thể kèm Deadline vào cuối Description (nếu có)

## Lưu ý: File dữ liệu vui lòng nén thành .rar sau đó mới up lên, mật khẩu vui lòng đặt theo tin nhắn đã bàn trước (Unsolve)

## Git rule

- Quy tắc đặt tên branch:
  - Tên branch đặt tên bằng tên "Title" của "Task" trong "Issue"
    VD: Trung-Create-BERT


- Quy tắc tên commit:
  - Khi commit, vui lòng gửi message tóm tắt ngắn gọn những gì đã push lên.
    VD: Create file APIMDS original for BERT-BASE

## Git turtorial

- Một số quá trình trước khi thực hiện push:
  - Bước 1: Git clone về máy
  - Bước 2: git remote add [tên remote] [link git]


- Để push lên Github vui lòng thực hiện theo cách sau:
  - Bước 1: Tạo nhánh mới: git branch [tên nhánh]
  - Bước 2: Vào nhánh mới: git check out [tên nhánh]
  - Bước 3: git pull để cập nhập thông tin
  - Bước 4: git add . :để thêm những thay đổi trong local branch
  - Bước 5: git commit -m "[tin nhắn]"
  - Bước 6: git push [tên remote]
  - Bước 7: Lên github đẩy pull request để bắt đầu review

# Cấu trúc thư mục

- **G3tm31fy0uc4n/**
  - **Data/**
    - README.md
  - **Embedding/**
    - README.md
  - **Models/**
    - README.md
  - README.md


# ---- CÒN UPDATE ----
