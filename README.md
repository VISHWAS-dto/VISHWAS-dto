<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Vishwas Shankar Kori | AI Engineer</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Poppins', sans-serif;
      background: #0f0c29;
      color: #fff;
      line-height: 1.6;
    }

    header {
      text-align: center;
      padding: 80px 20px;
      background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
    }

    header h1 {
      font-size: 3rem;
      margin-bottom: 10px;
    }

    header p {
      font-size: 1.2rem;
      color: #cbd5e1;
    }

    section {
      padding: 60px 20px;
      max-width: 1100px;
      margin: auto;
    }

    h2 {
      text-align: center;
      margin-bottom: 30px;
      font-size: 2rem;
      color: #a78bfa;
    }

    .about {
      text-align: center;
      max-width: 700px;
      margin: auto;
    }

    .projects {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
    }

    .card {
      background: #1e1b4b;
      padding: 20px;
      border-radius: 15px;
      transition: 0.3s;
    }

    .card:hover {
      transform: translateY(-5px);
      background: #2e2a7a;
    }

    .card h3 {
      margin-bottom: 10px;
      color: #c4b5fd;
    }

    .skills {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 10px;
    }

    .skill {
      background: #302b63;
      padding: 8px 15px;
      border-radius: 20px;
      font-size: 0.9rem;
    }

    footer {
      text-align: center;
      padding: 30px;
      background: #0f0c29;
      color: #aaa;
    }

    a {
      color: #a78bfa;
      text-decoration: none;
    }

    .btn {
      display: inline-block;
      margin-top: 15px;
      padding: 10px 20px;
      background: #7c3aed;
      border-radius: 25px;
      color: white;
      transition: 0.3s;
    }

    .btn:hover {
      background: #a78bfa;
    }
  </style>
</head>
<body>

<header>
  <h1>Vishwas Shankar Kori</h1>
  <p>AI/ML Engineer | LLM Systems | Agentic AI | RAG Pipelines</p>
  <a href="#contact" class="btn">Let's Connect</a>
</header>

<section>
  <h2>About Me</h2>
  <p class="about">
    I build scalable AI systems focused on reliability, reasoning, and production deployment. 
    My work revolves around LLM systems, RAG pipelines, and agentic AI workflows.
  </p>
</section>

<section>
  <h2>Projects</h2>
  <div class="projects">
    <div class="card">
      <h3>Human-in-the-Loop Chatbot</h3>
      <p>Stateful AI chatbot with human validation for safe responses.</p>
    </div>
    <div class="card">
      <h3>RAG Knowledge Assistant</h3>
      <p>End-to-end retrieval system with reduced hallucination.</p>
    </div>
    <div class="card">
      <h3>Essay Evaluation System</h3>
      <p>Multi-agent pipeline for automated scoring.</p>
    </div>
    <div class="card">
      <h3>Agentic Tweet Generator</h3>
      <p>Autonomous content generation with feedback loops.</p>
    </div>
  </div>
</section>

<section>
  <h2>Skills</h2>
  <div class="skills">
    <span class="skill">LangChain</span>
    <span class="skill">LangGraph</span>
    <span class="skill">PyTorch</span>
    <span class="skill">RAG</span>
    <span class="skill">ChromaDB</span>
    <span class="skill">Python</span>
    <span class="skill">Docker</span>
    <span class="skill">SQL</span>
  </div>
</section>

<section id="contact">
  <h2>Contact</h2>
  <p style="text-align:center;">
    <a href="mailto:vishwasshanker8@gmail.com">Email</a> | 
    <a href="https://www.linkedin.com/in/vishwas-kori/">LinkedIn</a> | 
    <a href="https://github.com/VISHWAS-dto">GitHub</a>
  </p>
</section>

<footer>
  <p>© 2026 Vishwas Shankar Kori</p>
</footer>

</body>
</html>
