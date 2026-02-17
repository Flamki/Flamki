<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ayush Singh — GitHub README Preview</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&family=Space+Grotesk:wght@300;400;500;600;700&display=swap');

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: #0d1117;
    color: #e6edf3;
    font-family: 'Space Grotesk', sans-serif;
    min-height: 100vh;
    padding: 40px 20px;
  }

  .readme {
    max-width: 860px;
    margin: 0 auto;
    background: #161b22;
    border: 1px solid #30363d;
    border-radius: 12px;
    overflow: hidden;
  }

  /* top bar */
  .topbar {
    background: #21262d;
    padding: 10px 16px;
    display: flex;
    align-items: center;
    gap: 8px;
    border-bottom: 1px solid #30363d;
  }
  .dot { width: 12px; height: 12px; border-radius: 50%; }
  .dot.r { background: #ff5f57; }
  .dot.y { background: #febc2e; }
  .dot.g { background: #28c840; }
  .topbar span { color: #8b949e; font-size: 12px; margin-left: 8px; font-family: 'JetBrains Mono', monospace; }

  .content { padding: 48px 56px; }

  /* hero */
  .hero { text-align: center; margin-bottom: 48px; }

  .typing-line {
    font-family: 'JetBrains Mono', monospace;
    font-size: 13px;
    color: #3fb950;
    margin-bottom: 20px;
    letter-spacing: 0.05em;
  }
  .typing-line::before { content: '> '; color: #6e7681; }

  .name {
    font-size: 52px;
    font-weight: 700;
    background: linear-gradient(135deg, #e6edf3 30%, #58a6ff 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    line-height: 1.1;
    margin-bottom: 12px;
  }

  .tagline {
    font-size: 16px;
    color: #8b949e;
    margin-bottom: 8px;
    font-weight: 400;
  }

  .flex-badge {
    display: inline-block;
    background: linear-gradient(135deg, #388bfd22, #388bfd44);
    border: 1px solid #388bfd66;
    color: #58a6ff;
    padding: 6px 16px;
    border-radius: 100px;
    font-size: 13px;
    font-weight: 600;
    margin: 16px 0 24px;
    letter-spacing: 0.02em;
  }

  .badges { display: flex; gap: 10px; justify-content: center; flex-wrap: wrap; margin-top: 16px; }
  .badge {
    padding: 8px 16px;
    border-radius: 8px;
    font-size: 12px;
    font-weight: 600;
    text-decoration: none;
    display: flex;
    align-items: center;
    gap: 6px;
    transition: transform 0.2s, opacity 0.2s;
    cursor: pointer;
  }
  .badge:hover { transform: translateY(-2px); opacity: 0.9; }
  .badge.portfolio { background: #21262d; border: 1px solid #30363d; color: #e6edf3; }
  .badge.linkedin { background: #0077b5; color: white; }
  .badge.email { background: #d14836; color: white; }
  .badge.resume { background: #238636; color: white; }

  /* divider */
  .divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, #30363d, transparent);
    margin: 40px 0;
  }

  /* section headers */
  .section-label {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    color: #3fb950;
    text-transform: uppercase;
    letter-spacing: 0.15em;
    margin-bottom: 6px;
  }

  h2 {
    font-size: 20px;
    font-weight: 700;
    color: #e6edf3;
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  /* OSS table */
  .oss-grid { display: flex; flex-direction: column; gap: 12px; }

  .oss-card {
    background: #0d1117;
    border: 1px solid #30363d;
    border-radius: 10px;
    padding: 16px 20px;
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 12px;
    align-items: center;
    transition: border-color 0.2s;
    position: relative;
    overflow: hidden;
  }
  .oss-card::before {
    content: '';
    position: absolute;
    left: 0; top: 0; bottom: 0;
    width: 3px;
  }
  .oss-card.jenkins::before { background: #f0883e; }
  .oss-card.nao::before { background: #58a6ff; }
  .oss-card.security::before { background: #3fb950; }

  .oss-card:hover { border-color: #58a6ff44; }

  .oss-org {
    font-size: 11px;
    font-family: 'JetBrains Mono', monospace;
    color: #8b949e;
    margin-bottom: 4px;
  }
  .oss-title { font-size: 14px; font-weight: 600; color: #e6edf3; margin-bottom: 4px; }
  .oss-desc { font-size: 12px; color: #8b949e; line-height: 1.5; }

  .pr-badge {
    display: inline-flex;
    align-items: center;
    gap: 5px;
    padding: 5px 12px;
    border-radius: 100px;
    font-size: 11px;
    font-weight: 700;
    white-space: nowrap;
    font-family: 'JetBrains Mono', monospace;
  }
  .pr-badge.merged { background: #6e40c922; border: 1px solid #6e40c9; color: #a371f7; }
  .pr-badge.closed { background: #da363322; border: 1px solid #da3633; color: #f85149; }
  .pr-badge .dot-s { width: 6px; height: 6px; border-radius: 50%; background: currentColor; }

  /* tech stack */
  .stack-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 10px; }
  .stack-category { background: #0d1117; border: 1px solid #30363d; border-radius: 10px; padding: 14px 16px; }
  .stack-cat-title { font-size: 11px; color: #8b949e; text-transform: uppercase; letter-spacing: 0.1em; margin-bottom: 10px; font-family: 'JetBrains Mono', monospace; }
  .stack-tags { display: flex; flex-wrap: wrap; gap: 6px; }
  .tag {
    padding: 3px 10px;
    border-radius: 100px;
    font-size: 11px;
    font-weight: 600;
    border: 1px solid;
  }
  .tag.blue { background: #388bfd11; border-color: #388bfd44; color: #58a6ff; }
  .tag.green { background: #3fb95011; border-color: #3fb95044; color: #3fb950; }
  .tag.orange { background: #f0883e11; border-color: #f0883e44; color: #f0883e; }

  /* projects */
  .project-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; }
  .project-card {
    background: #0d1117;
    border: 1px solid #30363d;
    border-radius: 10px;
    padding: 16px;
    transition: border-color 0.2s, transform 0.2s;
    cursor: pointer;
  }
  .project-card:hover { border-color: #58a6ff55; transform: translateY(-2px); }
  .project-icon { font-size: 24px; margin-bottom: 10px; }
  .project-name { font-size: 13px; font-weight: 700; color: #e6edf3; margin-bottom: 4px; }
  .project-desc { font-size: 11px; color: #8b949e; margin-bottom: 10px; line-height: 1.4; }
  .project-stack { display: flex; flex-wrap: wrap; gap: 4px; margin-bottom: 10px; }
  .project-tag { font-size: 10px; padding: 2px 7px; border-radius: 100px; background: #21262d; color: #8b949e; border: 1px solid #30363d; font-family: 'JetBrains Mono', monospace; }
  .project-link { font-size: 11px; color: #58a6ff; text-decoration: none; display: flex; align-items: center; gap: 4px; }

  /* stats row */
  .stats-row { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
  .stat-img { width: 100%; border-radius: 8px; border: 1px solid #30363d; }

  /* footer */
  .footer-center { text-align: center; }
  .footer-line { font-size: 13px; color: #8b949e; margin-bottom: 8px; }
  .footer-open { display: inline-flex; align-items: center; gap: 8px; background: #238636; color: white; padding: 8px 20px; border-radius: 100px; font-size: 13px; font-weight: 600; margin-top: 12px; }
  .green-dot { width: 8px; height: 8px; border-radius: 50%; background: #3fb950; animation: pulse 2s infinite; }
  @keyframes pulse { 0%,100%{opacity:1;transform:scale(1)} 50%{opacity:0.6;transform:scale(1.3)} }

  /* label note */
  .copy-note {
    text-align: center;
    padding: 16px;
    background: #0d1117;
    border-top: 1px solid #30363d;
    font-size: 12px;
    color: #8b949e;
    font-family: 'JetBrains Mono', monospace;
  }
</style>
</head>
<body>

<div style="text-align:center; margin-bottom: 24px;">
  <p style="color:#8b949e; font-size:13px; font-family: 'JetBrains Mono', monospace;">↓ This is a preview of how your GitHub README will look ↓</p>
</div>

<div class="readme">
  <div class="topbar">
    <div class="dot r"></div>
    <div class="dot y"></div>
    <div class="dot g"></div>
    <span>github.com/Flamki/Flamki · README.md</span>
  </div>

  <div class="content">

    <!-- HERO -->
    <div class="hero">
      <div class="typing-line">open_source_contributor && full_stack_developer</div>
      <div class="name">Ayush Singh</div>
      <div class="tagline">Building real software · Contributing to real codebases</div>
      <div class="flex-badge">⚡ Merged PRs @ Jenkins OSS &nbsp;·&nbsp; Y Combinator S24 (Nao Labs)</div>
      <div class="badges">
        <a class="badge portfolio">🌐 Portfolio</a>
        <a class="badge linkedin">in LinkedIn</a>
        <a class="badge email">✉ Email</a>
        <a class="badge resume">📄 Resume</a>
      </div>
    </div>

    <div class="divider"></div>

    <!-- OSS -->
    <div class="section-label">// open source</div>
    <h2>🔥 Merged Pull Requests</h2>
    <div class="oss-grid">

      <div class="oss-card jenkins">
        <div>
          <div class="oss-org">jenkins-infra/jenkins.io · Official CI/CD Platform</div>
          <div class="oss-title">Document hasPermission for secure form validation</div>
          <div class="oss-desc">Recommended hasPermission + FormValidation.ok() to prevent auth bypasses. Reviewed by 4 core Jenkins maintainers.</div>
        </div>
        <div class="pr-badge merged"><div class="dot-s"></div>#8831 Merged</div>
      </div>

      <div class="oss-card nao">
        <div>
          <div class="oss-org">getnao/nao · Y Combinator S24 · 500+ ⭐</div>
          <div class="oss-title">App version metadata & admin systems</div>
          <div class="oss-desc">Admin-protected tRPC route exposing version/commit/buildDate. Docker build-args wired into production Project Settings UI.</div>
        </div>
        <div class="pr-badge merged"><div class="dot-s"></div>#170 Merged</div>
      </div>

      <div class="oss-card nao">
        <div>
          <div class="oss-org">getnao/nao · Y Combinator S24</div>
          <div class="oss-title">Core infrastructure contribution</div>
          <div class="oss-desc">Improved core reliability and component architecture of the production codebase.</div>
        </div>
        <div class="pr-badge merged"><div class="dot-s"></div>#150 Merged</div>
      </div>

      <div class="oss-card security">
        <div>
          <div class="oss-org">getnao/nao · Y Combinator S24 · Security</div>
          <div class="oss-title">Path traversal vulnerability audit</div>
          <div class="oss-desc">Investigated filesystem vulnerability, confirmed mitigation via boundary checks, documented findings — preventing unnecessary remediation.</div>
        </div>
        <div class="pr-badge closed"><div class="dot-s"></div>#66 Closed</div>
      </div>

    </div>

    <div class="divider"></div>

    <!-- TECH STACK -->
    <div class="section-label">// tech stack</div>
    <h2>🛠️ What I Work With</h2>
    <div class="stack-grid">
      <div class="stack-category">
        <div class="stack-cat-title">Frontend</div>
        <div class="stack-tags">
          <span class="tag blue">React.js</span>
          <span class="tag blue">Next.js</span>
          <span class="tag blue">TypeScript</span>
          <span class="tag blue">Tailwind</span>
          <span class="tag blue">JavaScript</span>
        </div>
      </div>
      <div class="stack-category">
        <div class="stack-cat-title">Backend & DevOps</div>
        <div class="stack-tags">
          <span class="tag green">Node.js</span>
          <span class="tag green">tRPC</span>
          <span class="tag green">PostgreSQL</span>
          <span class="tag green">Docker</span>
          <span class="tag green">Linux</span>
          <span class="tag green">Git</span>
        </div>
      </div>
      <div class="stack-category">
        <div class="stack-cat-title">Data & AI</div>
        <div class="stack-tags">
          <span class="tag orange">Python</span>
          <span class="tag orange">TensorFlow</span>
          <span class="tag orange">scikit-learn</span>
          <span class="tag orange">ML</span>
        </div>
      </div>
    </div>

    <div class="divider"></div>

    <!-- PROJECTS -->
    <div class="section-label">// projects</div>
    <h2>🚀 Live Projects</h2>
    <div class="project-grid">
      <div class="project-card">
        <div class="project-icon">🏠</div>
        <div class="project-name">Vignaharta</div>
        <div class="project-desc">Full-stack real estate platform with custom Admin CMS</div>
        <div class="project-stack">
          <span class="project-tag">Next.js</span>
          <span class="project-tag">PostgreSQL</span>
          <span class="project-tag">Node.js</span>
        </div>
        <a class="project-link">↗ vignaharta.vercel.app</a>
      </div>
      <div class="project-card">
        <div class="project-icon">🎮</div>
        <div class="project-name">PokeQuest</div>
        <div class="project-desc">Pokémon discovery engine with real-time stat comparisons</div>
        <div class="project-stack">
          <span class="project-tag">React.js</span>
          <span class="project-tag">PokeAPI</span>
          <span class="project-tag">REST</span>
        </div>
        <a class="project-link">↗ pokequest-beige.vercel.app</a>
      </div>
      <div class="project-card">
        <div class="project-icon">🔊</div>
        <div class="project-name">Sonic Weaver</div>
        <div class="project-desc">3D audio simulator using Head-Related Transfer Function</div>
        <div class="project-stack">
          <span class="project-tag">Next.js</span>
          <span class="project-tag">Web Audio</span>
          <span class="project-tag">HRTF</span>
        </div>
        <a class="project-link">↗ sonic-weaver.vercel.app</a>
      </div>
    </div>

    <div class="divider"></div>

    <!-- STATS -->
    <div class="section-label">// github stats</div>
    <h2>📊 Stats</h2>
    <div class="stats-row">
      <img class="stat-img" src="https://github-readme-stats.vercel.app/api?username=flamki&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=58a6ff&icon_color=3fb950&text_color=8b949e" alt="stats">
      <img class="stat-img" src="https://github-readme-stats.vercel.app/api/top-langs/?username=flamki&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=58a6ff&text_color=8b949e" alt="langs">
    </div>

    <div class="divider"></div>

    <!-- FOOTER -->
    <div class="footer-center">
      <div class="footer-line">🎓 B.Tech IT · Data Science · DY Patil University · 2026</div>
      <div class="footer-line">9833Ayush@gmail.com · linkedin.com/in/ayush-s-singh</div>
      <div class="footer-open"><div class="green-dot"></div> Open to Remote Roles Internationally</div>
    </div>

  </div>

  <div class="copy-note">
    ↑ Preview only — copy the markdown below into your GitHub profile README ↑
  </div>
</div>

<div style="max-width:860px; margin: 40px auto; background: #161b22; border: 1px solid #30363d; border-radius: 12px; padding: 32px 40px;">
  <h3 style="color:#58a6ff; font-family:'JetBrains Mono',monospace; margin-bottom: 20px; font-size:14px;">// Copy this into your README.md</h3>
  <pre style="background:#0d1117; padding:24px; border-radius:8px; color:#8b949e; font-size:11px; font-family:'JetBrains Mono',monospace; overflow-x:auto; line-height:1.8; border: 1px solid #30363d; white-space: pre-wrap;"><code>&lt;div align="center"&gt;

&lt;img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:161b22,100:58a6ff&height=120&section=header&text=Ayush%20Singh&fontSize=40&fontColor=e6edf3&fontAlignY=65&desc=Full%20Stack%20Developer%20%C2%B7%20Open%20Source%20Contributor&descAlignY=85&descColor=8b949e" width="100%"&gt;

[![Portfolio](https://img.shields.io/badge/🌐_Portfolio-flamki--portfolio.vercel.app-0d1117?style=for-the-badge&labelColor=161b22)](https://flamki-portfolio.vercel.app/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/ayush-s-singh/)
[![Email](https://img.shields.io/badge/Email-9833Ayush@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:9833Ayush@gmail.com)

&lt;/div&gt;

---

## ⚡ Merged PRs — Real Production Codebases

| | Project | What I built | PR |
|--|--------|-------------|-----|
| 🔧 | **Jenkins** `jenkins-infra/jenkins.io` | `hasPermission + FormValidation.ok()` docs — prevents auth bypasses. Reviewed by 4 core maintainers | [#8831 ✅](https://github.com/jenkins-infra/jenkins.io/pull/8831) |
| 🚀 | **Nao Labs** `YC S24 · 500+⭐` | Admin-protected `system.version` tRPC route + Docker build-args wiring commit SHA into production UI | [#170 ✅](https://github.com/getnao/nao/pull/170) |
| 🔩 | **Nao Labs** `YC S24` | Core infrastructure contribution | [#150 ✅](https://github.com/getnao/nao/pull/150) |
| 🔒 | **Nao Labs** `YC S24 · Security` | Path traversal audit — confirmed mitigation, documented findings | [#66](https://github.com/getnao/nao/issues/66) |

---

## 🛠️ Tech Stack

![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![tRPC](https://img.shields.io/badge/tRPC-2596BE?style=flat-square&logo=trpc&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

---

## 🚀 Live Projects

| Project | Stack | |
|--------|-------|--|
| 🏠 **Vignaharta** — Real estate platform + Admin CMS | Next.js · PostgreSQL · Node.js | [↗ Live](https://vignaharta.vercel.app/) |
| 🎮 **PokeQuest** — Pokémon discovery engine | React.js · PokeAPI · REST | [↗ Live](https://pokequest-beige.vercel.app/) |
| 🔊 **Sonic Weaver** — 3D audio HRTF simulator | Next.js · Web Audio API | [↗ Live](https://sonic-weaver.vercel.app/) |

---

## 📊 Stats

&lt;div align="center"&gt;

![Stats](https://github-readme-stats.vercel.app/api?username=flamki&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=58a6ff&icon_color=3fb950&text_color=8b949e)
![Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=flamki&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=58a6ff&text_color=8b949e)

[![Holopin](https://holopin.me/flamki)](https://holopin.io/@flamki)

&lt;/div&gt;

---

&lt;div align="center"&gt;

🎓 B.Tech IT · Data Science · DY Patil University · 2026

🌍 **Open to remote roles internationally** — Frontend · Full Stack · React · Software Engineer

📬 [9833Ayush@gmail.com](mailto:9833Ayush@gmail.com)

&lt;img src="https://capsule-render.vercel.app/api?type=waving&color=0:58a6ff,100:0d1117&height=80&section=footer" width="100%"&gt;

&lt;/div&gt;</code></pre>
</div>

</body>
</html>
