# Hướng dẫn sử dụng G3tm31fy0uc4n

## 1. Quy tắc chung khi làm việc

### 1.1. Dữ liệu

- **Quy tắc đặt tên file dữ liệu:**  
  `Data_[Tên]_[RAW/PR/EMB]_[Sử dụng cho]`  
  Trong đó:

  - **RAW**: Dữ liệu nguyên gốc.
  - **PR**: Dữ liệu đang xử lý.
  - **EMB**: Dữ liệu đã qua quá trình embedding.
  **Ví dụ:**  
  `Data_APIMDS_RAW_BERT`: Dữ liệu APIMDS nguyên gốc dùng cho BERT.

- **Đối với các file dữ liệu không rõ tên:**  
  `Data_[Tên tượng trưng]_[RAW/PR/EMB]_[Sử dụng cho]`  
  Hoặc nếu file bị phân tách do dung lượng lớn:  
  `Data_[Tên tượng trưng]_[chỉ số]_[RAW/PR/EMB]_[Sử dụng cho]`
  **Ví dụ:**  
  `Data_FromCuckoo_RAW_BERTSMALL`, `Data_Split_0_PR_BERTBASE`.

- **README.md cho dữ liệu:**  
  Mỗi lần upload dữ liệu, vui lòng tạo file `README.md` trong thư mục **Data/** để hướng dẫn cách sử dụng file dữ liệu.  
  **Ví dụ:**  
  `Data_EMB_GATv2` sử dụng cho file `GATv2.py`. Trong README.md ghi rõ cách chạy file này.

- **Phân loại các file Data vào 3 thư mục riêng tương ứng label của chúng:**
  **Ví dụ:**  
  `Data_APIMDS_RAW_BERT`: Đưa vào folder "/Data/RAW"

### 1.2. Model & Embedding

- **Quy tắc đặt tên:**  
  `Model/Embedding_[Tên Model/Embedding]`
  **Ví dụ:**
  `Model_GATv2`

- **README.md cho Model/Embedding:**  
  Mỗi model hoặc embedding cần có file `README.md` trong thư mục **Model/** hoặc **Embedding/**. Nội dung file này cần giải thích cách chạy, cách thay đổi để sử dụng với dữ liệu khác.

### 1.3. Code

- **Quy tắc đặt tên hàm và biến:**

  - Đặt tên theo mẫu: `[Động từ][Something]`.  
    Trong đó, **Động từ** viết thường, **Something** viết hoa chữ cái đầu (viết hoa toàn bộ nếu đó là cụm từ viết tắt).  
    **Ví dụ:**  
    `createBERT`, `processData`.

- **Comment trong code:**  
  Vui lòng thêm chú thích (comment) cho mỗi đoạn code riêng biệt, mô tả chức năng của đoạn code đó.  
  **Ví dụ:**  
  `# Hàm createBERT tạo embedding cho dữ liệu.`

### 1.4. Task

- **Quản lý task bằng Issue:**  
  Các task sẽ được quản lý thông qua mục **Issue**.

- **Cách đặt tên Title của Issue:**  
  `ISSUE_[Tên người nhận]-[Create/Update]-[TASK]`.  
  Trong đó, **TASK** là đối tượng cần làm.
  **Ví dụ:**  
  `ISSUE_Trung-Create-BERT`.

- **Description của Issue:**  
  Ghi rõ chi tiết yêu cầu công việc, hướng dẫn và các thông tin cần thiết. Nếu có deadline, thêm vào cuối phần Description.

- **Assign task:**  
  Vui lòng assign task cho người thực hiện trong Issue.


## 2. Lưu ý về dữ liệu

- File dữ liệu cần nén thành `.rar` trước khi upload.
- Mật khẩu giải nén sẽ theo thỏa thuận trước đó (không giải quyết qua tin nhắn công khai).

## 3. Git Rule

### 3.1. Quy tắc đặt tên branch

- **Tên branch:**  
  Đặt tên branch theo Title của Task trong mục Issue (bỏ qua chữ ISSUE) 
  **Ví dụ:**  
  `Trung-Create-BERT`.

### 3.2. Quy tắc đặt tên commit

- **Tên commit:**  
  Khi commit, cần thêm message tóm tắt ngắn gọn nội dung.  
  **Ví dụ:**  
  `Create file APIMDS original for BERT-BASE`.

## 4. Git Tutorial

### 4.1. Các bước trước khi push code lên GitHub

- Bước 1: `git clone [repository link]` để tải repository về máy.
- Bước 2: `git remote add [tên remote] [link remote]` để thêm liên kết với remote repository.

### 4.2. Các bước để push lên GitHub

1. Tạo nhánh mới: `git branch [tên nhánh]`
2. Chuyển sang nhánh mới: `git checkout [tên nhánh]`
3. Cập nhật thông tin từ repository chính: `git pull`
4. Thêm thay đổi trong nhánh local: `git add .`
5. Commit thay đổi: `git commit -m "[tin nhắn]"`
6. Push lên remote: `git push [tên remote]`
7. Truy cập GitHub để tạo Pull Request, yêu cầu review.

## 5. Cấu trúc thư mục

```plaintext
G3tm31fy0uc4n/
  ├── Data/
  │   └── README.md
  ├── Embedding/
  │   └── README.md
  ├── Models/
  │   └── README.md
  └── README.md
```
