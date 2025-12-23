---
title: "Lấy dữ liệu mạng bằng Fetch API trong JavaScript"
date: 2025-12-19
draft: false
cover:
    image: "/bai6.png"  # Đường dẫn ảnh trong thư mục static
    alt: "Mô hình kết nối TCP" # Chữ hiện ra nếu ảnh lỗi
    caption: "Mô hình Client-Server cơ bản" # Chú thích nhỏ dưới ảnh
    relative: false # Để false để dùng đường dẫn tuyệt đối từ static
---

### 1. Fetch API là gì?
`fetch()` là một phương thức hiện đại trong JavaScript giúp chúng ta gửi các yêu cầu mạng (HTTP request) tới Server để lấy dữ liệu (thường là định dạng JSON).

### 2. Ví dụ lấy dữ liệu từ một API công khai
```javascript
fetch('[https://jsonplaceholder.typicode.com/users/1](https://jsonplaceholder.typicode.com/users/1)')
  .then(response => response.json())
  .then(data => {
    console.log("Tên người dùng:", data.name);
  })
  .catch(error => console.error('Lỗi:', error));

  Khi làm việc với mạng, dữ liệu trả về đôi khi không đúng định dạng. Việc sử dụng try...catch kết hợp với response.ok là bắt buộc để kiểm tra mã trạng thái HTTP (như 404 - không tìm thấy, 500 - lỗi server) trước khi tiến hành xử lý dữ liệu tiếp theo.