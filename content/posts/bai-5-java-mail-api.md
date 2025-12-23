---
title: "Xây dựng ứng dụng Chat đơn giản với Java"
date: 2025-12-19
draft: false
cover:
    image: "/bai5.jpg"  # Đường dẫn ảnh trong thư mục static
    alt: "Mô hình kết nối TCP" # Chữ hiện ra nếu ảnh lỗi
    caption: "Mô hình Client-Server cơ bản" # Chú thích nhỏ dưới ảnh
    relative: false # Để false để dùng đường dẫn tuyệt đối từ static
---

### 1. Ý tưởng hệ thống Chat
Hệ thống Chat yêu cầu Server phải nhận tin nhắn từ một người và "phát tán" (broadcast) tin nhắn đó tới tất cả những người đang tham gia.

### 2. Sử dụng `PrintWriter` và `BufferedReader`
Để gửi tin nhắn văn bản dễ dàng, chúng ta thường bao bọc luồng dữ liệu bằng `PrintWriter`.

```java
// Gửi tin nhắn
PrintWriter out = new PrintWriter(socket.getOutputStream(), true);
out.println("Chào mọi người!");

// Nhận tin nhắn
BufferedReader in = new BufferedReader(new InputStreamReader(socket.getInputStream()));
String msg = in.readLine();