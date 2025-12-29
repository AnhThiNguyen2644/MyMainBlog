---
title: "Trang chủ"
layout: "index"
---

<style>
    /* Container chính: Giới hạn chiều rộng để chữ không bị bè ra 2 bên màn hình */
    .home-container {
        max-width: 800px;
        margin: 0 auto;
        padding: 0 10px;
        font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    }

    /* Header: Avatar và Tên */
    .hero-section {
        text-align: center;
        padding: 40px 0;
        border-bottom: 1px dashed var(--border); /* Đường kẻ mờ ngăn cách */
        margin-bottom: 30px;
    }

    .hero-avatar {
        width: 140px;
        height: 140px;
        border-radius: 50%;
        object-fit: cover;
        border: 4px solid var(--entry); /* Viền tiệp màu nền */
        box-shadow: 0 0 20px rgba(255, 255, 255, 0.1); /* Hiệu ứng tỏa sáng nhẹ */
        margin-bottom: 15px;
        transition: transform 0.3s;
    }
    
    .hero-avatar:hover {
        transform: scale(1.05); /* Phóng to nhẹ khi rê chuột */
    }

    .hero-name {
        font-size: 28px;
        font-weight: 800;
        margin-bottom: 10px;
        letter-spacing: 1px;
    }

    /* Slogan nghệ thuật */
    .hero-slogan {
        font-family: 'Times New Roman', serif;
        font-size: 22px;
        font-style: italic;
        color: #f1c40f; /* Màu vàng Gold sang trọng */
        margin: 0;
        line-height: 1.5;
        opacity: 0.9;
    }

    /* Phần nội dung tâm sự */
    .story-section h3 {
        display: flex;
        align-items: center;
        gap: 10px;
        font-size: 22px;
        color: var(--primary);
        margin-bottom: 15px;
        border-left: 4px solid #f1c40f; /* Điểm nhấn bên trái tiêu đề */
        padding-left: 10px;
    }

    .story-content {
        font-size: 16px;
        line-height: 1.8; /* Dãn dòng cho dễ đọc */
        color: var(--secondary);
        text-align: justify; /* Căn đều 2 bên cho đẹp */
        margin-bottom: 30px;
    }

    /* Nút bấm xem bài viết */
    .btn-read-more {
        display: inline-block;
        background-color: var(--primary);
        color: var(--theme);
        padding: 10px 20px;
        border-radius: 25px;
        text-decoration: none;
        font-weight: bold;
        transition: opacity 0.3s;
        margin-top: 10px;
    }
    .btn-read-more:hover {
        opacity: 0.8;
    }

    /* Phần định hướng (Cards) */
    .future-grid {
        display: flex;
        flex-wrap: wrap;
        gap: 20px;
        margin-top: 20px;
    }

    .future-card {
        flex: 1;
        min-width: 250px;
        background-color: var(--entry);
        padding: 20px;
        border-radius: 12px;
        border: 1px solid var(--border);
        box-shadow: 0 4px 6px rgba(0,0,0,0.05);
        transition: transform 0.2s ease-in-out;
    }
    
    .future-card:hover {
        transform: translateY(-5px); /* Bay lên nhẹ khi rê chuột */
        border-color: #f1c40f;
    }

    .card-icon {
        font-size: 30px;
        margin-bottom: 10px;
        display: block;
    }
</style>

<div class="home-container">

<div class="hero-section">
    <img src="/MyMainBlog/avatar1.jpg" alt="Avatar Nguyễn Quỳnh Anh Thi" class="hero-avatar">
    
<div class="hero-name">Nguyễn Quỳnh Anh Thi 👋</div>

<p class="hero-slogan">
    "Từ kiến thức đến tương lai - Nơi chia sẻ đam mê Lập trình mạng & Hệ thống."
</p>
</div>

<div class="story-section">
<h3>☕ Đôi lời tâm sự</h3>
<div class="story-content">
<p>
Chào bạn, rất vui vì bạn đã ghé thăm "ngôi nhà số" của mình. Mình là <strong>Thi</strong>, một sinh viên IT tại HUTECH nhưng có tâm hồn hơi... "nghệ sĩ" một chút. Ngoài việc gõ code và cấu hình server, mình còn thích mày mò về thiết kế và xây dựng những thứ hay ho.
</p>
<p>
Blog này ban đầu chỉ là nơi để nộp đồ án, nhưng dần dần mình muốn biến nó thành nơi lưu lại hành trình trưởng thành của mình. Ở đây không chỉ có code khô khan đâu, mà còn có những câu chuyện về những đêm "thức trắng" fix bug, những lần build server thất bại, và cả những niềm vui nhỏ bé khi hệ thống chạy mượt mà.
</p>
<p style="text-align: center; margin-top: 20px;">
Nếu bạn đang tìm tài liệu học tập hay muốn đọc giải trí về đời sinh viên IT:<br>
<a href="/MyMainBlog/posts/" class="btn-read-more">📖 Xem Danh sách Bài viết</a>
</p>
</div>
</div>

<div class="story-section">
<h3>🔥 Định hướng sắp tới</h3>
<div class="future-grid">

<div class="future-card">
<span class="card-icon">☁️</span>
<strong>Cloud Computing</strong>
<p style="font-size: 14px; opacity: 0.8; margin-top: 5px;">
    Chinh phục chứng chỉ AWS và xây dựng hệ thống Scalable.
</p>
</div>

<div class="future-card">
<span class="card-icon">♾️</span>
<strong>DevOps & SysAdmin</strong>
<p style="font-size: 14px; opacity: 0.8; margin-top: 5px;">
    Tự động hóa mọi thứ với CI/CD Pipeline & Automation.
</p>
</div>

</div>
</div>

</div>