---
title: "Giao thức UDP trong lập trình mạng Java"
date: 2025-12-19
draft: false
cover:
    image: "/anh2.webp"  # Đường dẫn ảnh trong thư mục static
    alt: "Mô hình kết nối TCP" # Chữ hiện ra nếu ảnh lỗi
    caption: "Mô hình Client-Server cơ bản" # Chú thích nhỏ dưới ảnh
    relative: false # Để false để dùng đường dẫn tuyệt đối từ static
---

### 1. Tại sao dùng UDP?
Khác với TCP, UDP (User Datagram Protocol) không cần thiết lập kết nối. Nó gửi các "gói tin" (Datagram) đi một cách nhanh chóng. Phù hợp cho các ứng dụng như Livestream hoặc Game online.

### 2. Code ví dụ gửi gói tin UDP
```java
import java.net.*;

public class UDPSender {
    public static void main(String[] args) throws Exception {
        DatagramSocket socket = new DatagramSocket();
        String message = "Xin chào từ UDP Client!";
        byte[] data = message.getBytes();
        
        InetAddress address = InetAddress.getByName("localhost");
        DatagramPacket packet = new DatagramPacket(data, data.length, address, 5001);
        
        socket.send(packet);
        System.out.println("Đã gửi gói tin UDP.");
        socket.close();
    }
}

Trong thực tế, TCP được ví như một cuộc gọi điện thoại (phải nhấc máy mới nói chuyện được), còn UDP như việc gửi thư (cứ gửi đi mà không chắc người nhận có đọc được không). Khi lập trình, lỗi thường gặp nhất là BindException (do cổng Port đã bị ứng dụng khác chiếm dụng) hoặc ConnectException (do Server chưa chạy).