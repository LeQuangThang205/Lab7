# BÁO CÁO LAB 7: KIỂM THỬ API BẰNG POSTMAN

- **Họ và tên:** Lê Quang Thắng
- **Mã sinh viên:** 23010236
- **Lớp:** CNTT_3

---

## 1. Giới thiệu công cụ Postman
Postman là công cụ phổ biến dùng để kiểm thử API, gửi các yêu cầu HTTP/HTTPS và kiểm tra kết quả phản hồi từ máy chủ.

## 2. Kết quả kiểm thử API

### 2.1. Kiểm thử Request GET (Lấy dữ liệu)
- **URL:** `https://jsonplaceholder.typicode.com/posts/1`
- **Phương thức:** GET
- **Mô tả:** Lấy thông tin bài viết có ID = 1.
- **Kết quả:** Status `200 OK`.
![GET Request]<img width="1607" height="1007" alt="Ảnh chụp màn hình 2026-10-07 164903" src="https://github.com/user-attachments/assets/e5bfc808-2f63-4183-9e85-70aa2cab467e" />


### 2.2. Kiểm thử Request POST (Tạo mới dữ liệu)
- **URL:** `https://jsonplaceholder.typicode.com/posts`
- **Phương thức:** POST
- **Mô tả:** Gửi payload JSON để tạo mới bài viết.
- **Kết quả:** Status `201 Created`.
![POST Request]<img width="1610" height="1000" alt="Ảnh chụp màn hình 2026-10-07 165852" src="https://github.com/user-attachments/assets/06fca4eb-a22e-4a78-9881-a2407084a6f5" />

### 2.3. Kiểm thử Request PUT (Cập nhật dữ liệu)
- **URL:** `https://jsonplaceholder.typicode.com/posts/1`
- **Phương thức:** PUT
- **Mô tả:** Yêu cầu cập nhật bài viết có ID = 1.
- **Kết quả:** Status `200 OK`.
![DELETE Request]<img width="1600" height="990" alt="Ảnh chụp màn hình 2026-10-07 165731" src="https://github.com/user-attachments/assets/efc99bb6-4ba8-4b6c-8779-6b6e3f10df11" />


### 2.4. Kiểm thử Request DELETE (Xóa dữ liệu)
- **URL:** `https://jsonplaceholder.typicode.com/posts/1`
- **Phương thức:** DELETE
- **Mô tả:** Yêu cầu xóa bài viết có ID = 1.
- **Kết quả:** Status `200 OK`.
![DELETE Request]<img width="1603" height="1003" alt="Ảnh chụp màn hình 2026-10-07 165804" src="https://github.com/user-attachments/assets/3ebfc8ba-684c-4bd6-8a43-0bd74e2a25af" />


---
## 3. Kết luận
Đã nắm rõ quy trình gửi request, truyền tham số, truyền body JSON và kiểm tra Status Code trên Postman.
