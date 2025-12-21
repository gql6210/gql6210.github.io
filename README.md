<!doctype html>
<html lang="zh-CN">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>gql6210 — 个人主页</title>
  <meta name="description" content="gql6210 的个人主页 — 项目、博客与联系信息" />
  <link rel="stylesheet" href="assets/styles.css">
  <link rel="icon" href="data:;base64,iVBORw0KGgo=">
  <meta name="theme-color" content="#0f172a">
  <!-- Open Graph -->
  <meta property="og:title" content="gql6210 — 个人主页">
  <meta property="og:description" content="gql6210 的个人主页 — 项目、博客与联系信息">
  <meta property="og:type" content="website">
</head>
<body>
  <header class="site-header">
    <div class="container header-inner">
      <div class="brand">
        <!-- 简易头像 SVG 占位，可替换为 <img src="..."> -->
        <div class="avatar" aria-hidden="true">
          <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
            <rect width="100" height="100" rx="18" fill="#334155"/>
            <text x="50" y="58" font-size="42" fill="#fff" text-anchor="middle" font-family="sans-serif">G</text>
          </svg>
        </div>
        <div>
          <h1 class="name">gql6210</h1>
          <p class="tagline">工程师 · 开源爱好者 · 喜欢构建简单可靠的工具</p>
        </div>
      </div>

      <nav class="top-nav" aria-label="主导航">
        <a href="#projects">项目</a>
        <a href="#about">关于</a>
        <a href="#contact">联系</a>
        <button id="theme-toggle" class="btn-ghost" aria-label="切换主题">🌗</button>
      </nav>
    </div>
  </header>

  <main class="container">
    <section class="hero">
      <h2>你好，我是 <span class="accent">gql6210</span></h2>
      <p class="lead">这里是我的个人主页 —— 放置项目、博客、和联系信息的地方。</p>
      <p class="hero-actions">
        <a class="btn" href="#projects">查看项目</a>
        <a class="btn btn-ghost" href="#contact">联系我</a>
      </p>
    </section>

    <section id="projects" class="section">
      <h3>项目</h3>
      <div class="cards">
        <article class="card">
          <h4><a href="https://github.com/gql6210/example-project" target="_blank" rel="noopener">示例项目 A</a></h4>
          <p>一个用来展示项目模块化与 CI 配置的示例仓库。</p>
          <p class="meta">技术栈：JavaScript · Node · GitHub Actions</p>
        </article>

        <article class="card">
          <h4><a href="#" target="_blank" rel="noopener">示例项目 B</a></h4>
          <p>演示静态站与自动部署流程的轻量项目。</p>
          <p class="meta">技术栈：HTML · CSS · GitHub Pages</p>
        </article>
      </div>
      <p class="more"><a href="https://github.com/gql6210" target="_blank" rel="noopener">在 GitHub 上查看更多 →</a></p>
    </section>

    <section id="about" class="section">
      <h3>关于我</h3>
      <div class="two-col">
        <div>
          <p>我叫 gql6210，关注后端服务、工具链与自动化工作流。喜欢以简单可维护的方式解决问题。</p>
          <ul class="skills">
            <li>语言：JavaScript / TypeScript / Python</li>
            <li>工具：Docker · GitHub Actions · Linux</li>
            <li>兴趣：开源、性能优化、工程化</li>
          </ul>
        </div>
        <aside class="card small">
          <h4>状态</h4>
          <p>可接短期 freelance 与开源协作</p>
          <p class="meta">当前位置：线上 · 时区：你所在时区</p>
        </aside>
      </div>
    </section>

    <section id="contact" class="section">
      <h3>联系</h3>
      <p>欢迎通过下面方式联系我：</p>
      <ul class="contact-list">
        <li>邮箱：<a href="mailto:your-email@example.com">your-email@example.com</a>（请替换为你的邮箱）</li>
        <li>GitHub：<a href="https://github.com/gql6210" target="_blank" rel="noopener">github.com/gql6210</a></li>
        <li>Telegram / Twitter / LinkedIn：在此处加入你的社交链接</li>
      </ul>
      <p>或使用下面的快捷链接：</p>
      <p><a class="btn" href="mailto:your-email@example.com">发送邮件</a></p>
    </section>
  </main>

  <footer class="site-footer">
    <div class="container footer-inner">
      <p>© <span id="year"></span> gql6210 — 基于静态模板构建</p>
      <p class="small"><a href="https://docs.github.com/en/pages" target="_blank" rel="noopener">如何部署到 GitHub Pages</a></p>
    </div>
  </footer>

  <script src="assets/script.js" type="module"></script>
</body>
</html>
