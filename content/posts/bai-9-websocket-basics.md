---
title: "Giới thiệu về kết nối thời gian thực WebSocket"
date: 2025-12-19
draft: false
cover:
    image: "/bai9.webp"  # Đường dẫn ảnh trong thư mục static
    alt: "Mô hình kết nối TCP" # Chữ hiện ra nếu ảnh lỗi
    caption: "Mô hình Client-Server cơ bản" # Chú thích nhỏ dưới ảnh
    relative: false # Để false để dùng đường dẫn tuyệt đối từ static
---

### 1. WebSocket vs HTTP
Khác với HTTP (Client hỏi - Server trả lời), WebSocket cho phép tạo ra một đường ống kết nối luôn mở, giúp cả hai bên có thể gửi dữ liệu cho nhau bất cứ lúc nào.

### 2. Ví dụ WebSocket đơn giản (Client)
```javascript
const socket = new WebSocket('ws://localhost:8080');

socket.onopen = () => {
    socket.send('Xin chào Server!');
};

socket.onmessage = (event) => {
    console.log('Nhận tin nhắn từ Server:', event.data);
};

### 1. Cuộc cách mạng từ HTTP lên WebSocket
Giao thức HTTP truyền thống hoạt động theo kiểu "Hỏi - Đáp": Client hỏi thì Server mới trả lời. WebSocket phá vỡ rào cản này bằng cách giữ một kết nối luôn mở (Full-duplex), cho phép Server chủ động đẩy dữ liệu xuống Client mà không cần đợi yêu cầu.

### 2. Minh họa Code Client-side
```javascript
const chatSocket = new WebSocket('ws://[chat.example.com/v1](https://chat.example.com/v1)');

chatSocket.onopen = (e) => {
    console.log("[open] Kết nối đã thiết lập thành công");
    chatSocket.send("User 01 đã gia nhập phòng chat");
};

chatSocket.onmessage = (event) => {
    let message = event.data;
    console.log(`[message] Tin nhắn mới từ server: ${message}`);
};

chatSocket.onerror = (error) => {
    console.log(`[error] Lỗi: ${error.message}`);
};