<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Abdullah Wahid — ML Engineer</title>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet" />
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@latest/tabler-icons.min.css" />
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: #f5f4f0;
    color: #1a1a18;
    min-height: 100vh;
    padding: 2rem 1rem 3rem;
  }

  .wrapper {
    max-width: 720px;
    margin: 0 auto;
  }

  /* HERO */
  .hero {
    background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
    border-radius: 16px;
    padding: 2.5rem 2rem 2rem;
    text-align: center;
    position: relative;
    overflow: hidden;
    margin-bottom: 1.25rem;
  }
  .hero::before {
    content: '';
    position: absolute; inset: 0;
    background: radial-gradient(ellipse at 20% 50%, rgba(83,74,183,0.35) 0%, transparent 60%),
                radial-gradient(ellipse at 80% 20%, rgba(29,158,117,0.25) 0%, transparent 55%);
  }
  .hero-avatar {
    width: 84px; height: 84px; border-radius: 50%;
    background: linear-gradient(135deg, #534AB7, #1D9E75);
    display: flex; align-items: center; justify-content: center;
    font-size: 28px; font-weight: 700; color: #fff;
    margin: 0 auto 1rem;
    position: relative; z-index: 1;
    border: 3px solid rgba(255,255,255,0.15);
    font-family: 'Space Mono', monospace;
  }
  .hero h1 {
    font-family: 'Space Mono', monospace;
    font-size: 22px; font-weight: 700; color: #fff;
    position: relative; z-index: 1; letter-spacing: -0.5px;
  }
  .hero p {
    font-size: 14px; color: rgba(255,255,255,0.6);
    margin-top: 6px; position: relative; z-index: 1;
  }
  .hero-badges {
    display: flex; gap: 8px; justify-content: center;
    flex-wrap: wrap; margin-top: 1.25rem;
    position: relative; z-index: 1;
  }
  .badge {
    padding: 5px 14px; border-radius: 99px;
    font-size: 12px; font-weight: 500; border: 1px solid;
  }
  .badge-purple { background: rgba(83,74,183,0.25); color: #AFA9EC; border-color: rgba(83,74,183,0.5); }
  .badge-teal   { background: rgba(29,158,117,0.2); color: #5DCAA5; border-color: rgba(29,158,117,0.4); }
  .badge-coral  { background: rgba(216,90,48,0.2);  color: #F0997B; border-color: rgba(216,90,48,0.4); }

  .contact-row {
    display: flex; gap: 8px; justify-content: center;
    margin-top: 1.25rem; position: relative; z-index: 1; flex-wrap: wrap;
  }
  .contact-btn {
    padding: 6px 14px; border-radius: 8px;
    font-size: 12px; font-weight: 500;
    display: flex; align-items: center; gap: 6px;
    text-decoration: none;
    border: 1px solid rgba(255,255,255,0.15);
    color: rgba(255,255,255,0.8);
    background: rgba(255,255,255,0.07);
    transition: background 0.2s;
  }
  .contact-btn:hover { background: rgba(255,255,255,0.14); }
  .contact-btn i { font-size: 15px; }

  /* METRICS */
  .metrics-row {
    display: grid; grid-template-columns: repeat(3, 1fr);
    gap: 8px; margin-bottom: 1.25rem;
  }
  .metric-card {
    background: #fff; border-radius: 12px;
    border: 0.5px solid #e0deda;
    padding: 1rem; text-align: center;
  }
  .metric-num {
    font-family: 'Space Mono', monospace;
    font-size: 22px; font-weight: 700; display: block;
  }
  .metric-num.purple { color: #534AB7; }
  .metric-num.teal   { color: #0F6E56; }
  .metric-num.coral  { color: #993C1D; }
  .metric-lbl { font-size: 11px; color: #888780; margin-top: 3px; display: block; }

  /* SECTION TITLE */
  .section { margin-bottom: 1.25rem; }
  .section-title {
    font-family: 'Space Mono', monospace;
    font-size: 10px; font-weight: 700;
    color: #888780; text-transform: uppercase;
    letter-spacing: 1.8px; margin-bottom: 0.75rem;
    display: flex; align-items: center; gap: 10px;
  }
  .section-title::after {
    content: ''; flex: 1; height: 0.5px; background: #e0deda;
  }

  /* EXPERIENCE CARDS */
  .exp-grid {
    display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 10px;
  }
  .exp-card {
    background: #fff; border: 0.5px solid #e0deda;
    border-radius: 14px; padding: 1rem 1.1rem;
    border-top: 3px solid transparent;
  }
  .exp-card.purple { border-top-color: #534AB7; }
  .exp-card.teal   { border-top-color: #1D9E75; }
  .exp-card.coral  { border-top-color: #D85A30; }
  .exp-card.pink   { border-top-color: #D4537E; }
  .exp-card.amber  { border-top-color: #BA7517; }

  .exp-icon {
    width: 36px; height: 36px; border-radius: 10px;
    display: flex; align-items: center; justify-content: center;
    margin-bottom: 10px; font-size: 18px;
  }
  .exp-icon.purple { background: #EEEDFE; color: #534AB7; }
  .exp-icon.teal   { background: #E1F5EE; color: #0F6E56; }
  .exp-icon.coral  { background: #FAECE7; color: #993C1D; }
  .exp-icon.pink   { background: #FBEAF0; color: #993556; }
  .exp-icon.amber  { background: #FAEEDA; color: #854F0B; }

  .exp-card h3 { font-size: 13px; font-weight: 500; color: #1a1a18; margin-bottom: 8px; }
  .exp-card ul { list-style: none; }
  .exp-card ul li {
    font-size: 12px; color: #5f5e5a;
    line-height: 1.5; padding: 3px 0 3px 14px; position: relative;
  }
  .exp-card ul li::before { content: '›'; position: absolute; left: 0; color: #b4b2a9; }

  /* SKILLS */
  .skills-box {
    background: #fff; border: 0.5px solid #e0deda;
    border-radius: 14px; padding: 1.1rem 1.25rem;
  }
  .skill-row {
    display: flex; align-items: center; gap: 12px; margin-bottom: 10px;
  }
  .skill-row:last-child { margin-bottom: 0; }
  .skill-label { font-size: 12px; font-weight: 500; color: #5f5e5a; width: 120px; flex-shrink: 0; }
  .skill-track {
    flex: 1; height: 6px; background: #f1efe8;
    border-radius: 99px; overflow: hidden;
  }
  .skill-fill {
    height: 100%; border-radius: 99px;
    animation: grow 1.1s cubic-bezier(.4,0,.2,1) forwards;
  }
  @keyframes grow { from { width: 0; } }
  .skill-pct {
    font-family: 'Space Mono', monospace;
    font-size: 11px; color: #b4b2a9; width: 32px; text-align: right; flex-shrink: 0;
  }

  /* PILLS */
  .pills { display: flex; flex-wrap: wrap; gap: 6px; }
  .pill {
    padding: 4px 12px; border-radius: 99px;
    font-size: 12px; font-weight: 500; border: 0.5px solid;
  }
  .pill-blue   { background: #E6F1FB; color: #185FA5; border-color: #B5D4F4; }
  .pill-purple { background: #EEEDFE; color: #3C3489; border-color: #CECBF6; }
  .pill-teal   { background: #E1F5EE; color: #085041; border-color: #9FE1CB; }
  .pill-amber  { background: #FAEEDA; color: #633806; border-color: #FAC775; }
  .pill-coral  { background: #FAECE7; color: #712B13; border-color: #F5C4B3; }
  .pill-gray   { background: #F1EFE8; color: #444441; border-color: #D3D1C7; }
  .pill-green  { background: #EAF3DE; color: #27500A; border-color: #C0DD97; }

  /* QUOTE */
  .quote {
    background: #fff; border-left: 3px solid #534AB7;
    border-radius: 0 12px 12px 0;
    padding: 0.9rem 1.1rem;
    font-size: 13px; color: #5f5e5a;
    font-style: italic; line-height: 1.7;
    border-top: 0.5px solid #e0deda;
    border-right: 0.5px solid #e0deda;
    border-bottom: 0.5px solid #e0deda;
  }
  .quote strong { color: #1a1a18; font-style: normal; }
</style>
</head>
<body>
<div class="wrapper">

  <div class="hero">
    <div class="hero-avatar">AW</div>
    <h1>Abdullah Wahid</h1>
    <p>Machine Learning Engineer · NLP &amp; LLM Specialist</p>
    <div class="hero-badges">
      <span class="badge badge-purple">Agentic AI</span>
      <span class="badge badge-teal">RAG Systems</span>
      <span class="badge badge-coral">LLM Fine-tuning</span>
    </div>
    <div class="contact-row">
      <a class="contact-btn" href="https://www.linkedin.com/in/abdullahwahid/" target="_blank">
        <i class="ti ti-brand-linkedin"></i> LinkedIn
      </a>
      <a class="contact-btn" href="mailto:abdullah.wahid.250@gmail.com">
        <i class="ti ti-mail"></i> Email
      </a>
      <a class="contact-btn" href="https://wa.me/201002509842" target="_blank">
        <i class="ti ti-brand-whatsapp"></i> WhatsApp
      </a>
    </div>
  </div>

  <div class="metrics-row">
    <div class="metric-card">
      <span class="metric-num purple">7+</span>
      <span class="metric-lbl">Core AI Domains</span>
    </div>
    <div class="metric-card">
      <span class="metric-num teal">10+</span>
      <span class="metric-lbl">Tools &amp; Frameworks</span>
    </div>
    <div class="metric-card">
      <span class="metric-num coral">E2E</span>
      <span class="metric-lbl">Production AI</span>
    </div>
  </div>

  <div class="section">
    <div class="section-title">Experience highlights</div>
    <div class="exp-grid">

      <div class="exp-card purple">
        <div class="exp-icon purple"><i class="ti ti-robot"></i></div>
        <h3>Agentic AI &amp; Multi-Agent Systems</h3>
        <ul>
          <li>Autonomous workflows with CrewAI, LangChain &amp; Pydantic</li>
          <li>Agentic RAG via LangGraph &amp; ReAct agents</li>
          <li>Multi-step reasoning &amp; tool-augmented retrieval</li>
        </ul>
      </div>

      <div class="exp-card teal">
        <div class="exp-icon teal"><i class="ti ti-search"></i></div>
        <h3>RAG Pipeline Engineering</h3>
        <ul>
          <li>End-to-end pipelines with LangChain &amp; LlamaIndex</li>
          <li>FAISS, Chroma &amp; Pinecone for semantic search</li>
          <li>Hallucination reduction via retrieval constraints</li>
        </ul>
      </div>

      <div class="exp-card coral">
        <div class="exp-icon coral"><i class="ti ti-adjustments"></i></div>
        <h3>LLM Fine-Tuning &amp; Optimization</h3>
        <ul>
          <li>LoRA &amp; QLoRA on custom domain datasets</li>
          <li>Improved contextual understanding &amp; accuracy</li>
          <li>OpenAI &amp; Hugging Face LLM integration</li>
        </ul>
      </div>

      <div class="exp-card pink">
        <div class="exp-icon pink"><i class="ti ti-message-dots"></i></div>
        <h3>Conversational AI &amp; Chatbots</h3>
        <ul>
          <li>Automated intent classification systems</li>
          <li>Backend API integrations &amp; optimized flows</li>
          <li>Scalable user-experience design</li>
        </ul>
      </div>

      <div class="exp-card amber">
        <div class="exp-icon amber"><i class="ti ti-chart-bar"></i></div>
        <h3>Data Analysis &amp; Insights</h3>
        <ul>
          <li>Python-based data visualization pipelines</li>
          <li>Actionable insight extraction</li>
          <li>Data-driven decision support</li>
        </ul>
      </div>

    </div>
  </div>

  <div class="section">
    <div class="section-title">Core skill proficiency</div>
    <div class="skills-box">
      <div class="skill-row">
        <span class="skill-label">LLMs &amp; RAG</span>
        <div class="skill-track"><div class="skill-fill" style="width:95%;background:#534AB7"></div></div>
        <span class="skill-pct">95%</span>
      </div>
      <div class="skill-row">
        <span class="skill-label">LangChain / Graph</span>
        <div class="skill-track"><div class="skill-fill" style="width:90%;background:#1D9E75"></div></div>
        <span class="skill-pct">90%</span>
      </div>
      <div class="skill-row">
        <span class="skill-label">Fine-tuning</span>
        <div class="skill-track"><div class="skill-fill" style="width:85%;background:#D85A30"></div></div>
        <span class="skill-pct">85%</span>
      </div>
      <div class="skill-row">
        <span class="skill-label">MLOps / Docker</span>
        <div class="skill-track"><div class="skill-fill" style="width:80%;background:#378ADD"></div></div>
        <span class="skill-pct">80%</span>
      </div>
      <div class="skill-row">
        <span class="skill-label">FastAPI / Backend</span>
        <div class="skill-track"><div class="skill-fill" style="width:82%;background:#BA7517"></div></div>
        <span class="skill-pct">82%</span>
      </div>
      <div class="skill-row">
        <span class="skill-label">PyTorch / HF</span>
        <div class="skill-track"><div class="skill-fill" style="width:88%;background:#D4537E"></div></div>
        <span class="skill-pct">88%</span>
      </div>
    </div>
  </div>

  <div class="section">
    <div class="section-title">Tech stack</div>
    <div class="pills">
      <span class="pill pill-blue">Python</span>
      <span class="pill pill-purple">LangChain</span>
      <span class="pill pill-purple">LangGraph</span>
      <span class="pill pill-purple">CrewAI</span>
      <span class="pill pill-teal">FastAPI</span>
      <span class="pill pill-teal">Docker</span>
      <span class="pill pill-teal">MLflow</span>
      <span class="pill pill-amber">PyTorch</span>
      <span class="pill pill-amber">HuggingFace</span>
      <span class="pill pill-coral">LoRA / QLoRA</span>
      <span class="pill pill-coral">FAISS</span>
      <span class="pill pill-coral">Chroma</span>
      <span class="pill pill-coral">Pinecone</span>
      <span class="pill pill-gray">PostgreSQL</span>
      <span class="pill pill-gray">MongoDB</span>
      <span class="pill pill-green">Azure</span>
      <span class="pill pill-green">Airflow</span>
      <span class="pill pill-blue">LlamaIndex</span>
      <span class="pill pill-blue">Scikit-learn</span>
      <span class="pill pill-gray">Pydantic</span>
    </div>
  </div>

  <div class="quote">
    "AI is not just about building models — it's about building systems that <strong>work in production</strong> and deliver real value."
  </div>

</div>
</body>
</html>
