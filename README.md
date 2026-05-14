Perfil larissa · HTML
Copiar

<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>LarissaDev95 — GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&family=Space+Grotesk:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; }
  :root {
    --rich-black: #000D09;
    --dark-green: #032221;
    --bangladesh: #03624C;
    --meadow: #2CC295;
    --caribbean: #00DF81;
    --anti-flash: #F1F7F6;
    --pine: #063028;
    --font-mono: 'JetBrains Mono', monospace;
    --font-sans: 'Space Grotesk', sans-serif;
  }
  body {
    background: #0a0a0a;
    display: flex;
    justify-content: center;
    align-items: flex-start;
    min-height: 100vh;
    padding: 40px 16px;
    font-family: var(--font-sans);
  }
  .readme-wrap {
    background: var(--rich-black);
    color: var(--anti-flash);
    width: 100%;
    max-width: 860px;
    border-radius: 12px;
    overflow: hidden;
    border: 1px solid var(--pine);
  }
 
  /* HEADER */
  .header-banner {
    background: linear-gradient(135deg, var(--dark-green) 0%, var(--pine) 40%, var(--bangladesh) 100%);
    padding: 48px 40px 40px;
    position: relative;
    overflow: hidden;
    border-bottom: 2px solid var(--bangladesh);
  }
  .header-banner::before {
    content: '';
    position: absolute;
    top: -60px; right: -60px;
    width: 240px; height: 240px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(0,223,129,0.12) 0%, transparent 70%);
  }
  .header-top {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    gap: 24px;
    flex-wrap: wrap;
  }
  .header-name {
    font-size: 42px;
    font-weight: 700;
    color: var(--caribbean);
    letter-spacing: -1px;
    line-height: 1;
    font-family: var(--font-mono);
  }
  .header-name span { color: var(--meadow); }
  .header-handle {
    font-size: 14px;
    color: var(--meadow);
    font-family: var(--font-mono);
    margin-top: 6px;
    opacity: 0.85;
  }
  .header-badges {
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
    margin-top: 14px;
  }
  .badge {
    font-family: var(--font-mono);
    font-size: 11px;
    padding: 4px 12px;
    border-radius: 20px;
    font-weight: 600;
    letter-spacing: 0.5px;
  }
  .badge-green { background: var(--bangladesh); color: var(--caribbean); border: 1px solid var(--meadow); }
  .badge-mint  { background: rgba(0,223,129,0.1); color: var(--caribbean); border: 1px solid var(--caribbean); }
  .badge-dark  { background: var(--rich-black); color: var(--meadow); border: 1px solid var(--pine); }
  .typing-line {
    font-family: var(--font-mono);
    font-size: 13px;
    color: var(--meadow);
    margin-top: 18px;
    padding: 10px 16px;
    background: rgba(0,0,0,0.4);
    border-left: 3px solid var(--caribbean);
    border-radius: 0 6px 6px 0;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .cursor {
    display: inline-block; width: 8px; height: 14px;
    background: var(--caribbean);
    animation: blink 1s infinite;
    vertical-align: -2px;
  }
  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }
 
  /* SECTIONS */
  .section { padding: 28px 40px; border-bottom: 1px solid var(--pine); }
  .section-title {
    font-family: var(--font-mono);
    font-size: 12px;
    color: var(--meadow);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, var(--pine), transparent);
  }
  .dot { width: 6px; height: 6px; border-radius: 50%; background: var(--caribbean); display: inline-block; }
 
  /* WHOAMI */
  .whoami-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
  .whoami-row {
    display: flex;
    background: var(--dark-green);
    border-radius: 6px;
    overflow: hidden;
    border: 1px solid var(--pine);
  }
  .whoami-key {
    font-family: var(--font-mono);
    font-size: 12px;
    color: var(--caribbean);
    padding: 8px 12px;
    background: var(--pine);
    min-width: 90px;
    font-weight: 600;
  }
  .whoami-val {
    font-family: var(--font-mono);
    font-size: 12px;
    color: var(--anti-flash);
    padding: 8px 12px;
  }
  .online { color: var(--caribbean); }
 
  /* TECH */
  .tech-grid { display: flex; flex-wrap: wrap; gap: 8px; }
  .tech-pill {
    display: flex;
    align-items: center;
    gap: 6px;
    padding: 6px 14px;
    border-radius: 6px;
    font-family: var(--font-mono);
    font-size: 12px;
    font-weight: 600;
    border: 1px solid;
    transition: transform 0.2s;
    cursor: default;
  }
  .tech-pill:hover { transform: translateY(-2px); }
  .tech-python { background: rgba(20,53,76,0.6); color: #4dabf7; border-color: #1c3a52; }
  .tech-js     { background: rgba(50,51,48,0.6); color: #f7df1e; border-color: #3a3a20; }
  .tech-html   { background: rgba(67,21,10,0.6); color: #ff7043; border-color: #4a1f0d; }
  .tech-css    { background: rgba(14,33,57,0.6); color: #42a5f5; border-color: #0e2333; }
  .tech-linux  { background: rgba(50,40,0,0.6);  color: #fcc624; border-color: #3a3000; }
  .tech-git    { background: rgba(60,15,5,0.6);  color: #f05033; border-color: #4a1005; }
  .tech-vscode { background: rgba(0,35,60,0.6);  color: #007acc; border-color: #003050; }
  .tech-kali   { background: rgba(30,40,70,0.6); color: #557c94; border-color: #253050; }
 
  /* COURSES */
  .courses-table { width: 100%; border-collapse: collapse; font-family: var(--font-mono); font-size: 13px; }
  .courses-table th {
    color: var(--meadow);
    font-size: 11px;
    letter-spacing: 1px;
    text-transform: uppercase;
    padding: 8px 16px;
    text-align: left;
    background: var(--pine);
    border-bottom: 1px solid var(--bangladesh);
  }
  .courses-table td {
    padding: 10px 16px;
    border-bottom: 1px solid var(--dark-green);
    color: var(--anti-flash);
  }
  .courses-table tr:hover td { background: var(--dark-green); }
  .status-active  { color: var(--caribbean); font-weight: 700; }
  .status-scholar { color: #f7df1e; font-weight: 700; }
  .status-next    { color: var(--meadow); font-weight: 700; }
 
  /* STATS */
  .stats-grid { display: grid; grid-template-columns: repeat(3,1fr); gap: 12px; }
  .stat-card {
    background: var(--dark-green);
    border: 1px solid var(--bangladesh);
    border-radius: 10px;
    padding: 18px 20px;
    position: relative;
    overflow: hidden;
  }
  .stat-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--bangladesh), var(--caribbean));
  }
  .stat-label { font-family: var(--font-mono); font-size: 11px; color: var(--meadow); text-transform: uppercase; letter-spacing: 1px; margin-bottom: 6px; }
  .stat-value { font-family: var(--font-mono); font-size: 28px; font-weight: 700; color: var(--caribbean); line-height: 1; }
  .stat-sub   { font-size: 12px; color: rgba(241,247,246,0.5); margin-top: 4px; font-family: var(--font-mono); }
 
  /* GRAPH */
  .graph-row { display: flex; gap: 3px; align-items: flex-end; height: 60px; }
  .graph-bar {
    flex: 1;
    background: var(--bangladesh);
    border-radius: 2px 2px 0 0;
    min-height: 4px;
    transition: background 0.2s;
    cursor: default;
  }
  .graph-bar:hover { background: var(--caribbean); }
  .graph-labels { display: flex; justify-content: space-between; margin-top: 6px; }
  .graph-label { font-family: var(--font-mono); font-size: 10px; color: rgba(241,247,246,0.4); }
 
  /* CONNECT */
  .connect-grid { display: flex; gap: 12px; flex-wrap: wrap; }
  .connect-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 10px 20px;
    border-radius: 8px;
    font-family: var(--font-mono);
    font-size: 13px;
    font-weight: 600;
    text-decoration: none;
    cursor: pointer;
    border: 1px solid var(--bangladesh);
    background: var(--dark-green);
    color: var(--meadow);
    transition: all 0.2s;
  }
  .connect-btn:hover { background: var(--bangladesh); color: var(--caribbean); border-color: var(--caribbean); transform: translateY(-1px); }
  .connect-btn-primary { background: var(--bangladesh); color: var(--caribbean); border-color: var(--caribbean); }
 
  /* FOOTER */
  .footer {
    padding: 24px 40px;
    text-align: center;
    font-family: var(--font-mono);
    font-size: 12px;
    color: rgba(44,194,149,0.5);
    background: var(--dark-green);
  }
  .footer span { color: var(--caribbean); }
 
  @media (max-width: 600px) {
    .header-banner { padding: 32px 20px 28px; }
    .section { padding: 22px 20px; }
    .header-name { font-size: 30px; }
    .whoami-grid { grid-template-columns: 1fr; }
    .stats-grid { grid-template-columns: 1fr 1fr; }
    .footer { padding: 20px; }
  }
</style>
</head>
<body>
<div class="readme-wrap">
 
  <!-- HEADER -->
  <div class="header-banner">
    <div class="header-top">
      <div>
        <div class="header-name">Larissa<span>Corrêa</span></div>
        <div class="header-handle">@LarissaDev95</div>
        <div class="header-badges">
          <span class="badge badge-green">Full Stack Dev</span>
          <span class="badge badge-mint">🔐 Ethical Hacker</span>
          <span class="badge badge-dark">Bolsista ✅</span>
        </div>
      </div>
      <div style="text-align:right;">
        <div style="font-family:var(--font-mono);font-size:11px;color:var(--meadow);opacity:0.7;">STATUS</div>
        <div style="font-family:var(--font-mono);font-size:13px;color:var(--caribbean);margin-top:4px;">● Online &amp; Evoluindo</div>
        <div style="font-family:var(--font-mono);font-size:11px;color:rgba(241,247,246,0.4);margin-top:8px;">Mato Grosso do Sul, BR</div>
      </div>
    </div>
    <div class="typing-line">
      <span style="color:var(--caribbean);">&gt;</span>
      <span id="typing-text">Desenvolvendo sistemas seguros...</span>
      <span class="cursor"></span>
    </div>
  </div>
 
  <!-- WHOAMI -->
  <div class="section">
    <div class="section-title"><span class="dot"></span> whoami</div>
    <div class="whoami-grid">
      <div class="whoami-row"><span class="whoami-key">Nome</span><span class="whoami-val">Larissa Corrêa</span></div>
      <div class="whoami-row"><span class="whoami-key">Handle</span><span class="whoami-val">@LarissaDev95</span></div>
      <div class="whoami-row"><span class="whoami-key">Função</span><span class="whoami-val">Full Stack Dev</span></div>
      <div class="whoami-row"><span class="whoami-key">Missão</span><span class="whoami-val">Ethical Hacker 🔐</span></div>
      <div class="whoami-row"><span class="whoami-key">Bolsa</span><span class="whoami-val">Hacker Ético 🏆</span></div>
      <div class="whoami-row"><span class="whoami-key">Foco</span><span class="whoami-val">Cybersec &amp; Pentest</span></div>
      <div class="whoami-row" style="grid-column:1/-1">
        <span class="whoami-key">Status</span>
        <span class="whoami-val online">🟢 Online e em constante evolução</span>
      </div>
    </div>
  </div>
 
  <!-- TECH -->
  <div class="section">
    <div class="section-title"><span class="dot"></span> tech --list</div>
    <div class="tech-grid">
      <div class="tech-pill tech-python">🐍 Python</div>
      <div class="tech-pill tech-js">⚡ JavaScript</div>
      <div class="tech-pill tech-html">🌐 HTML5</div>
      <div class="tech-pill tech-css">🎨 CSS3</div>
      <div class="tech-pill tech-linux">🐧 Linux</div>
      <div class="tech-pill tech-git">🔀 Git</div>
      <div class="tech-pill tech-vscode">💻 VS Code</div>
      <div class="tech-pill tech-kali">🛡️ Kali Linux</div>
    </div>
  </div>
 
  <!-- STUDYING -->
  <div class="section">
    <div class="section-title"><span class="dot"></span> studying --active</div>
    <table class="courses-table">
      <thead>
        <tr>
          <th>🎓 Curso</th>
          <th>📌 Status</th>
        </tr>
      </thead>
      <tbody>
        <tr><td>Desenvolvimento de Sistemas</td><td class="status-active">[EM CURSO]</td></tr>
        <tr><td>Redes de Computadores</td><td class="status-active">[EM CURSO]</td></tr>
        <tr><td>Hacker Ético</td><td class="status-scholar">[BOLSISTA ✅]</td></tr>
        <tr><td>Cibersegurança Avançada</td><td class="status-next">[PRÓXIMO NÍVEL 🔓]</td></tr>
      </tbody>
    </table>
  </div>
 
  <!-- STATS -->
  <div class="section">
    <div class="section-title"><span class="dot"></span> github --stats</div>
    <div class="stats-grid">
      <div class="stat-card">
        <div class="stat-label">Repositórios</div>
        <div class="stat-value" id="repo-count">—</div>
        <div class="stat-sub">públicos</div>
      </div>
      <div class="stat-card">
        <div class="stat-label">Seguidores</div>
        <div class="stat-value" id="followers-count">—</div>
        <div class="stat-sub">na comunidade</div>
      </div>
      <div class="stat-card">
        <div class="stat-label">Contribuições</div>
        <div class="stat-value">∞</div>
        <div class="stat-sub">em progresso</div>
      </div>
    </div>
    <div style="margin-top:16px;">
      <div style="font-family:var(--font-mono);font-size:11px;color:var(--meadow);margin-bottom:8px;letter-spacing:1px;">ATIVIDADE — ÚLTIMAS 24 SEMANAS</div>
      <div class="graph-row" id="activity-graph"></div>
      <div class="graph-labels">
        <span class="graph-label">Jan</span>
        <span class="graph-label">Fev</span>
        <span class="graph-label">Mar</span>
        <span class="graph-label">Abr</span>
        <span class="graph-label">Mai</span>
        <span class="graph-label">Jun</span>
      </div>
    </div>
  </div>
 
  <!-- CONNECT -->
  <div class="section">
    <div class="section-title"><span class="dot"></span> connect --social</div>
    <div class="connect-grid">
      <a class="connect-btn connect-btn-primary" href="https://github.com/LarissaDev95" target="_blank">
        🐙 GitHub · LarissaDev95
      </a>
    </div>
  </div>
 
  <!-- FOOTER -->
  <div class="footer">
    <span>keep hacking 🔐</span> · feito com as cores da sua paleta · <span>@LarissaDev95</span>
  </div>
 
</div>
 
<script>
  // Typing animation
  const lines = [
    'Desenvolvendo sistemas seguros...',
    'Aprendendo Ethical Hacking...',
    'Full Stack em execução...',
    'Cibersegurança é o destino 🔐'
  ];
  let li = 0, ci = 0, del = false;
  const el = document.getElementById('typing-text');
  function type() {
    const t = lines[li];
    if (!del) {
      ci++;
      el.textContent = t.slice(0, ci);
      if (ci === t.length) { del = true; setTimeout(type, 1800); return; }
    } else {
      ci--;
      el.textContent = t.slice(0, ci);
      if (ci === 0) { del = false; li = (li + 1) % lines.length; }
    }
    setTimeout(type, del ? 35 : 60);
  }
  type();
 
  // Activity graph
  const heights = [15,25,40,20,55,30,45,60,35,50,25,40,55,30,20,45,60,25,40,55,30,50,35,45];
  const graph = document.getElementById('activity-graph');
  heights.forEach(h => {
    const b = document.createElement('div');
    b.className = 'graph-bar';
    b.style.height = h + 'px';
    b.style.opacity = 0.4 + (h / 60) * 0.6;
    graph.appendChild(b);
  });
 
  // GitHub API
  fetch('https://api.github.com/users/LarissaDev95')
    .then(r => r.json())
    .then(d => {
      if (d.public_repos !== undefined) document.getElementById('repo-count').textContent = d.public_repos;
      if (d.followers !== undefined) document.getElementById('followers-count').textContent = d.followers;
    }).catch(() => {});
</script>
</body>
</html>
