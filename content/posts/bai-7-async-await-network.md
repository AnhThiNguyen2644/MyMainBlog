---
title: "Xử lý bất đồng bộ với Async/Await trong JS"
date: 2025-12-19
draft: false
cover:
    image: "/bai7.webp"  # Đường dẫn ảnh trong thư mục static
    alt: "Mô hình kết nối TCP" # Chữ hiện ra nếu ảnh lỗi
    caption: "Mô hình Client-Server cơ bản" # Chú thích nhỏ dưới ảnh
    relative: false # Để false để dùng đường dẫn tuyệt đối từ static
---

### 1. Tại sao cần Async/Await?
Khi gọi dữ liệu từ mạng, chúng ta không biết khi nào dữ liệu mới về. Thay vì làm trình duyệt bị "treo", chúng ta dùng `async/await` để đợi dữ liệu một cách mượt mà.

### 2. Ví dụ thực tế
```javascript
async function getNetworkData() {
    try {
        let response = await fetch('[https://api.github.com/users/octocat](https://api.github.com/users/octocat)');
        let data = await response.json();
        console.log("Dữ liệu từ GitHub:", data);
    } catch (error) {
        console.error("Lỗi kết nối mạng:", error);
    }
}
getNetworkData();

Khi làm việc với mạng, dữ liệu trả về đôi khi không đúng định dạng. Việc sử dụng try...catch kết hợp với response.ok là bắt buộc để kiểm tra mã trạng thái HTTP (như 404 - không tìm thấy, 500 - lỗi server) trước khi tiến hành xử lý dữ liệu tiếp theo.