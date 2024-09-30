# Hướng dẫn sử dụng G3tm31fy0uc4n

## 1. Quy tắc chung khi làm việc

### 1.1. Dữ liệu

- **Quy tắc đặt tên file dữ liệu:**  
  `[RAW/PR/EMB]_[Tên]_[Sử dụng cho]`  
  Trong đó:

  - **RAW**: Dữ liệu nguyên gốc.
  - **PR**: Dữ liệu qua xử lý làm sạch
  - **EMB**: Dữ liệu đã qua quá trình embedding.
    **Ví dụ:**  
    `RAW_APIMDS_BERT`: Dữ liệu APIMDS nguyên gốc dùng cho BERT.

- **Đối với các file dữ liệu không rõ tên:**  
  `[RAW/PR/EMB]_[Tên tượng trưng]_[Sử dụng cho]`  
  Hoặc nếu file bị phân tách do dung lượng lớn: (gộp lại file .rar đặt tên không có chỉ số)
  `[RAW/PR/EMB]_[Tên tượng trưng]_[Chỉ số]_[Sử dụng cho]`
  **Ví dụ:**  
  `RAW_FromCuckoo_BERTSMALL`, `PR_FromCuckoo_0_BERTBASE`.

- **README.md cho dữ liệu:**  
  Mỗi lần upload dữ liệu, vui lòng tạo file `README.md` trong thư mục **Data/** để hướng dẫn cách sử dụng file dữ liệu.  
  **Ví dụ:**  
  `RAW_EMB_GATv2` sử dụng cho file `GATv2.py`. Trong README.md ghi rõ cách chạy file này.

- **Phân loại các file Data vào 3 thư mục riêng tương ứng label của chúng:**
  **Ví dụ:**  
  `RAW_APIMDS_BERT`: Đưa vào folder "/Data/RAW"

### 1.2. Model & Embedding

- **Quy tắc đặt tên:**  
  `Model/Embedding_[Tên Model/Embedding]`
  **Ví dụ:**
  `Model_GATv2`

- **README.md cho Model/Embedding:**  
  Mỗi model hoặc embedding cần có file `README.md` trong thư mục **Model/** hoặc **Embedding/**. Nội dung file này cần giải thích cách chạy, cách thay đổi để sử dụng với dữ liệu khác.

- **Lưu ý**
  Nếu như các model hoặc embedding có thể tái sử dụng đoạn code lấy dữ liệu, hoặc có thể tối ưu thời gian. Gộp vào thành 1 file và đặt tên thành `Model/Embedding_[Tên đại diện cho thuật toán]`
  **Ví dụ:**
  `Model_GNN`

### 1.3. Code

- **Quy tắc đặt tên hàm và biến:**

  - Đặt tên theo mẫu: `[Động từ][Something]`.  
    Trong đó, **Động từ** viết thường, **Something** viết hoa chữ cái đầu (viết hoa toàn bộ nếu đó là cụm từ viết tắt).  
    **Ví dụ:**  
    `createBERT`, `processData`.

- **Comment trong code:**  
   Vui lòng thêm chú thích (comment) cho mỗi đoạn code riêng biệt, mô tả chức năng của đoạn code đó. Đặt theo mẫu `[Vắn tắt].
  **Ví dụ:**  
`# Hàm createBERT tạo embedding cho dữ liệu`

### 1.4. Task

- **Cách đặt tên Task:**  
  `[Tên người nhận]_[Create/Fix/RemoveF/Feature]_[Vắn tắt muốn làm gì với các tùy chọn [FIX/REMOVEF/FEATURE]_[Data/Model/Embed]_[TASK]`.  
  Trong đó, **TASK** là đối tượng cần làm, **Create** là tạo mới, **Fix** là sửa lỗi, **RemoveF** là xóa chức năng, hoặc những thứ không cần thiết, **Feature** để thêm chức năng, các vắn tắt có thể là hàm trong code.
  **Ví dụ:**  
  `Trung_Create_Embed_BERT`, `Trung_Feature_512Dimension_Embed_BERT` -> Trung hãy tạo mô hình embedding BERT nhé , Trung thêm chúc năng cho mô hình embedding BERT tạo ra vector 512 chiều nhé

## 2. Lưu ý về dữ liệu

- File dữ liệu cần nén thành `.rar` trước khi upload.
- Mật khẩu giải nén sẽ theo thỏa thuận trước đó (không giải quyết qua tin nhắn công khai).

## 3. Git Rule

### 3.1. Quy tắc đặt tên branch

- **Tên branch:**  
  Đặt tên branch theo TASK
  **Ví dụ:**  
  `Trung_Create_Embed_BERT`, `Trung_Fix_512Dimension_Embed_BERT`

### 3.2. Quy tắc đặt tên commit

- **Tên commit:**  
  Khi commit, cần thêm nội dung ngắn gọn diễn đạt đủ ý đã thực hiện.
  Quy tắc đặt commit: [Động từ] [Đối tượng] [Cho đối tượng khác (nếu có)]
  **Ví dụ:**  
  `Create file APIMDS original for BERT-BASE`.

- **Lưu ý:**
  Nên commit khi có thay đổi nhỏ, tránh commit khi thay đổi một lượng lớn

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
  │   ├── README.md
  │   ├── RAW
  │   ├── PR
  │   └── EMB
  ├── Embedding/
  │   └── README.md
  ├── Models/
  │   └── README.md
  └── README.md
```
