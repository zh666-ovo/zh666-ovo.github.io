---
layout: default
title: Home
---

<section class="hero">
    <div class="hero-tag">
        <span class="status-dot"></span>
        MY LEARNING JOURNEY
    </div>

    <h1>
        Explore the World of<br>
        <span class="gradient-text">Computer Science.</span>
    </h1>

    <p class="hero-description">
        记录技术学习、代码实践与思考。
        从底层系统到人工智能，不断探索计算机科学的世界。
    </p>

    <div class="hero-buttons">
        <a href="#articles" class="btn-primary">阅读文章 ↗</a>
        <a href="#categories" class="btn-secondary">探索分类</a>
    </div>

    <div class="hero-decoration">01 / LEARN · BUILD · EXPLORE</div>
</section>

<section id="categories" class="section">
    <div class="section-heading">
        <div>
            <span class="section-label">KNOWLEDGE AREAS</span>
            <h2>学习领域</h2>
        </div>
        <span class="section-number">01 — 04</span>
    </div>

    <div class="category-grid">

        <a href="#articles" class="category-card">
            <span class="category-icon">⌘</span>
            <h3>Operating Systems</h3>
            <p>操作系统、进程管理、内存与并发</p>
            <span class="card-arrow">↗</span>
        </a>

        <a href="#articles" class="category-card">
            <span class="category-icon">⌁</span>
            <h3>Computer Networks</h3>
            <p>TCP/IP、路由算法、网络协议</p>
            <span class="card-arrow">↗</span>
        </a>

        <a href="#articles" class="category-card">
            <span class="category-icon">◈</span>
            <h3>Deep Learning</h3>
            <p>CNN、神经网络与机器学习</p>
            <span class="card-arrow">↗</span>
        </a>

        <a href="#articles" class="category-card">
            <span class="category-icon">⌘</span>
            <h3>Development</h3>
            <p>C++、Python 与工程实践</p>
            <span class="card-arrow">↗</span>
        </a>

    </div>
</section>

<section id="articles" class="section">
    <div class="section-heading">
        <div>
            <span class="section-label">LATEST WRITINGS</span>
            <h2>最近的文章</h2>
        </div>
        <span class="section-number">
            {{ site.posts.size }} ARTICLES
        </span>
    </div>

    <div class="article-list">
        {% for post in site.posts %}
        <a class="article-card" href="{{ post.url | relative_url }}">
            <div class="article-card-main">
                <span class="article-card-category">
                    {{ post.categories | join: " / " | default: "TECH NOTES" }}
                </span>
                <h3>{{ post.title }}</h3>
                <p>
                    {{ post.excerpt | strip_html | truncate: 110 }}
                </p>
            </div>

            <div class="article-card-meta">
                <time>{{ post.date | date: "%Y-%m-%d" }}</time>
                <span class="article-arrow">↗</span>
            </div>
        </a>
        {% endfor %}
    </div>
</section>
