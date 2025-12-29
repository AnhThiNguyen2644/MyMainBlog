---
title: "Đóng gói và giải mã dữ liệu JSON"
date: 2025-12-19
draft: false
cover:
    image: "/anh8.png"  # Đường dẫn ảnh trong thư mục static
    alt: "Mô hình kết nối TCP" # Chữ hiện ra nếu ảnh lỗi
    caption: "Mô hình Client-Server cơ bản" # Chú thích nhỏ dưới ảnh
    relative: false # Để false để dùng đường dẫn tuyệt đối từ static
---

### 1. JSON là gì?
JSON (JavaScript Object Notation) là định dạng dữ liệu nhẹ, dễ đọc, được dùng để trao đổi dữ liệu giữa Server (Java) và Client (JavaScript).

### 2. Thao tác với JSON trong JS
```javascript
const user = { id: 1, name: "AnhThi" };

// Chuyển đối tượng thành chuỗi để gửi đi
const jsonString = JSON.stringify(user);

// Chuyển chuỗi nhận được thành đối tượng để sử dụng
const obj = JSON.parse(jsonString);


### 1. JSON - Ngôn ngữ chung của Internet
JSON (JavaScript Object Notation) đã thay thế hoàn toàn XML để trở thành tiêu chuẩn truyền tải dữ liệu giữa Server (Java) và Client (JS). Nó có cấu trúc phân cấp, gọn nhẹ và tiết kiệm băng thông tối đa cho người dùng di động.

### 2. Thao tác nâng cao với JSON
```javascript
// Dữ liệu phức tạp từ Server Java gửi về
const rawData = '{"id": 101, "status": "active", "tags": ["java", "network"]}';

// Giải mã (Parsing)
const project = JSON.parse(rawData);
console.log(project.tags[0]); // Kết quả: java

// Đóng gói (Stringify) với định dạng đẹp để debug
const formattedJSON = JSON.stringify(project, null, 4);