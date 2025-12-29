---
title: " Lập trình Socket TCP cơ bản với Java"
date: 2025-12-19
draft: false
cover:
    image: "/anh1.jpg"  # Đường dẫn ảnh trong thư mục static
    alt: "Mô hình kết nối TCP" # Chữ hiện ra nếu ảnh lỗi
    caption: "Mô hình Client-Server cơ bản" # Chú thích nhỏ dưới ảnh
    relative: false # Để false để dùng đường dẫn tuyệt đối từ static
tags: ["Java", "Lập trình mạng", "Socket"]
---

### 1. Khái niệm TCP Socket
TCP (Transmission Control Protocol) là giao thức hướng kết nối, đảm bảo dữ liệu được truyền đến đúng nơi và đúng thứ tự. Trong Java, chúng ta sử dụng hai lớp chính:
- `ServerSocket`: Dùng cho phía Server để lắng nghe kết nối.
- `Socket`: Dùng cho phía Client để kết nối tới Server.

### 2. Code ví dụ Server đơn giản
```java
import java.io.*;
import java.net.*;

public class MyServer {
    public static void main(String[] args) throws IOException {
        ServerSocket server = new ServerSocket(5000);
        System.out.println("Server đang đợi kết nối tại cổng 5000...");
        
        Socket socket = server.accept(); // Chấp nhận kết nối từ Client
        System.out.println("Client đã kết nối thành công!");
        
        server.close();
    }
}

Trong thực tế, TCP được ví như một cuộc gọi điện thoại (phải nhấc máy mới nói chuyện được), còn UDP như việc gửi thư (cứ gửi đi mà không chắc người nhận có đọc được không). Khi lập trình, lỗi thường gặp nhất là BindException (do cổng Port đã bị ứng dụng khác chiếm dụng) hoặc ConnectException (do Server chưa chạy).