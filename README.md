<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Vishwas Shankar Kori — AI/ML Engineer</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@400;600;700;800&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg: #03020a;
    --surface: #0b0a1a;
    --surface2: #120f2a;
    --border: rgba(120, 80, 255, 0.18);
    --purple: #7c3aed;
    --purple-bright: #a78bfa;
    --purple-glow: rgba(167, 139, 250, 0.15);
    --cyan: #22d3ee;
    --cyan-dim: rgba(34, 211, 238, 0.12);
    --green: #10b981;
    --amber: #f59e0b;
    --pink: #ec4899;
    --text: #f1f0ff;
    --text-muted: #8b8aaa;
    --text-dim: #4b4a6a;
    --mono: 'Space Mono', monospace;
    --display: 'Syne', sans-serif;
    --body: 'DM Sans', sans-serif;
  }
  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--body);
    line-height: 1.6;
    overflow-x: hidden;
  }

  /* ANIMATED GRID BG */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(124, 58, 237, 0.04) 1px, transparent 1px),
      linear-gradient(90deg, rgba(124, 58, 237, 0.04) 1px, transparent 1px);
    background-size: 60px 60px;
    pointer-events: none;
    z-index: 0;
  }

  /* ORBS */
  .orb {
    position: fixed;
    border-radius: 50%;
    filter: blur(90px);
    pointer-events: none;
    z-index: 0;
    animation: orb-drift 20s ease-in-out infinite alternate;
  }
  .orb-1 { width: 500px; height: 500px; background: rgba(124, 58, 237, 0.12); top: -100px; left: -100px; }
  .orb-2 { width: 400px; height: 400px; background: rgba(34, 211, 238, 0.07); bottom: 10%; right: -80px; animation-delay: -10s; }
  .orb-3 { width: 300px; height: 300px; background: rgba(236, 72, 153, 0.06); top: 50%; left: 40%; animation-delay: -5s; }
  @keyframes orb-drift { from { transform: translate(0,0) scale(1); } to { transform: translate(30px, -20px) scale(1.1); } }

  /* LAYOUT */
  .container { max-width: 900px; margin: 0 auto; padding: 0 2rem; position: relative; z-index: 1; }

  /* HEADER */
  header {
    padding: 5rem 0 3rem;
    position: relative;
  }
  .header-badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: var(--purple-glow);
    border: 1px solid rgba(167, 139, 250, 0.3);
    color: var(--purple-bright);
    font-family: var(--mono);
    font-size: 11px;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    padding: 6px 14px;
    border-radius: 20px;
    margin-bottom: 1.8rem;
    animation: fade-up 0.6s ease both;
  }
  .header-badge::before { content: ''; width: 6px; height: 6px; background: var(--green); border-radius: 50%; animation: pulse-dot 2s ease infinite; }
  @keyframes pulse-dot { 0%,100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.5; transform: scale(0.8); } }

  h1 {
    font-family: var(--display);
    font-size: clamp(2.8rem, 7vw, 5rem);
    font-weight: 800;
    letter-spacing: -0.02em;
    line-height: 1.05;
    margin-bottom: 1rem;
    animation: fade-up 0.6s 0.1s ease both;
  }
  h1 span.accent { color: var(--purple-bright); }

  .tagline {
    font-family: var(--mono);
    font-size: 14px;
    color: var(--text-muted);
    letter-spacing: 0.04em;
    margin-bottom: 2rem;
    animation: fade-up 0.6s 0.2s ease both;
  }
  .tagline span { color: var(--cyan); }

  .header-links {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    animation: fade-up 0.6s 0.3s ease both;
  }
  .link-pill {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    padding: 8px 16px;
    border-radius: 8px;
    font-family: var(--mono);
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 0.06em;
    text-decoration: none;
    border: 1px solid var(--border);
    background: var(--surface);
    color: var(--text-muted);
    transition: all 0.2s ease;
  }
  .link-pill:hover { border-color: var(--purple-bright); color: var(--purple-bright); background: var(--purple-glow); transform: translateY(-1px); }
  .link-pill svg { width: 14px; height: 14px; }

  /* DIVIDER */
  .divider {
    display: flex;
    align-items: center;
    gap: 1rem;
    margin: 3rem 0 2rem;
  }
  .divider::before, .divider::after { content: ''; flex: 1; height: 1px; background: var(--border); }
  .divider-label {
    font-family: var(--mono);
    font-size: 10px;
    color: var(--text-dim);
    letter-spacing: 0.2em;
    text-transform: uppercase;
  }

  /* ABOUT */
  .about-block {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 2rem;
    margin-bottom: 2rem;
    position: relative;
    overflow: hidden;
  }
  .about-block::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--purple-bright), transparent);
  }
  .code-block {
    font-family: var(--mono);
    font-size: 13px;
    line-height: 2;
    color: var(--text-muted);
  }
  .code-block .kw { color: #ff79c6; }
  .code-block .cls { color: #8be9fd; }
  .code-block .str { color: #f1fa8c; }
  .code-block .prop { color: var(--purple-bright); }
  .code-block .arr { color: var(--green); }
  .code-block .comment { color: var(--text-dim); font-style: italic; }
  .code-block .highlight { color: var(--cyan); }

  /* SECTION HEADER */
  .section-header {
    margin-bottom: 1.5rem;
  }
  .section-tag {
    font-family: var(--mono);
    font-size: 10px;
    color: var(--purple-bright);
    letter-spacing: 0.2em;
    text-transform: uppercase;
    margin-bottom: 0.4rem;
  }
  .section-title {
    font-family: var(--display);
    font-size: 1.6rem;
    font-weight: 700;
    letter-spacing: -0.01em;
  }

  /* PROJECTS */
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(380px, 1fr));
    gap: 1.5rem;
    margin-bottom: 2rem;
  }
  .project-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 1.5rem;
    text-decoration: none;
    color: inherit;
    display: block;
    position: relative;
    overflow: hidden;
    transition: all 0.3s ease;
  }
  .project-card:hover {
    border-color: rgba(167, 139, 250, 0.5);
    background: var(--surface2);
    transform: translateY(-3px);
    box-shadow: 0 20px 60px rgba(124, 58, 237, 0.12);
  }
  .project-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 1px;
    background: linear-gradient(90deg, transparent, rgba(167,139,250,0.4), transparent);
    opacity: 0;
    transition: opacity 0.3s;
  }
  .project-card:hover::before { opacity: 1; }
  .project-accent {
    position: absolute;
    top: -20px; right: -20px;
    width: 100px; height: 100px;
    border-radius: 50%;
    filter: blur(40px);
    opacity: 0.4;
  }
  .project-number {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--text-dim);
    margin-bottom: 0.8rem;
    letter-spacing: 0.1em;
  }
  .project-title {
    font-family: var(--display);
    font-size: 1.05rem;
    font-weight: 700;
    margin-bottom: 0.6rem;
    color: var(--text);
  }
  .project-desc {
    font-size: 13.5px;
    color: var(--text-muted);
    line-height: 1.6;
    margin-bottom: 1rem;
  }
  .project-desc b { color: var(--cyan); font-weight: 500; }
  .project-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
  }
  .tag {
    font-family: var(--mono);
    font-size: 11px;
    padding: 3px 10px;
    border-radius: 20px;
    letter-spacing: 0.04em;
  }
  .tag-purple { background: rgba(124, 58, 237, 0.15); color: var(--purple-bright); border: 1px solid rgba(124,58,237,0.2); }
  .tag-cyan { background: var(--cyan-dim); color: var(--cyan); border: 1px solid rgba(34,211,238,0.2); }
  .tag-green { background: rgba(16, 185, 129, 0.12); color: var(--green); border: 1px solid rgba(16,185,129,0.2); }
  .tag-amber { background: rgba(245, 158, 11, 0.12); color: var(--amber); border: 1px solid rgba(245,158,11,0.2); }
  .tag-pink { background: rgba(236, 72, 153, 0.12); color: var(--pink); border: 1px solid rgba(236,72,153,0.2); }

  /* SKILLS */
  .skills-section { margin-bottom: 3rem; }
  .skill-group { margin-bottom: 1.5rem; }
  .skill-group-label {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--text-dim);
    letter-spacing: 0.15em;
    text-transform: uppercase;
    margin-bottom: 0.75rem;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .skill-group-label::after { content: ''; flex: 1; height: 1px; background: var(--border); }
  .skill-chips {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }
  .chip {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 6px 14px;
    border-radius: 8px;
    font-family: var(--body);
    font-size: 13px;
    font-weight: 500;
    border: 1px solid var(--border);
    background: var(--surface);
    color: var(--text-muted);
    transition: all 0.2s;
    cursor: default;
  }
  .chip:hover { border-color: rgba(167,139,250,0.4); color: var(--purple-bright); background: var(--purple-glow); }
  .chip-dot { width: 5px; height: 5px; border-radius: 50%; flex-shrink: 0; }

  /* CERTS */
  .cert-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 1.2rem 1.5rem;
    display: flex;
    align-items: center;
    gap: 1rem;
    margin-bottom: 0.75rem;
    transition: all 0.2s;
  }
  .cert-card:hover { border-color: rgba(167,139,250,0.4); background: var(--surface2); }
  .cert-icon {
    width: 40px; height: 40px;
    border-radius: 10px;
    background: var(--purple-glow);
    border: 1px solid rgba(167,139,250,0.3);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 18px;
    flex-shrink: 0;
  }
  .cert-name { font-size: 14px; font-weight: 500; color: var(--text); }
  .cert-meta { font-family: var(--mono); font-size: 11px; color: var(--text-dim); margin-top: 2px; }

  /* STATS */
  .stats-row {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 1rem;
    margin-bottom: 2rem;
  }
  .stat-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 1.2rem;
    text-align: center;
  }
  .stat-number {
    font-family: var(--display);
    font-size: 2rem;
    font-weight: 800;
    color: var(--purple-bright);
    line-height: 1;
    margin-bottom: 4px;
  }
  .stat-label { font-size: 12px; color: var(--text-dim); font-family: var(--mono); letter-spacing: 0.08em; }

  /* CTA */
  .cta-block {
    background: linear-gradient(135deg, var(--surface2) 0%, rgba(124,58,237,0.1) 100%);
    border: 1px solid rgba(167,139,250,0.25);
    border-radius: 20px;
    padding: 3rem 2rem;
    text-align: center;
    margin: 3rem 0;
    position: relative;
    overflow: hidden;
  }
  .cta-block::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--purple-bright), var(--cyan), transparent);
  }
  .cta-quote {
    font-family: var(--display);
    font-size: clamp(1rem, 3vw, 1.4rem);
    font-weight: 600;
    color: var(--text);
    margin-bottom: 0.5rem;
    font-style: italic;
  }
  .cta-sub { font-size: 13px; color: var(--text-dim); margin-bottom: 2rem; font-family: var(--mono); }
  .cta-buttons { display: flex; gap: 12px; justify-content: center; flex-wrap: wrap; }
  .btn-primary {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 12px 24px;
    border-radius: 10px;
    font-family: var(--mono);
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 0.08em;
    text-decoration: none;
    text-transform: uppercase;
    background: var(--purple);
    color: #fff;
    border: none;
    transition: all 0.2s;
    cursor: pointer;
  }
  .btn-primary:hover { background: #6d28d9; transform: translateY(-1px); box-shadow: 0 8px 24px rgba(124,58,237,0.35); }
  .btn-outline {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 12px 24px;
    border-radius: 10px;
    font-family: var(--mono);
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 0.08em;
    text-decoration: none;
    text-transform: uppercase;
    background: transparent;
    color: var(--text-muted);
    border: 1px solid var(--border);
    transition: all 0.2s;
  }
  .btn-outline:hover { border-color: var(--cyan); color: var(--cyan); background: var(--cyan-dim); transform: translateY(-1px); }

  /* FOOTER */
  footer {
    border-top: 1px solid var(--border);
    padding: 2rem 0;
    text-align: center;
    font-family: var(--mono);
    font-size: 11px;
    color: var(--text-dim);
    letter-spacing: 0.08em;
  }
  footer span { color: var(--purple-bright); }

  /* ANIMATIONS */
  @keyframes fade-up {
    from { opacity: 0; transform: translateY(16px); }
    to { opacity: 1; transform: translateY(0); }
  }
  .fade-up { animation: fade-up 0.6s ease both; }
  .delay-1 { animation-delay: 0.1s; }
  .delay-2 { animation-delay: 0.2s; }
  .delay-3 { animation-delay: 0.3s; }
  .delay-4 { animation-delay: 0.4s; }
</style>
</head>
<body>
<div class="orb orb-1"></div>
<div class="orb orb-2"></div>
<div class="orb orb-3"></div>

<div class="container">

  <!-- HEADER -->
  <header>
    <div class="header-badge">Available for AI/ML roles</div>
    <h1>Vishwas<br/><span class="accent">Shankar Kori</span></h1>
    <p class="tagline">
      AI / ML Engineer &nbsp;·&nbsp; <span>LLM Systems</span> &nbsp;·&nbsp; Agentic AI &nbsp;·&nbsp; RAG Pipelines<br/>
      B.Tech EE @ IIT Indore &nbsp;·&nbsp; Indore, India
    </p>
    <div class="header-links">
      <a href="https://www.linkedin.com/in/vishwas-kori/" class="link-pill" target="_blank">
        <svg viewBox="0 0 24 24" fill="currentColor"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect width="4" height="12" x="2" y="9"/><circle cx="4" cy="4" r="2"/></svg>
        LinkedIn
      </a>
      <a href="https://github.com/VISHWAS-dto" class="link-pill" target="_blank">
        <svg viewBox="0 0 24 24" fill="currentColor"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/></svg>
        GitHub
      </a>
      <a href="https://vishwas-dto.github.io/vishwas.portfolio/" class="link-pill" target="_blank">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><line x1="2" y1="12" x2="22" y2="12"/><path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg>
        Portfolio
      </a>
      <a href="mailto:vishwasshanker8@gmail.com" class="link-pill">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
        Email
      </a>
      <a href="https://wellfound.com/u/vishwas-kori" class="link-pill" target="_blank">
        <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 14.5v-9l6 4.5-6 4.5z"/></svg>
        Wellfound
      </a>
    </div>
  </header>

  <!-- ABOUT -->
  <div class="divider"><span class="divider-label">// about.py</span></div>
  <div class="about-block fade-up">
    <div class="code-block">
<span class="kw">class</span> <span class="cls">VishwasShankarKori</span>:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;<br/>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="prop">role</span>       = <span class="str">"ML &amp; AI Engineer"</span><br/>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="prop">education</span>  = <span class="str">"B.Tech EE @ IIT Indore (2026)"</span><br/>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="prop">location</span>   = <span class="str">"Indore, Madhya Pradesh 🇮🇳"</span><br/>
&nbsp;&nbsp;&nbsp;&nbsp;<br/>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="prop">focus</span> = <span class="arr">[</span><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="str">"LLM-Powered Systems"</span>,<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="str">"RAG Pipelines"</span>,<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="str">"Agentic AI Workflows"</span>,<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="str">"Multi-step Reasoning"</span>,<br/>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="arr">]</span><br/>
&nbsp;&nbsp;&nbsp;&nbsp;<br/>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="prop">currently</span> = <span class="highlight">"Building production-grade AI pipelines 🚀"</span><br/>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="prop">open_to</span>   = <span class="highlight">"AI/ML Engineering Roles and Collaborations"</span><br/>
    </div>
  </div>

  <!-- STATS -->
  <div class="stats-row fade-up delay-1">
    <div class="stat-card">
      <div class="stat-number">5+</div>
      <div class="stat-label">AI Projects</div>
    </div>
    <div class="stat-card">
      <div class="stat-number">3+</div>
      <div class="stat-label">LangGraph Systems</div>
    </div>
    <div class="stat-card">
      <div class="stat-number">IIT</div>
      <div class="stat-label">Indore, 2026</div>
    </div>
    <div class="stat-card">
      <div class="stat-number">∞</div>
      <div class="stat-label">Open to Build</div>
    </div>
  </div>

  <!-- PROJECTS -->
  <div class="divider"><span class="divider-label">// projects/</span></div>
  <div class="section-header fade-up">
    <p class="section-tag">Featured Work</p>
    <h2 class="section-title">Things I've built</h2>
  </div>

  <div class="projects-grid">
    <a href="https://github.com/VISHWAS-dto/Human-in-the-Loop-LLM-Chatbot-with-LangChain" class="project-card" target="_blank">
      <div class="project-accent" style="background:rgba(167,139,250,0.3)"></div>
      <div class="project-number">01 / HITL SYSTEM</div>
      <div class="project-title">Human-in-the-Loop LLM Chatbot</div>
      <div class="project-desc">Stateful chatbot with <b>LangGraph + NVIDIA NIM</b> — interrupt-driven human validation, persistent memory and approval-based response control for safer AI interactions.</div>
      <div class="project-tags">
        <span class="tag tag-purple">LangGraph</span>
        <span class="tag tag-cyan">NVIDIA NIM</span>
        <span class="tag tag-green">Stateful Memory</span>
      </div>
    </a>

    <a href="https://github.com/VISHWAS-dto/rag-application-nvidia-langchain" class="project-card" target="_blank">
      <div class="project-accent" style="background:rgba(34,211,238,0.25)"></div>
      <div class="project-number">02 / RAG PIPELINE</div>
      <div class="project-title">RAG Knowledge Assistant</div>
      <div class="project-desc">End-to-end RAG pipeline with <b>NVIDIA Embeddings + ChromaDB</b> — intelligent chunking, semantic search, and grounded LLM responses that slash hallucinations.</div>
      <div class="project-tags">
        <span class="tag tag-cyan">ChromaDB</span>
        <span class="tag tag-amber">NVIDIA NIM</span>
        <span class="tag tag-purple">LangChain</span>
      </div>
    </a>

    <a href="https://github.com/VISHWAS-dto/genai-essay-evaluation-system" class="project-card" target="_blank">
      <div class="project-accent" style="background:rgba(16,185,129,0.25)"></div>
      <div class="project-number">03 / EVAL SYSTEM</div>
      <div class="project-title">GenAI Essay Evaluation Pipeline</div>
      <div class="project-desc">Agentic pipeline with <b>parallel LangGraph nodes + Pydantic outputs</b> — multi-dimensional essay scoring across clarity, reasoning, and language at scale.</div>
      <div class="project-tags">
        <span class="tag tag-purple">LangGraph</span>
        <span class="tag tag-green">Pydantic</span>
        <span class="tag tag-cyan">Parallel Agents</span>
      </div>
    </a>

    <a href="https://github.com/VISHWAS-dto/persistence-workflow" class="project-card" target="_blank">
      <div class="project-accent" style="background:rgba(245,158,11,0.2)"></div>
      <div class="project-number">04 / MEMORY</div>
      <div class="project-title">Persistence Workflow System</div>
      <div class="project-desc">Persistent memory architecture for <b>multi-turn LLM conversations</b> — stateful LangGraph agent with dynamic context injection and compression strategies.</div>
      <div class="project-tags">
        <span class="tag tag-amber">LangGraph</span>
        <span class="tag tag-purple">LangChain</span>
        <span class="tag tag-green">Context Mgmt</span>
      </div>
    </a>

    <a href="https://github.com/VISHWAS-dto/agentic-ai-tweet-generator" class="project-card" target="_blank" style="grid-column: 1 / -1;">
      <div class="project-accent" style="background:rgba(236,72,153,0.2)"></div>
      <div class="project-number">05 / AGENTIC AI</div>
      <div class="project-title">Agentic AI Tweet Generator</div>
      <div class="project-desc">Multi-step agentic system using <b>LangGraph + LLM evaluation loops</b> — autonomously generates, scores, and refines tweets. Zero manual effort.</div>
      <div class="project-tags">
        <span class="tag tag-pink">Agentic AI</span>
        <span class="tag tag-purple">LangGraph</span>
        <span class="tag tag-cyan">Eval Loops</span>
        <span class="tag tag-green">Python</span>
      </div>
    </a>
  </div>

  <!-- SKILLS -->
  <div class="divider"><span class="divider-label">// skills/</span></div>
  <div class="section-header fade-up">
    <p class="section-tag">Technical Arsenal</p>
    <h2 class="section-title">What I work with</h2>
  </div>

  <div class="skills-section fade-up delay-1">
    <div class="skill-group">
      <div class="skill-group-label">GenAI & LLM</div>
      <div class="skill-chips">
        <span class="chip"><span class="chip-dot" style="background:var(--purple-bright)"></span>LangChain</span>
        <span class="chip"><span class="chip-dot" style="background:var(--purple-bright)"></span>LangGraph</span>
        <span class="chip"><span class="chip-dot" style="background:var(--cyan)"></span>NVIDIA NIM</span>
        <span class="chip"><span class="chip-dot" style="background:var(--amber)"></span>Hugging Face</span>
        <span class="chip"><span class="chip-dot" style="background:var(--green)"></span>Groq</span>
        <span class="chip"><span class="chip-dot" style="background:var(--pink)"></span>Prompt Engineering</span>
        <span class="chip"><span class="chip-dot" style="background:var(--purple-bright)"></span>MCP</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-label">Machine Learning</div>
      <div class="skill-chips">
        <span class="chip"><span class="chip-dot" style="background:var(--cyan)"></span>scikit-learn</span>
        <span class="chip"><span class="chip-dot" style="background:var(--green)"></span>Random Forest</span>
        <span class="chip"><span class="chip-dot" style="background:var(--amber)"></span>SVM</span>
        <span class="chip"><span class="chip-dot" style="background:var(--purple-bright)"></span>K-Means</span>
        <span class="chip"><span class="chip-dot" style="background:var(--pink)"></span>PCA</span>
        <span class="chip"><span class="chip-dot" style="background:var(--cyan)"></span>XGBoost</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-label">Deep Learning & NLP</div>
      <div class="skill-chips">
        <span class="chip"><span class="chip-dot" style="background:var(--pink)"></span>PyTorch</span>
        <span class="chip"><span class="chip-dot" style="background:var(--purple-bright)"></span>ANN / RNN</span>
        <span class="chip"><span class="chip-dot" style="background:var(--green)"></span>Embeddings</span>
        <span class="chip"><span class="chip-dot" style="background:var(--cyan)"></span>TF-IDF</span>
        <span class="chip"><span class="chip-dot" style="background:var(--amber)"></span>Tokenization</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-label">RAG & Retrieval</div>
      <div class="skill-chips">
        <span class="chip"><span class="chip-dot" style="background:var(--amber)"></span>ChromaDB</span>
        <span class="chip"><span class="chip-dot" style="background:var(--cyan)"></span>Semantic Search</span>
        <span class="chip"><span class="chip-dot" style="background:var(--purple-bright)"></span>Vectorization</span>
        <span class="chip"><span class="chip-dot" style="background:var(--green)"></span>LLM Agents</span>
        <span class="chip"><span class="chip-dot" style="background:var(--pink)"></span>SQL</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-label">Tools & Platforms</div>
      <div class="skill-chips">
        <span class="chip"><span class="chip-dot" style="background:var(--cyan)"></span>Python</span>
        <span class="chip"><span class="chip-dot" style="background:var(--pink)"></span>Streamlit</span>
        <span class="chip"><span class="chip-dot" style="background:var(--green)"></span>Flask</span>
        <span class="chip"><span class="chip-dot" style="background:var(--purple-bright)"></span>Docker</span>
        <span class="chip"><span class="chip-dot" style="background:var(--amber)"></span>Git</span>
        <span class="chip"><span class="chip-dot" style="background:var(--cyan)"></span>Jupyter</span>
        <span class="chip"><span class="chip-dot" style="background:var(--green)"></span>Pandas / NumPy</span>
        <span class="chip"><span class="chip-dot" style="background:var(--pink)"></span>Tableau</span>
      </div>
    </div>
  </div>

  <!-- CERTS -->
  <div class="divider"><span class="divider-label">// certifications/</span></div>
  <div class="section-header fade-up">
    <p class="section-tag">Credentials</p>
    <h2 class="section-title">Certifications</h2>
  </div>
  <div class="fade-up delay-1">
    <div class="cert-card">
      <div class="cert-icon">🎓</div>
      <div>
        <div class="cert-name">Complete Data Science, ML, Deep Learning & NLP Bootcamp</div>
        <div class="cert-meta">Udemy &nbsp;·&nbsp; Krish Naik</div>
      </div>
    </div>
    <div class="cert-card">
      <div class="cert-icon">🤖</div>
      <div>
        <div class="cert-name">Complete Generative AI with LangChain & Hugging Face</div>
        <div class="cert-meta">Udemy &nbsp;·&nbsp; Krish Naik</div>
      </div>
    </div>
  </div>

  <!-- CTA -->
  <div class="cta-block fade-up">
    <div class="cta-quote">"I don't just use AI — I build the systems that make AI trustworthy, scalable, and useful."</div>
    <div class="cta-sub">// actively looking for AI/ML engineering roles and GenAI collaborations</div>
    <div class="cta-buttons">
      <a href="https://www.linkedin.com/in/vishwas-kori/" class="btn-primary" target="_blank">
        <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect width="4" height="12" x="2" y="9"/><circle cx="4" cy="4" r="2"/></svg>
        Connect on LinkedIn
      </a>
      <a href="mailto:vishwasshanker8@gmail.com" class="btn-outline">
        <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
        Send a Message
      </a>
      <a href="https://vishwas-dto.github.io/vishwas.portfolio/" class="btn-outline" target="_blank">
        <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><line x1="2" y1="12" x2="22" y2="12"/><path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg>
        View Portfolio
      </a>
    </div>
  </div>

  <footer>
    crafted with intention &nbsp;·&nbsp; <span>@VISHWAS-dto</span> &nbsp;·&nbsp; Indore, India
  </footer>

</div>
</body>
</html>
