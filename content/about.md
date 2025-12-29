---
title: "Giới thiệu bản thân"
layout: "about"
date: 2025-12-19
draft: false
summary: "profile"
---

<style>
    /* Khung bao ngoài */
    .about-container {
        max-width: 800px;
        margin: 0 auto;
        font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    }

    /* Avatar đẹp */
    .about-header {
        text-align: center;
        margin-bottom: 40px;
    }
    .about-avatar {
        width: 160px;
        height: 160px;
        border-radius: 50%;
        object-fit: cover;
        border: 4px solid var(--entry);
        box-shadow: 0 8px 20px rgba(0,0,0,0.15); /* Bóng đổ sâu hơn */
        transition: transform 0.3s ease;
    }
    .about-avatar:hover {
        transform: rotate(5deg) scale(1.05); /* Hiệu ứng nghiêng nhẹ khi rê chuột */
    }

    /* Bảng thông tin cá nhân */
    .profile-table {
        width: 100%;
        border-collapse: collapse;
        margin-bottom: 30px;
        background-color: var(--entry);
        border-radius: 10px;
        overflow: hidden; /* Bo tròn góc bảng */
        box-shadow: 0 2px 5px rgba(0,0,0,0.05);
    }
    .profile-table td {
        padding: 12px 20px;
        border-bottom: 1px solid var(--border);
    }
    .profile-table tr:last-child td {
        border-bottom: none;
    }
    .profile-label {
        font-weight: bold;
        color: var(--primary);
        width: 35%;
    }

    /* Các khối nội dung (Mục tiêu, Cột mốc) */
    .content-box {
        margin-bottom: 40px;
    }
    .section-title {
        font-size: 22px;
        font-weight: bold;
        margin-bottom: 15px;
        display: flex;
        align-items: center;
        gap: 10px;
        color: var(--primary);
        border-bottom: 2px solid var(--border);
        padding-bottom: 10px;
    }
    
    /* Danh sách cột mốc */
    .milestone-list {
        list-style: none;
        padding: 0;
    }
    .milestone-item {
        position: relative;
        padding-left: 25px;
        margin-bottom: 10px;
    }
    .milestone-item::before {
        content: "✔️"; /* Dấu tích đẹp hơn dấu chấm tròn */
        position: absolute;
        left: 0;
        top: 2px;
        font-size: 14px;
    }

    /* Gallery chứng chỉ */
    .cert-grid {
        display: flex;
        flex-wrap: wrap;
        gap: 15px;
        justify-content: center;
    }
    .cert-item {
        flex: 1;
        min-width: 200px;
        max-width: 30%;
        transition: transform 0.3s;
    }
    .cert-item:hover {
        transform: translateY(-5px);
        z-index: 10;
    }
    .cert-img {
        width: 100%;
        height: auto;
        border-radius: 8px;
        border: 1px solid var(--border);
        box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        cursor: zoom-in;
    }

    /* Định hướng (Card style) - Giữ nguyên style đẹp cũ */
    .future-grid {
        display: flex;
        flex-wrap: wrap;
        gap: 20px;
    }
    .future-card {
        flex: 1;
        min-width: 250px;
        background-color: var(--entry);
        padding: 20px;
        border-radius: 12px;
        border: 1px solid var(--border);
        box-shadow: 0 4px 6px rgba(0,0,0,0.05);
        transition: transform 0.2s;
    }
    .future-card:hover {
        transform: translateY(-5px);
        border-color: var(--primary);
    }
</style>

<div class="about-container">

<div class="about-header">
    <img src="/Bloglaptrinh/avatar1.jpg" alt="Avatar Nguyễn Quỳnh Anh Thi" class="about-avatar">
    <p style="margin-top: 20px; font-size: 16px; font-style: italic; opacity: 0.9;">
        "Chào mừng thầy và các bạn đã ghé thăm Blog cá nhân của mình. 👋"
    </p>
</div>

