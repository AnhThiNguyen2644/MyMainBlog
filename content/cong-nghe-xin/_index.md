---
title: "Công Nghệ Xịn"
date: 2025-12-25
draft: false
layout: "list" 
---

<style>
    .tech-container {
        display: flex;
        flex-wrap: wrap;
        gap: 20px;
        justify-content: center;
        margin-top: 30px;
    }
    .tech-card {
        flex: 1;
        min-width: 280px;
        max-width: 350px;
        background: var(--entry);
        border: 1px solid var(--border);
        border-radius: 12px;
        overflow: hidden;
        transition: transform 0.3s ease;
    }
    .tech-card:hover {
        transform: translateY(-5px);
        box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        border-color: var(--primary);
    }
    .tech-img-box {
        width: 100%;
        height: 160px;
        background: #f5f5f5;
        display: flex;
        align-items: center;
        justify-content: center;
        border-bottom: 1px solid var(--border);
        padding: 20px;
    }
    .tech-img {
        max-width: 100%;
        max-height: 100%;
        object-fit: contain;
    }
    .tech-content { padding: 20px; }
    .tech-title { font-size: 20px; font-weight: bold; color: var(--primary); margin-bottom: 10px; }
    .tech-desc { font-size: 15px; opacity: 0.9; line-height: 1.6; }
</style>

<div style="text-align: center; max-width: 700px; margin: 0 auto 40px auto;">
    <p style="opacity: 0.8;">Các công nghệ và công cụ đắc lực hỗ trợ tôi trong quá trình học tập.</p>
</div>

<div class="tech-container">

<div class="tech-card">
    <div class="tech-img-box">
        <img src="/MyMainBlog/images/vscode.png" alt="VS Code" class="tech-img">
    </div>
    <div class="tech-content">
        <div class="tech-title">Visual Studio Code</div>
        <div class="tech-desc">Trình soạn thảo code mạnh mẽ với kho extension khổng lồ.</div>
    </div>
</div>

<div class="tech-card">
    <div class="tech-img-box">
        <img src="/MyMainBlog/images/github.png" alt="Github" class="tech-img">
    </div>
    <div class="tech-content">
        <div class="tech-title">GitHub & Git</div>
        <div class="tech-desc">Quản lý mã nguồn, làm việc nhóm và CI/CD tự động hóa.</div>
    </div>
</div>

<div class="tech-card">
    <div class="tech-img-box">
        <img src="/MyMainBlog/images/hugo.png" alt="Hugo" class="tech-img">
    </div>
    <div class="tech-content">
        <div class="tech-title">Hugo Framework</div>
        <div class="tech-desc">Nền tảng xây dựng web tĩnh siêu tốc độ.</div>
    </div>
</div>

</div>