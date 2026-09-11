<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ermiyas Abate — Security &amp; Software</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;600;700&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#0f1720;
    --panel:#141d29;
    --border:#28333f;
    --amber:#e8a33d;
    --teal:#5fd6c8;
    --text:#e7e9ec;
    --muted:#8b96a5;
  }

  *{box-sizing:border-box;}

  body{
    margin:0;
    background:var(--ink);
    color:var(--text);
    font-family:'Inter',sans-serif;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }

  a{color:var(--amber);}

  code,.mono{
    font-family:'JetBrains Mono',monospace;
  }

  .wrap{
    max-width:760px;
    margin:0 auto;
    padding:64px 24px 96px;
  }

  /* ---------- terminal window shell ---------- */
  .term{
    background:var(--panel);
    border:1px solid var(--border);
    border-radius:8px;
    overflow:hidden;
    margin-bottom:28px;
  }

  .term-bar{
    display:flex;
    align-items:center;
    gap:8px;
    padding:10px 14px;
    background:#0d141d;
    border-bottom:1px solid var(--border);
  }

  .dot{width:10px;height:10px;border-radius:50%;}
  .dot.r{background:#e2645b;}
  .dot.y{background:#e6b955;}
  .dot.g{background:#5fbf68;}

  .term-title{
    margin-left:8px;
    font-family:'JetBrains Mono',monospace;
    font-size:12.5px;
    color:var(--muted);
  }

  .term-body{padding:22px 22px 26px;}

  .prompt{
    font-family:'JetBrains Mono',monospace;
    font-size:14px;
    color:var(--teal);
    margin:0 0 10px;
  }
  .prompt span{color:var(--muted);}

  /* ---------- hero ---------- */
  .hero-name{
    font-family:'JetBrains Mono',monospace;
    font-weight:700;
    font-size:clamp(28px,5vw,38px);
    margin:0 0 4px;
    letter-spacing:-0.5px;
  }

  .hero-role{
    color:var(--muted);
    font-size:15px;
    margin:0 0 20px;
  }

  .hero-body p{margin:0 0 14px;max-width:62ch;}
  .hero-body p:last-child{margin-bottom:0;}

  .badges{
    display:flex;
    gap:12px;
    align-items:center;
    margin-top:18px;
    flex-wrap:wrap;
  }
  .badges img{display:block;}

  /* ---------- section headings ---------- */
  h2.section-head{
    font-family:'JetBrains Mono',monospace;
    font-size:14px;
    font-weight:500;
    color:var(--muted);
    margin:0 0 16px;
  }
  h2.section-head .path{color:var(--amber);}

  /* ---------- stack chips ---------- */
  .stack-grid{
    display:flex;
    flex-wrap:wrap;
    gap:10px;
  }

  .chip{
    display:flex;
    align-items:center;
    gap:9px;
    padding:9px 14px;
    background:#0d141d;
    border:1px solid var(--border);
    border-radius:6px;
    font-family:'JetBrains Mono',monospace;
    font-size:13px;
    color:var(--text);
  }

  .chip .sw{width:9px;height:9px;border-radius:2px;flex:none;}

  /* ---------- stats grid ---------- */
  .stats-grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:18px;
  }
  .stats-grid img{width:100%;display:block;border-radius:4px;}
  .stats-full img{width:100%;display:block;border-radius:4px;}

  @media (max-width:620px){
    .stats-grid{grid-template-columns:1fr;}
  }

  /* ---------- footer ---------- */
  footer{
    margin-top:40px;
    padding-top:20px;
    border-top:1px solid var(--border);
    font-family:'JetBrains Mono',monospace;
    font-size:12.5px;
    color:var(--muted);
    display:flex;
    justify-content:space-between;
    flex-wrap:wrap;
    gap:10px;
  }

  @media (prefers-reduced-motion:no-preference){
    .term{animation:rise .5s ease-out both;}
  }
  @keyframes rise{
    from{opacity:0;transform:translateY(8px);}
    to{opacity:1;transform:translateY(0);}
  }
</style>
</head>
<body>
<div class="wrap">

  <!-- Hero: whoami -->
  <section class="term">
    <div class="term-bar">
      <span class="dot r"></span><span class="dot y"></span><span class="dot g"></span>
      <span class="term-title">whoami</span>
    </div>
    <div class="term-body">
      <p class="prompt"><span>ermiyas@addis-ababa:~$</span> whoami</p>
      <h1 class="hero-name">Ermiyas Abate</h1>
      <p class="hero-role">Computer scientist · security researcher · Addis Ababa, Ethiopia</p>
      <div class="hero-body">
        <p>I hold a Bachelor's and Master's degree in Computer Science and spend most of my time now on cybersecurity and ethical hacking — breaking systems on purpose so I can help teams fix them before someone else finds the gap.</p>
        <p>I care about the mechanics underneath a system as much as the surface: how it fails, where it trusts too much, and what it takes to make it hold.</p>
      </div>
      <div class="badges">
        <img src="https://komarev.com/ghpvc/?username=ermiyasabate&label=Profile%20views&color=e8a33d&style=flat-square" alt="Profile view counter for ermiyasabate">
      </div>
    </div>
  </section>

  <!-- Stack -->
  <section class="term">
    <div class="term-bar">
      <span class="dot r"></span><span class="dot y"></span><span class="dot g"></span>
      <span class="term-title">stack.json</span>
    </div>
    <div class="term-body">
      <h2 class="section-head"><span class="path">~/stack</span> $ ls</h2>
      <div class="stack-grid">
        <span class="chip"><span class="sw" style="background:#E34F26;"></span>HTML5</span>
        <span class="chip"><span class="sw" style="background:#1572B6;"></span>CSS3</span>
        <span class="chip"><span class="sw" style="background:#F7DF1E;"></span>JavaScript</span>
        <span class="chip"><span class="sw" style="background:#3776AB;"></span>Python</span>
        <span class="chip"><span class="sw" style="background:#3178C6;"></span>TypeScript</span>
      </div>
    </div>
  </section>

  <!-- GitHub stats -->
  <section class="term">
    <div class="term-bar">
      <span class="dot r"></span><span class="dot y"></span><span class="dot g"></span>
      <span class="term-title">stats.log</span>
    </div>
    <div class="term-body">
      <h2 class="section-head"><span class="path">~/github</span> $ fetch --stats</h2>
      <div class="stats-grid">
        <img src="https://github-readme-stats.vercel.app/api?username=ermiyasabate&theme=catppuccin_mocha&show_icons=true&locale=en&hide_border=true&bg_color=0d141d" alt="GitHub stats for ermiyasabate">
        <img src="https://github-readme-streak-stats.herokuapp.com/?user=ermiyasabate&theme=catppuccin_mocha&hide_border=true&background=0d141d" alt="GitHub streak stats for ermiyasabate">
      </div>
    </div>
  </section>

  <section class="term">
    <div class="term-bar">
      <span class="dot r"></span><span class="dot y"></span><span class="dot g"></span>
      <span class="term-title">breakdown.log</span>
    </div>
    <div class="term-body">
      <h2 class="section-head"><span class="path">~/github</span> $ fetch --languages --hours</h2>
      <div class="stats-grid">
        <img src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=ermiyasabate&theme=algolia" alt="Repos per language for ermiyasabate">
        <img src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=ermiyasabate&theme=algolia" alt="Most productive time for ermiyasabate">
      </div>
    </div>
  </section>

  <section class="term">
    <div class="term-bar">
      <span class="dot r"></span><span class="dot y"></span><span class="dot g"></span>
      <span class="term-title">profile.log</span>
    </div>
    <div class="term-body">
      <h2 class="section-head"><span class="path">~/github</span> $ fetch --profile-details</h2>
      <div class="stats-full">
        <img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=ermiyasabate&theme=algolia" alt="Profile details for ermiyasabate">
      </div>
    </div>
  </section>

  <!-- Trophies -->
  <section class="term">
    <div class="term-bar">
      <span class="dot r"></span><span class="dot y"></span><span class="dot g"></span>
      <span class="term-title">trophies.log</span>
    </div>
    <div class="term-body">
      <h2 class="section-head"><span class="path">~/github</span> $ fetch --trophies</h2>
      <div class="stats-full">
        <img src="https://github-profile-trophy.vercel.app/?username=ermiyasabate&theme=catppuccin_mocha&margin-w=6&column=9&no-bg=true" alt="GitHub trophies for ermiyasabate">
      </div>
    </div>
  </section>

  <footer>
    <span>github.com/ermiyasabate</span>
    <span>last login: Addis Ababa, ET</span>
  </footer>

</div>
</body>
</html>
