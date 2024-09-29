# Hướng dẫn sử dụng G3tm31fy0uc4n

## Thống nhất khi làm việc

### Dữ liệu

- Quy tắc đặt tên file dữ liệu: [Tên]_[ORI/EMBEDED]_[Dùng cho] (ORI là file gốc, chưa thông qua embedding)
  VD: APIMDS_ORI_BERT
- Đối với các file dữ liệu không rõ tên: [Tên tượng trưng]_[ORI/EMBEDED]_[Dùng cho] / [Tên tượng trưng]_[chỉ số]_[ORI/EMBEDED]\_[Dùng cho] (Đối với các file bị phân tách do lưu lượng quá lớn,...)
  VD: Data_ORI_BERTSMALL, DataSplit0_BERTBASE,...
- Các file khi được upload lên vui lòng kèm theo phần hướng dẫn sử dụng trong file "README.md" trong folder "Data" .
  VD: Data_EMBEDED_GATv2 sử dụng cho file GATv2.py -> Chạy như thế nào,...

### Model & Embedding

- Quy tắc đặt tên: [Tên Model/Embedding]
- Viết file "README.md" trong folder "Model/Embedding" giải thích cách chạy ra sao.

## Lưu ý: File dữ liệu vui lòng nén thành .rar sau đó mới up lên, mật khẩu vui lòng đặt theo tin nhắn đã bàn trước (Unsolve)

## Git rule

- Quy tắc đặt tên branch:
  - Tên branch nên bắt đầu bằng từ "create/" hoặc "fix/" tương ứng với tạo hoặc sửa, sau "/" là tạo hoặc sửa tên của tệp tin tương ứng muốn làm gì với file đó, cuối cùng thêm "-[tên mình]".
    VD: Tạo file data.rar chứa dữ liệu: create/data-Trung; fix/bert-Trung
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
  - **Model/**
    - models.md
  - README.md
  - requirements.txt

# ---- CÒN UPDATE ----
