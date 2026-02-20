<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Zinvera – README Preview</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #ffffff;
    --surface: #f7f7f7;
    --border: #e8e8e8;
    --text: #111111;
    --muted: #777777;
    --accent: #111111;
    --tag-bg: #f0f0f0;
  }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--bg);
    color: var(--text);
    max-width: 760px;
    margin: 0 auto;
    padding: 60px 32px;
    line-height: 1.7;
    font-size: 15px;
  }

  /* ── HEADER ── */
  .header {
    text-align: center;
    padding-bottom: 48px;
    border-bottom: 1px solid var(--border);
    margin-bottom: 48px;
  }

  .header h1 {
    font-size: 2.6rem;
    font-weight: 600;
    letter-spacing: -0.03em;
    margin-bottom: 10px;
  }

  .header .subtitle {
    color: var(--muted);
    font-size: 0.95rem;
    font-weight: 300;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    margin-bottom: 24px;
  }

  .links {
    display: flex;
    justify-content: center;
    gap: 12px;
    flex-wrap: wrap;
  }

  .link-pill {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    padding: 7px 16px;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 99px;
    font-size: 0.82rem;
    font-family: 'DM Mono', monospace;
    color: var(--text);
    text-decoration: none;
    transition: background 0.15s, border-color 0.15s;
  }
  .link-pill:hover { background: #ebebeb; border-color: #ccc; }
  .link-pill svg { width: 13px; height: 13px; flex-shrink: 0; }

  /* ── SECTION ── */
  .section {
    margin-bottom: 48px;
  }

  .section-label {
    font-size: 0.7rem;
    font-family: 'DM Mono', monospace;
    text-transform: uppercase;
    letter-spacing: 0.14em;
    color: var(--muted);
    margin-bottom: 16px;
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  .about-text {
    color: #333;
    font-weight: 300;
    font-size: 0.97rem;
    max-width: 600px;
    margin: 0 auto;
    text-align: center;
    line-height: 1.8;
  }

  /* ── STACK ── */
  .stack-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
  }

  .stack-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 18px 20px;
  }

  .stack-card h4 {
    font-size: 0.7rem;
    font-family: 'DM Mono', monospace;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 12px;
  }

  .badge-row {
    display: flex;
    flex-wrap: wrap;
    gap: 7px;
  }

  .badge {
    display: inline-flex;
    align-items: center;
    gap: 5px;
    padding: 4px 10px;
    background: #fff;
    border: 1px solid var(--border);
    border-radius: 6px;
    font-size: 0.78rem;
    font-family: 'DM Mono', monospace;
    color: var(--text);
    white-space: nowrap;
  }
  .badge-dot {
    width: 7px;
    height: 7px;
    border-radius: 50%;
    flex-shrink: 0;
  }

  /* ── PROJECTS ── */
  .project-list {
    display: flex;
    flex-direction: column;
    gap: 12px;
  }

  .project-card {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 16px 20px;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    gap: 16px;
    flex-wrap: wrap;
  }

  .project-info h4 {
    font-size: 0.9rem;
    font-weight: 500;
    margin-bottom: 3px;
  }
  .project-info p {
    font-size: 0.8rem;
    color: var(--muted);
    font-weight: 300;
  }

  .project-tags {
    display: flex;
    gap: 6px;
    flex-wrap: wrap;
    justify-content: flex-end;
  }
  .tag {
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    padding: 3px 9px;
    background: #fff;
    border: 1px solid var(--border);
    border-radius: 5px;
    color: #555;
    white-space: nowrap;
  }

  /* ── FOCUS ── */
  .focus-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }

  .focus-item {
    display: flex;
    align-items: flex-start;
    gap: 12px;
    padding: 14px 16px;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    font-size: 0.85rem;
    color: #333;
    font-weight: 300;
  }
  .focus-item strong { color: #111; font-weight: 500; }
  .focus-num {
    font-family: 'DM Mono', monospace;
    font-size: 0.68rem;
    color: var(--muted);
    margin-top: 3px;
    flex-shrink: 0;
  }

  /* ── ACTIVITY ── */
  .activity-wrap {
    display: flex;
    gap: 16px;
    justify-content: center;
    flex-wrap: wrap;
  }
  .activity-wrap img {
    border-radius: 10px;
    border: 1px solid var(--border);
    height: 150px;
  }

  /* ── FOOTER ── */
  .footer {
    text-align: center;
    padding-top: 32px;
    border-top: 1px solid var(--border);
    margin-top: 12px;
    font-size: 0.75rem;
    font-family: 'DM Mono', monospace;
    color: #bbb;
  }
</style>
</head>
<body>

<!-- HEADER -->
<div class="header">
  <h1>Zinvera</h1>
  <p class="subtitle">Full-Stack Developer · System Architecture · Germany</p>
  <div class="links">
    <a class="link-pill" href="mailto:zinverazin@gmail.com">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="M2 7l10 7 10-7"/></svg>
      zinverazin@gmail.com
    </a>
    <a class="link-pill" href="https://github.com/zinvera">
      <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z"/></svg>
      github/zinvera
    </a>
  </div>
</div>

<!-- ABOUT -->
<div class="section">
  <div class="section-label">About</div>
  <p class="about-text">
    Passionate Full-Stack Developer based in Germany. My focus lies in building scalable web applications, optimizing backend performance, and maintaining clean architecture. I prefer strong typing and modular design over hype-driven development.
  </p>
</div>

<!-- STACK -->
<div class="section">
  <div class="section-label">Stack</div>
  <div class="stack-grid">
    <div class="stack-card">
      <h4>Languages</h4>
      <div class="badge-row">
        <span class="badge"><span class="badge-dot" style="background:#3178C6"></span>TypeScript</span>
        <span class="badge"><span class="badge-dot" style="background:#3776AB"></span>Python</span>
      </div>
    </div>
    <div class="stack-card">
      <h4>Frontend</h4>
      <div class="badge-row">
        <span class="badge"><span class="badge-dot" style="background:#61DAFB"></span>React</span>
        <span class="badge"><span class="badge-dot" style="background:#000"></span>Next.js</span>
        <span class="badge"><span class="badge-dot" style="background:#26A69A"></span>i18next</span>
      </div>
    </div>
    <div class="stack-card">
      <h4>Backend & ORM</h4>
      <div class="badge-row">
        <span class="badge"><span class="badge-dot" style="background:#339933"></span>Node.js</span>
        <span class="badge"><span class="badge-dot" style="background:#2D3748"></span>Prisma</span>
        <span class="badge"><span class="badge-dot" style="background:#3ECF8E"></span>Supabase</span>
      </div>
    </div>
    <div class="stack-card">
      <h4>Data & Infra</h4>
      <div class="badge-row">
        <span class="badge"><span class="badge-dot" style="background:#4169E1"></span>PostgreSQL</span>
        <span class="badge"><span class="badge-dot" style="background:#003545"></span>MariaDB</span>
        <span class="badge"><span class="badge-dot" style="background:#2496ED"></span>Docker</span>
      </div>
    </div>
  </div>
</div>

<!-- PROJECTS -->
<div class="section">
  <div class="section-label">Projects</div>
  <div class="project-list">
    <div class="project-card">
      <div class="project-info">
        <h4>SaaS Boilerplate</h4>
        <p>Multi-tenant production starter kit with i18n support</p>
      </div>
      <div class="project-tags">
        <span class="tag">Next.js</span>
        <span class="tag">Prisma</span>
        <span class="tag">MariaDB</span>
      </div>
    </div>
    <div class="project-card">
      <div class="project-info">
        <h4>API Gateway</h4>
        <p>Middleware for rate-limiting and caching</p>
      </div>
      <div class="project-tags">
        <span class="tag">TypeScript</span>
        <span class="tag">Express</span>
        <span class="tag">Redis</span>
      </div>
    </div>
    <div class="project-card">
      <div class="project-info">
        <h4>Inventory System</h4>
        <p>Internal tool for asset management and tracking</p>
      </div>
      <div class="project-tags">
        <span class="tag">PostgreSQL</span>
        <span class="tag">React</span>
        <span class="tag">Docker</span>
      </div>
    </div>
  </div>
</div>

<!-- CURRENT FOCUS -->
<div class="section">
  <div class="section-label">Current Focus</div>
  <div class="focus-grid">
    <div class="focus-item">
      <span class="focus-num">01</span>
      <span><strong>Architecting</strong> scalable backend systems using Node.js, Prisma, and SQL</span>
    </div>
    <div class="focus-item">
      <span class="focus-num">02</span>
      <span><strong>Developing</strong> responsive, internationalized interfaces with React</span>
    </div>
    <div class="focus-item">
      <span class="focus-num">03</span>
      <span><strong>Optimizing</strong> database queries and studying system design patterns</span>
    </div>
    <div class="focus-item">
      <span class="focus-num">04</span>
      <span><strong>Open Source</strong> contributions and code reviews</span>
    </div>
  </div>
</div>

<!-- ACTIVITY -->
<div class="section">
  <div class="section-label">Activity</div>
  <div class="activity-wrap">
    <img src="https://github-readme-stats.vercel.app/api?username=zinvera&show_icons=true&theme=default&hide_border=true&title_color=000000&text_color=333333&icon_color=000000&cache_seconds=86400" alt="stats" />
    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=zinvera&layout=compact&theme=default&hide_border=true&title_color=000000&text_color=333333&cache_seconds=86400" alt="languages" />
  </div>
</div>

<!-- FOOTER -->
<div class="footer">
  zinvera · github.com/zinvera
</div>

</body>
</html>
