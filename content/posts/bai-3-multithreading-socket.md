---
title: " Xử lý đa luồng (Multithreading) trong Server"
date: 2025-12-19
draft: false
cover:
    image: "/anh3.png"  # Đường dẫn ảnh trong thư mục static
    alt: "Mô hình kết nối TCP" # Chữ hiện ra nếu ảnh lỗi
    caption: "Mô hình Client-Server cơ bản" # Chú thích nhỏ dưới ảnh
    relative: false # Để false để dùng đường dẫn tuyệt đối từ static
---

### 1. Tại sao Server cần Đa luồng?
Trong lập trình mạng, nếu Server chỉ chạy đơn luồng, nó sẽ bị "nghẽn" (blocking). Khi một Client đang kết nối và gửi dữ liệu, các Client khác muốn kết nối vào sẽ phải xếp hàng đợi. 

Để giải quyết vấn đề này, chúng ta sử dụng **Multithreading** để mỗi khi có một khách hàng mới, Server sẽ cử ra một "người phục vụ" (Thread) riêng cho khách hàng đó.

### 2. Cấu trúc mã nguồn Server đa luồng (Java)

Dưới đây là cách triển khai một Server có thể phục vụ nhiều người cùng lúc:

```java
import java.io.*;
import java.net.*;

public class MultiThreadedServer {
    public static void main(String[] args) {
        try (ServerSocket serverSocket = new ServerSocket(8888)) {
            System.out.println("Server đa luồng đang chạy tại cổng 8888...");

            while (true) {
                Socket socket = serverSocket.accept();
                System.out.println("Có Client mới kết nối: " + socket.getInetAddress());

                // Tạo một Thread mới cho mỗi Client
                new Thread(new ClientHandler(socket)).start();
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}

// Lớp xử lý riêng cho từng Client
class ClientHandler implements Runnable {
    private Socket socket;

    public ClientHandler(Socket socket) {
        this.socket = socket;
    }

    @Override
    public void run() {
        try {
            // Xử lý đọc/ghi dữ liệu ở đây
            System.out.println("Đang xử lý Client trong luồng: " + Thread.currentThread().getName());
            socket.close();
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}

Thay vì tạo Thread mới liên tục gây tốn tài nguyên (overhead), các hệ thống lớn thường dùng ExecutorService. Điều này giúp kiểm soát số lượng luồng tối đa chạy cùng lúc, tránh việc máy chủ bị treo do quá tải CPU khi có hàng nghìn Client truy cập đồng thời.