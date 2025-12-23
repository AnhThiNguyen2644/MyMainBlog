---
title: "Lập trình truyền file qua Socket trong Java"
date: 2025-12-19
draft: false
---

### 1. Nguyên lý truyền file
Để truyền file, chúng ta chuyển file thành mảng các byte (byte array), sau đó gửi mảng byte này qua luồng xuất (`OutputStream`) của Socket.

### 2. Code ví dụ gửi file (Client)
```java
FileInputStream fis = new FileInputStream("anh_cua_toi.jpg");
OutputStream os = socket.getOutputStream();

byte[] buffer = new byte[4096];
int bytesRead;
while ((bytesRead = fis.read(buffer)) != -1) {
    os.write(buffer, 0, bytesRead);
}
System.out.println("Gửi file thành công!");