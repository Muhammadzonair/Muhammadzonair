<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Muhammad Zonair — GitHub Profile Preview</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&family=Sora:wght@300;400;600;700&display=swap');

  :root {
    --bg: #0d1117;
    --surface: #161b22;
    --border: #30363d;
    --accent: #39d353;
    --accent2: #58a6ff;
    --text: #e6edf3;
    --muted: #8b949e;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    font-family: 'Sora', sans-serif;
    color: var(--text);
    min-height: 100vh;
    padding: 24px;
  }

  .readme {
    max-width: 860px;
    margin: 0 auto;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 40px 48px;
    animation: fadeUp 0.6s ease both;
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .header {
    text-align: center;
    margin-bottom: 36px;
  }

  .avatar-ring {
    width: 90px;
    height: 90px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--accent), var(--accent2));
    padding: 3px;
    margin: 0 auto 16px;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .avatar-inner {
    width: 100%;
    height: 100%;
    border-radius: 50%;
    background: var(--surface);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 36px;
  }

  h1 {
    font-size: 2rem;
    font-weight: 700;
    background: linear-gradient(90deg, var(--accent), var(--accent2));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin-bottom: 6px;
  }

  .subtitle {
    color: var(--muted);
    font-size: 0.95rem;
    letter-spacing: 0.05em;
    margin-bottom: 14px;
  }

  .badges {
    display: flex;
    gap: 8px;
    justify-content: center;
    flex-wrap: wrap;
    margin-bottom: 8px;
  }

  .badge {
    background: #21262d;
    border: 1px solid var(--border);
    border-radius: 20px;
    padding: 4px 12px;
    font-size: 0.72rem;
    font-family: 'JetBrains Mono', monospace;
    color: var(--accent);
  }

  hr {
    border: none;
    border-top: 1px solid var(--border);
    margin: 28px 0;
  }

  h2 {
    font-size: 1.15rem;
    font-weight: 600;
    color: var(--text);
    margin-bottom: 16px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .about-list {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 10px;
  }

  .about-list li {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    font-size: 0.9rem;
    color: var(--muted);
    line-height: 1.5;
  }

  .about-list li span.icon {
    font-size: 1rem;
    flex-shrink: 0;
  }

  .about-list li strong {
    color: var(--text);
  }

  .tech-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .tech-chip {
    padding: 6px 14px;
    border-radius: 6px;
    font-size: 0.78rem;
    font-weight: 600;
    font-family: 'JetBrains Mono', monospace;
    border: 1px solid transparent;
    transition: transform 0.2s, box-shadow 0.2s;
    cursor: default;
  }

  .tech-chip:hover {
    transform: translateY(-2px);
    box-shadow: 0 4px 12px rgba(0,0,0,0.3);
  }

  .html   { background: #E34F2618; border-color: #E34F26; color: #E34F26; }
  .css    { background: #1572B618; border-color: #1572B6; color: #1572B6; }
  .js     { background: #F7DF1E18; border-color: #F7DF1E; color: #F7DF1E; }
  .react  { background: #61DAFB18; border-color: #61DAFB; color: #61DAFB; }
  .boot   { background: #7952B318; border-color: #7952B3; color: #7952B3; }
  .git    { background: #F0503218; border-color: #F05032; color: #F05032; }
  .github { background: #ffffff18; border-color: #ffffff55; color: #e6edf3; }
  .vscode { background: #007ACC18; border-color: #007ACC; color: #007ACC; }

  .stats-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
    margin-bottom: 12px;
  }

  .stat-card {
    background: #0d1117;
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 20px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }

  .stat-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--accent), var(--accent2));
  }

  .stat-number {
    font-size: 2rem;
    font-weight: 700;
    font-family: 'JetBrains Mono', monospace;
    color: var(--accent);
  }

  .stat-label {
    font-size: 0.75rem;
    color: var(--muted);
    margin-top: 4px;
  }

  .projects-table {
    width: 100%;
    border-collapse: collapse;
    font-size: 0.87rem;
  }

  .projects-table th {
    text-align: left;
    padding: 10px 12px;
    background: #21262d;
    color: var(--muted);
    font-weight: 600;
    font-size: 0.78rem;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    border-bottom: 1px solid var(--border);
  }

  .projects-table th:first-child { border-radius: 6px 0 0 0; }
  .projects-table th:last-child  { border-radius: 0 6px 0 0; }

  .projects-table td {
    padding: 12px;
    border-bottom: 1px solid var(--border);
    vertical-align: top;
  }

  .projects-table tr:last-child td { border-bottom: none; }

  .projects-table tr:hover td {
    background: #21262d55;
  }

  .project-link {
    color: var(--accent2);
    text-decoration: none;
    font-weight: 600;
  }

  .project-link:hover { text-decoration: underline; }

  .tech-tag {
    display: inline-block;
    background: #21262d;
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 2px 8px;
    font-size: 0.7rem;
    color: var(--muted);
    font-family: 'JetBrains Mono', monospace;
    margin: 2px 2px 0 0;
  }

  .connect-card {
    background: linear-gradient(135deg, #161b22, #21262d);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 20px 24px;
    display: flex;
    align-items: center;
    gap: 16px;
    transition: border-color 0.2s;
  }

  .connect-card:hover { border-color: var(--accent2); }

  .connect-icon {
    font-size: 2rem;
    flex-shrink: 0;
  }

  .connect-info { flex: 1; }
  .connect-info .name { font-weight: 600; font-size: 0.95rem; }
  .connect-info .handle { color: var(--muted); font-size: 0.82rem; font-family: 'JetBrains Mono', monospace; }

  .visit-btn {
    background: var(--accent2);
    color: #0d1117;
    border: none;
    border-radius: 6px;
    padding: 8px 16px;
    font-size: 0.8rem;
    font-weight: 700;
    cursor: pointer;
    text-decoration: none;
    transition: opacity 0.2s;
  }

  .visit-btn:hover { opacity: 0.85; }

  .quote {
    text-align: center;
    font-style: italic;
    color: var(--muted);
    font-size: 0.88rem;
    margin-top: 8px;
    padding: 16px;
    border-top: 1px solid var(--border);
  }

  .wave-bar {
    height: 4px;
    background: linear-gradient(90deg, var(--accent), var(--accent2), var(--accent));
    background-size: 200%;
    border-radius: 2px;
    margin-top: 24px;
    animation: shimmer 3s linear infinite;
  }

  @keyframes shimmer {
    0% { background-position: 0%; }
    100% { background-position: 200%; }
  }

  .label { font-size: 0.7rem; color: var(--muted); text-align: center; margin-top: 6px; font-family: 'JetBrains Mono', monospace; }
</style>
</head>
<body>

<div class="readme">

  <!-- HEADER -->
  <div class="header">
    <div class="avatar-ring">
      <div class="avatar-inner">👨‍💻</div>
    </div>
    <h1>Muhammad Zonair</h1>
    <p class="subtitle">Frontend Developer · HTML · CSS · JavaScript · React</p>
    <div class="badges">
      <span class="badge">👁 Profile Views: Growing</span>
      <span class="badge">⭐ Open to Collaborate</span>
    </div>
  </div>

  <hr>

  <!-- ABOUT -->
  <h2>🧑‍💻 About Me</h2>
  <ul class="about-list">
    <li><span class="icon">🔭</span><div>Currently working on <strong>personal web projects & internship tasks</strong></div></li>
    <li><span class="icon">🌱</span><div>Currently learning <strong>React, advanced JavaScript & UI/UX design</strong></div></li>
    <li><span class="icon">👯</span><div>Looking to collaborate on <strong>open-source frontend projects</strong></div></li>
    <li><span class="icon">🤝</span><div>Looking for help with <strong>backend integration & APIs</strong></div></li>
    <li><span class="icon">💬</span><div>Ask me about <strong>HTML, CSS, JavaScript, React, responsive design</strong></div></li>
    <li><span class="icon">⚡</span><div>Fun fact: <strong>I build things from scratch before using frameworks — fundamentals first!</strong></div></li>
  </ul>

  <hr>

  <!-- TECH STACK -->
  <h2>🛠️ Tech Stack</h2>
  <div class="tech-grid">
    <span class="tech-chip html">HTML5</span>
    <span class="tech-chip css">CSS3</span>
    <span class="tech-chip js">JavaScript</span>
    <span class="tech-chip react">React</span>
    <span class="tech-chip boot">Bootstrap</span>
    <span class="tech-chip git">Git</span>
    <span class="tech-chip github">GitHub</span>
    <span class="tech-chip vscode">VS Code</span>
  </div>

  <hr>

  <!-- STATS -->
  <h2>📊 GitHub Stats</h2>
  <div class="stats-grid">
    <div class="stat-card">
      <div class="stat-number">9</div>
      <div class="stat-label">Public Repositories</div>
    </div>
    <div class="stat-card">
      <div class="stat-number">23</div>
      <div class="stat-label">Contributions (Last Year)</div>
    </div>
    <div class="stat-card">
      <div class="stat-number">3</div>
      <div class="stat-label">Languages Used</div>
    </div>
    <div class="stat-card">
      <div class="stat-number">🟢</div>
      <div class="stat-label">Active & Building</div>
    </div>
  </div>
  <p class="label">↑ Live stats will auto-update on GitHub via github-readme-stats</p>

  <hr>

  <!-- PROJECTS -->
  <h2>🚀 Featured Projects</h2>
  <table class="projects-table">
    <thead>
      <tr>
        <th>Project</th>
        <th>Description</th>
        <th>Tech</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><a class="project-link" href="#">🏥 Hospital Mgmt System</a></td>
        <td>Modern, responsive hospital management frontend</td>
        <td><span class="tech-tag">HTML</span><span class="tech-tag">CSS</span><span class="tech-tag">Bootstrap</span></td>
      </tr>
      <tr>
        <td><a class="project-link" href="#">🕌 Orphanage Webpage</a></td>
        <td>Warm, trustworthy landing page for an orphanage</td>
        <td><span class="tech-tag">HTML</span><span class="tech-tag">CSS</span></td>
      </tr>
      <tr>
        <td><a class="project-link" href="#">✈️ Airport Management</a></td>
        <td>Internship task built with React</td>
        <td><span class="tech-tag">JavaScript</span></td>
      </tr>
      <tr>
        <td><a class="project-link" href="#">🍽️ Restaurant Website</a></td>
        <td>Clean restaurant landing page</td>
        <td><span class="tech-tag">HTML</span><span class="tech-tag">CSS</span></td>
      </tr>
      <tr>
        <td><a class="project-link" href="#">🎓 CGPA Calculator</a></td>
        <td>React-based CGPA calculator</td>
        <td><span class="tech-tag">JavaScript</span><span class="tech-tag">React</span></td>
      </tr>
    </tbody>
  </table>

  <hr>

  <!-- CONNECT -->
  <h2>📫 Connect With Me</h2>
  <div class="connect-card">
    <div class="connect-icon">🐙</div>
    <div class="connect-info">
      <div class="name">Muhammad Zonair on GitHub</div>
      <div class="handle">@Muhammadzonair</div>
    </div>
    <a class="visit-btn" href="https://github.com/Muhammadzonair" target="_blank">Visit →</a>
  </div>

  <div class="quote">
    "First, solve the problem. Then, write the code." — John Johnson
  </div>

  <div class="wave-bar"></div>

</div>

</body>
</html>