<div class="content-box">
    <div class="section-title">👤 Thông tin cá nhân</div>
    <table class="profile-table">
        <tr>
            <td class="profile-label">Họ và tên</td>
            <td>Nguyễn Quỳnh Anh Thi</td>
        </tr>
        <tr>
            <td class="profile-label">Mã số sinh viên</td>
            <td>2280603022</td>
        </tr>
        <tr>
            <td class="profile-label">Lớp</td>
            <td>22DTHE7</td>
        </tr>
        <tr>
            <td class="profile-label">Khoa</td>
            <td>Công nghệ Thông tin - Hệ thống Thông tin</td>
        </tr>
    </table>
</div>

<div class="content-box">
    <div class="section-title">🚀 Mục tiêu nghề nghiệp</div>
    <p style="background-color: var(--entry); padding: 15px; border-left: 4px solid var(--primary); border-radius: 4px;">
        Trở thành một <strong>Senior Information Systems Engineer</strong>, người có khả năng thiết kế và vận hành những hệ thống thông tin quy mô lớn, đảm bảo luồng dữ liệu của doanh nghiệp luôn thông suốt và bảo mật.
    </p>
</div>

<div class="content-box">
    <div class="section-title">🌟 Những cột mốc đã đạt được</div>
    <ul class="milestone-list">
        <li class="milestone-item">
            <strong>Hệ thống Quản lý Bán hàng (ERP mini):</strong> Sử dụng C# .NET và SQL Server, giúp tối ưu quy trình nhập xuất kho.
        </li>
        <li class="milestone-item">
            <strong>Website Thương mại điện tử:</strong> Xây dựng bằng Java Spring Boot, tích hợp thanh toán online.
        </li>
        <li class="milestone-item">
            <strong>Blog Công nghệ cá nhân (Dự án này):</strong> Triển khai quy trình CI/CD tự động hóa với Hugo và GitHub Pages.
        </li>
    </ul>
</div>

<div class="content-box">
    <div class="section-title">🏆 Chứng chỉ & Bằng cấp</div>
    <div class="cert-grid">
        <a href="/Bloglaptrinh/chung-chi/chungchi1.PNG" target="_blank" class="cert-item">
            <img src="/Bloglaptrinh/chung-chi/chungchi1.PNG" alt="Chứng chỉ 1" class="cert-img">
        </a>
        <a href="/Bloglaptrinh/chung-chi/chungchi2.PNG" target="_blank" class="cert-item">
            <img src="/Bloglaptrinh/chung-chi/chungchi2.PNG" alt="Chứng chỉ 2" class="cert-img">
        </a>
        <a href="/Bloglaptrinh/chung-chi/chungchi3.PNG" target="_blank" class="cert-item">
            <img src="/Bloglaptrinh/chung-chi/chungchi3.PNG" alt="Chứng chỉ 3" class="cert-img">
        </a>
    </div>
</div>

<div class="content-box">
    <div class="section-title">🔥 Định hướng tương lai</div>
    <div class="future-grid">
        <div class="future-card">
            <div style="font-size: 35px; margin-bottom: 10px;">☁️</div>
            <h4 style="margin: 0 0 10px 0; color: var(--primary);">Cloud Computing</h4>
            <p style="font-size: 14px; opacity: 0.9;">Chuyên sâu kiến trúc AWS/Azure, triển khai giải pháp Scalability.</p>
        </div>
        <div class="future-card">
            <div style="font-size: 35px; margin-bottom: 10px;">♾️</div>
            <h4 style="margin: 0 0 10px 0; color: var(--primary);">DevOps & SysAdmin</h4>
            <p style="font-size: 14px; opacity: 0.9;">Tối ưu hóa vận hành, cầu nối Dev-Ops qua CI/CD.</p>
        </div>
        <div class="future-card">
            <div style="font-size: 35px; margin-bottom: 10px;">📊</div>
            <h4 style="margin: 0 0 10px 0; color: var(--primary);">Data Analysis</h4>
            <p style="font-size: 14px; opacity: 0.9;">Phân tích dữ liệu để đưa ra quyết định chiến lược.</p>
        </div>
    </div>
</div>

<hr style="margin: 40px 0; opacity: 0.3;">
<div style="text-align: center; font-style: italic; opacity: 0.8;">
    <p>“Cảm ơn mọi người đã ghé thăm! Mọi ý kiến đóng góp xin gửi về GitHub của mình.”</p>
    <p>❤️</p>
</div>

</div>