<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="theme-color" content="#080a0c" />
  <meta name="description" content="Vishwas Shankar — AI/ML engineer building LLM and agentic AI systems." />
  <title>Vishwas Shankar — AI / ML Engineer</title>

  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=DM+Mono:wght@400;500&family=Manrope:wght@400;500;600;700;800&display=swap" rel="stylesheet" />

  <style>
    :root {
      color-scheme: dark;
      --bg: #080a0c;
      --panel: #0e1113;
      --panel-light: #14191a;
      --text: #edf1eb;
      --muted: #8b9590;
      --line: rgba(222, 239, 227, .12);
      --green: #c4f26b;
      --mint: #80edc0;
      --mono: "DM Mono", monospace;
      --sans: "Manrope", sans-serif;
      --page: 1180px;
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      background:
        radial-gradient(ellipse at 80% 10%, rgba(80, 127, 96, .11), transparent 30rem),
        var(--bg);
      color: var(--text);
      font-family: var(--sans);
      -webkit-font-smoothing: antialiased;
    }
    a { color: inherit; text-decoration: none; }
    button { font: inherit; }
    ::selection { background: var(--green); color: #111; }

    .shell { width: min(var(--page), calc(100% - 48px)); margin: 0 auto; }
    .mono { font-family: var(--mono); }
    .eyebrow {
      color: var(--green);
      font: 500 11px var(--mono);
      letter-spacing: .16em;
      text-transform: uppercase;
    }

    .topbar {
      position: sticky;
      top: 0;
      z-index: 10;
      border-bottom: 1px solid var(--line);
      background: rgba(8, 10, 12, .78);
      backdrop-filter: blur(18px);
    }
    .nav {
      height: 72px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    .brand {
      display: inline-flex;
      align-items: center;
      gap: 12px;
      font-size: 13px;
      font-weight: 800;
      letter-spacing: -.03em;
    }
    .brand-mark {
      width: 28px;
      height: 28px;
      display: grid;
      place-items: center;
      border: 1px solid rgba(196, 242, 107, .45);
      border-radius: 50%;
      color: var(--green);
      font: 12px var(--mono);
    }
    .nav-links { display: flex; align-items: center; gap: 32px; }
    .nav-links a {
      color: #aab2ad;
      font: 11px var(--mono);
      transition: color .2s;
    }
    .nav-links a:hover { color: var(--green); }
    .nav-contact {
      border: 1px solid var(--line);
      padding: 11px 15px;
      border-radius: 2px;
      color: var(--text) !important;
    }
    .nav-contact:hover { border-color: var(--green); }

    .hero {
      min-height: 690px;
      display: grid;
      grid-template-columns: 1.05fr .95fr;
      align-items: center;
      gap: 48px;
      padding: 72px 0 82px;
      position: relative;
    }
    .hero-copy { position: relative; z-index: 1; }
    .availability {
      display: inline-flex;
      align-items: center;
      gap: 9px;
      margin-bottom: 30px;
      padding: 9px 12px;
      border: 1px solid var(--line);
      color: #b9c2bc;
      font: 10px var(--mono);
      letter-spacing: .06em;
      text-transform: uppercase;
    }
    .pulse {
      width: 7px; height: 7px; border-radius: 50%;
      background: var(--green);
      box-shadow: 0 0 13px rgba(196, 242, 107, .8);
    }
    h1 {
      max-width: 700px;
      margin: 0;
      font-size: clamp(52px, 7.2vw, 94px);
      line-height: .98;
      letter-spacing: -.085em;
      font-weight: 600;
    }
    h1 span { color: var(--green); }
    .hero-lede {
      max-width: 520px;
      margin: 27px 0 0;
      color: #a4ada7;
      font-size: 16px;
      line-height: 1.8;
    }
    .hero-actions { display: flex; gap: 12px; margin-top: 34px; flex-wrap: wrap; }
    .button {
      display: inline-flex;
      align-items: center;
      gap: 12px;
      padding: 14px 17px;
      border: 1px solid var(--line);
      font: 11px var(--mono);
      transition: transform .2s, border-color .2s, background .2s;
    }
    .button:hover { transform: translateY(-2px); border-color: var(--green); }
    .button-primary { background: var(--green); border-color: var(--green); color: #10130c; }
    .button-primary:hover { background: #d5ff87; }
    .arrow { font-size: 16px; line-height: 10px; }

    .hero-visual {
      position: relative;
      min-height: 470px;
      display: grid;
      place-items: center;
      overflow: hidden;
      border: 1px solid var(--line);
      background:
        linear-gradient(rgba(255,255,255,.025) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,.025) 1px, transparent 1px),
        radial-gradient(circle at 50% 50%, rgba(115, 192, 143, .11), transparent 48%),
        #0b0e10;
      background-size: 34px 34px, 34px 34px, auto, auto;
    }
    .visual-label {
      position: absolute;
      top: 20px; left: 20px;
      color: #748079;
      font: 9px var(--mono);
      letter-spacing: .12em;
      text-transform: uppercase;
    }
    .visual-index {
      position: absolute;
      right: 20px; bottom: 18px;
      color: #748079;
      font: 9px var(--mono);
    }
    .orbit {
      position: absolute;
      width: min(78%, 360px);
      aspect-ratio: 1;
      border: 1px solid rgba(196, 242, 107, .17);
      border-radius: 50%;
      animation: rotate 36s linear infinite;
    }
    .orbit::before, .orbit::after {
      content: "";
      position: absolute;
      inset: 12%;
      border: 1px solid rgba(128, 237, 192, .17);
      border-radius: 50%;
      transform: rotateX(68deg) rotateZ(24deg);
    }
    .orbit::after {
      inset: 23%;
      border-color: rgba(196, 242, 107, .25);
      transform: rotateX(68deg) rotateZ(-34deg);
    }
    .orbit-dot {
      position: absolute;
      left: 17%; top: 18%;
      width: 7px; height: 7px;
      background: var(--green);
      border-radius: 50%;
      box-shadow: 0 0 18px var(--green);
    }
    .core {
      width: 135px; height: 135px;
      display: grid;
      place-items: center;
      position: relative;
      z-index: 1;
      border: 1px solid rgba(196, 242, 107, .45);
      border-radius: 50%;
      background: radial-gradient(circle, rgba(196,242,107,.14), rgba(10,15,12,.7) 68%);
      box-shadow: 0 0 80px rgba(128, 237, 192, .12), inset 0 0 28px rgba(128,237,192,.08);
      color: var(--green);
      font: 12px var(--mono);
      letter-spacing: .1em;
    }
    .core::before, .core::after {
      content: "";
      position: absolute;
      inset: -15px;
      border: 1px solid rgba(128,237,192,.14);
      border-radius: 50%;
    }
    .core::after { inset: -30px; border-color: rgba(128,237,192,.08); }
    .float-card {
      position: absolute;
      z-index: 2;
      min-width: 132px;
      padding: 12px 13px;
      border: 1px solid rgba(222,239,227,.14);
      background: rgba(12,16,16,.88);
      backdrop-filter: blur(10px);
    }
    .float-card small { display: block; color: #77837b; font: 9px var(--mono); text-transform: uppercase; }
    .float-card strong { display: block; margin-top: 7px; color: #dbe5dd; font: 11px var(--mono); }
    .card-a { top: 22%; left: 8%; }
    .card-b { top: 35%; right: 7%; }
    .card-c { bottom: 20%; left: 15%; }

    .ticker {
      border-top: 1px solid var(--line);
      border-bottom: 1px solid var(--line);
      overflow: hidden;
      background: rgba(255,255,255,.015);
    }
    .ticker-track {
      display: flex;
      justify-content: space-around;
      gap: 40px;
      padding: 18px 0;
      color: #8e9991;
      font: 10px var(--mono);
      letter-spacing: .12em;
      text-transform: uppercase;
      white-space: nowrap;
    }
    .ticker-track span::before { content: "✳"; color: var(--green); margin-right: 12px; }

    section { padding: 112px 0; border-bottom: 1px solid var(--line); }
    .section-head {
      display: flex;
      justify-content: space-between;
      align-items: end;
      gap: 30px;
      margin-bottom: 48px;
    }
    .section-head h2 {
      margin: 12px 0 0;
      font-size: clamp(34px, 5vw, 58px);
      line-height: 1;
      font-weight: 500;
      letter-spacing: -.07em;
    }
    .section-note { max-width: 330px; color: var(--muted); font-size: 13px; line-height: 1.7; }

    .about-grid { display: grid; grid-template-columns: .8fr 1.2fr; gap: 70px; }
    .about-statement {
      margin: 0;
      max-width: 430px;
      font-size: clamp(25px, 3.5vw, 40px);
      line-height: 1.3;
      letter-spacing: -.055em;
    }
    .about-statement em { color: var(--green); font-style: normal; }
    .about-copy { color: #9ba69f; font-size: 14px; line-height: 1.9; }
    .career-row {
      display: grid;
      grid-template-columns: 140px 1fr auto;
      gap: 18px;
      align-items: center;
      padding: 18px 0;
      border-top: 1px solid var(--line);
      font-size: 12px;
    }
    .career-row:last-child { border-bottom: 1px solid var(--line); }
    .career-date { color: #77827b; font: 10px var(--mono); }
    .career-role { color: #dce5dd; font-weight: 600; }
    .career-company { color: var(--green); font: 10px var(--mono); }

    .skill-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 12px; }
    .skill-card {
      min-height: 196px;
      padding: 25px;
      border: 1px solid var(--line);
      background: linear-gradient(145deg, rgba(255,255,255,.035), rgba(255,255,255,.008));
      transition: border-color .2s, transform .2s;
    }
    .skill-card:hover { border-color: rgba(196,242,107,.42); transform: translateY(-3px); }
    .skill-top { display: flex; justify-content: space-between; align-items: center; }
    .skill-number { color: #69766e; font: 10px var(--mono); }
    .skill-icon { color: var(--green); font-size: 17px; }
    .skill-card h3 { margin: 26px 0 12px; font-size: 17px; font-weight: 600; letter-spacing: -.04em; }
    .skill-card p { margin: 0; color: #8f9a92; font-size: 12px; line-height: 1.8; }

    .tool-cloud { display: flex; flex-wrap: wrap; gap: 9px; margin-top: 27px; }
    .tool {
      border: 1px solid var(--line);
      padding: 9px 11px;
      color: #aab4ac;
      font: 10px var(--mono);
      transition: color .2s, border-color .2s;
    }
    .tool:hover { color: var(--green); border-color: rgba(196,242,107,.4); }

    .contact {
      display: grid;
      grid-template-columns: 1fr auto;
      align-items: end;
      gap: 30px;
    }
    .contact h2 { max-width: 680px; }
    .contact-links { display: flex; flex-direction: column; min-width: 220px; }
    .contact-links a {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 14px 0;
      border-bottom: 1px solid var(--line);
      color: #b5c0b8;
      font: 11px var(--mono);
    }
    .contact-links a:hover { color: var(--green); }

    footer { padding: 24px 0; color: #67736b; font: 9px var(--mono); }
    .footer-inner { display: flex; justify-content: space-between; gap: 20px; }

    @keyframes rotate { to { transform: rotate(360deg); } }
    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after { scroll-behavior: auto !important; animation-duration: .01ms !important; transition-duration: .01ms !important; }
    }
    @media (max-width: 800px) {
      .hero { grid-template-columns: 1fr; padding-top: 65px; }
      .hero-visual { min-height: 410px; }
      .about-grid { grid-template-columns: 1fr; gap: 35px; }
      .section-head { align-items: start; flex-direction: column; }
      .contact { grid-template-columns: 1fr; }
      .contact-links { max-width: 420px; }
    }
    @media (max-width: 560px) {
      .shell { width: min(100% - 32px, var(--page)); }
      .nav { height: 62px; }
      .nav-links { gap: 14px; }
      .nav-links a:not(.nav-contact) { display: none; }
      .hero { min-height: auto; padding: 62px 0; gap: 36px; }
      .hero-visual { min-height: 350px; }
      .float-card { min-width: 112px; padding: 10px; }
      .card-a { left: 4%; }
      .card-b { right: 3%; }
      .card-c { left: 7%; }
      .ticker-track { justify-content: flex-start; gap: 26px; }
      section { padding: 78px 0; }
      .skill-grid { grid-template-columns: 1fr; }
      .career-row { grid-template-columns: 1fr auto; }
      .career-date { grid-column: 1 / -1; }
      .footer-inner { flex-direction: column; }
    }
  </style>
</head>

<body>
  <header class="topbar">
    <nav class="nav shell" aria-label="Main navigation">
      <a class="brand" href="#home" aria-label="Vishwas Shankar home">
        <span class="brand-mark">VS</span>
        <span>VISHWAS SHANKAR</span>
      </a>
      <div class="nav-links">
        <a href="#about">ABOUT</a>
        <a href="#expertise">EXPERTISE</a>
        <a class="nav-contact" href="#contact">LET’S TALK <span class="arrow">↗</span></a>
      </div>
    </nav>
  </header>

  <main>
    <section class="hero shell" id="home">
      <div class="hero-copy">
        <div class="availability"><span class="pulse"></span> AI / ML ENGINEER · BACKEND DEVELOPER</div>
        <h1>Intelligence,<br /><span>engineered.</span></h1>
        <p class="hero-lede">
          I’m Vishwas Shankar. I build LLM and agentic AI systems, retrieval pipelines,
          and the backend foundations that bring them into the real world.
        </p>
        <div class="hero-actions">
          <a class="button button-primary" href="https://vishwas-dto.github.io/vishwas.portfolio/" target="_blank" rel="noreferrer">
            EXPLORE PORTFOLIO <span class="arrow">↗</span>
          </a>
          <a class="button" href="https://github.com/VISHWAS-dto?tab=repositories" target="_blank" rel="noreferrer">
            VIEW GITHUB <span class="arrow">↗</span>
          </a>
        </div>
      </div>

      <div class="hero-visual" aria-label="Abstract visualization of connected AI systems">
        <span class="visual-label">SYSTEMS / 01 — 04</span>
        <div class="orbit"><span class="orbit-dot"></span></div>
        <div class="core">AI SYSTEMS</div>
        <div class="float-card card-a"><small>Architecture</small><strong>RETRIEVAL → REASONING</strong></div>
        <div class="float-card card-b"><small>Orchestration</small><strong>TOOLS · AGENTS · APIs</strong></div>
        <div class="float-card card-c"><small>Focus</small><strong>BUILT FOR THE REAL WORLD</strong></div>
        <span class="visual-index">FIG 01 / CONNECTED INTELLIGENCE</span>
      </div>
    </section>

    <div class="ticker" aria-label="Areas of focus">
      <div class="ticker-track shell">
        <span>Generative AI</span><span>RAG Pipelines</span><span>Agentic Systems</span>
        <span>Backend Engineering</span><span>System Design</span>
      </div>
    </div>

    <section id="about">
      <div class="shell">
        <div class="section-head">
          <div>
            <div class="eyebrow">01 — THE ENGINEER</div>
            <h2>Built to make<br />complexity useful.</h2>
          </div>
          <p class="section-note">A blend of applied AI, product-minded backend engineering, and thoughtful system design.</p>
        </div>

        <div class="about-grid">
          <p class="about-statement">
            Turning emerging AI capabilities into <em>reliable systems</em> people can actually use.
          </p>
          <div>
            <p class="about-copy">
              My work sits where machine learning meets software engineering. I’m focused on
              Generative AI, retrieval augmented generation, and agentic workflows, supported
              by clean APIs and scalable backend architecture.
            </p>
            <div class="career-row">
              <span class="career-date">CURRENT</span>
              <span class="career-role">Backend Developer</span>
              <span class="career-company">CATALYX</span>
            </div>
            <div class="career-row">
              <span class="career-date">PREVIOUS</span>
              <span class="career-role">Software Engineer</span>
              <span class="career-company">LACTO</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="expertise">
      <div class="shell">
        <div class="section-head">
          <div>
            <div class="eyebrow">02 — CAPABILITIES</div>
            <h2>Where I create<br />momentum.</h2>
          </div>
          <p class="section-note">From model-powered workflows to the dependable services behind them.</p>
        </div>

        <div class="skill-grid">
          <article class="skill-card">
            <div class="skill-top"><span class="skill-number">CAPABILITY / 01</span><span class="skill-icon">✳</span></div>
            <h3>Generative AI &amp; RAG</h3>
            <p>Retrieval pipelines, vector embeddings, and LLM applications designed around useful context and clear outcomes.</p>
          </article>
          <article class="skill-card">
            <div class="skill-top"><span class="skill-number">CAPABILITY / 02</span><span class="skill-icon">⌘</span></div>
            <h3>Agents &amp; orchestration</h3>
            <p>Agentic workflows and tool coordination with LangChain, LangGraph, and n8n.</p>
          </article>
          <article class="skill-card">
            <div class="skill-top"><span class="skill-number">CAPABILITY / 03</span><span class="skill-icon">↗</span></div>
            <h3>Backend &amp; APIs</h3>
            <p>Python services, REST APIs, and application backends built with practical frameworks and clean interfaces.</p>
          </article>
          <article class="skill-card">
            <div class="skill-top"><span class="skill-number">CAPABILITY / 04</span><span class="skill-icon">◈</span></div>
            <h3>Systems &amp; infrastructure</h3>
            <p>Microservices, scalable architecture, data modeling, containerization, and cloud fundamentals.</p>
          </article>
        </div>

        <div class="tool-cloud" aria-label="Technologies">
          <span class="tool">Python</span><span class="tool">PyTorch</span><span class="tool">FastAPI</span>
          <span class="tool">Django</span><span class="tool">Flask</span><span class="tool">Node.js</span>
          <span class="tool">SQL</span><span class="tool">LangChain</span><span class="tool">LangGraph</span>
          <span class="tool">n8n</span><span class="tool">C++</span><span class="tool">JavaScript</span>
          <span class="tool">Java</span><span class="tool">React</span><span class="tool">Docker</span>
          <span class="tool">AWS</span><span class="tool">Git</span><span class="tool">MLOps</span>
        </div>
      </div>
    </section>

    <section id="contact">
      <div class="shell contact">
        <div>
          <div class="eyebrow">03 — OPEN CHANNEL</div>
          <h2>Have a meaningful<br />problem to solve?</h2>
          <p class="hero-lede">Let’s talk about AI, backend systems, or the next thing you’re building.</p>
        </div>
        <div class="contact-links">
          <a href="mailto:vishwasshanker8@gmail.com"><span>EMAIL</span><span>↗</span></a>
          <a href="https://www.linkedin.com/in/vishwas-kori/" target="_blank" rel="noreferrer"><span>LINKEDIN</span><span>↗</span></a>
          <a href="https://github.com/VISHWAS-dto" target="_blank" rel="noreferrer"><span>GITHUB</span><span>↗</span></a>
          <a href="https://vishwas-dto.github.io/vishwas.portfolio/" target="_blank" rel="noreferrer"><span>PORTFOLIO</span><span>↗</span></a>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="shell footer-inner">
      <span>© <span id="year"></span> VISHWAS SHANKAR</span>
      <span>DESIGNED FOR WHAT’S NEXT · BUILT FOR THE WEB</span>
    </div>
  </footer>

  <script>
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>
```
