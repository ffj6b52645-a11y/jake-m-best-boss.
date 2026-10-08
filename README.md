<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta
    name="description"
    content="Jake M — professional software developer, builder, and problem solver."
  />
  <title>Jake M | Developer</title>

  <style>
    :root {
      --bg: #0d1117;
      --bg-light: #161b22;
      --card: #111820;
      --border: #30363d;
      --text: #f0f6fc;
      --muted: #8b949e;
      --green: #3fb950;
      --blue: #58a6ff;
      --purple: #bc8cff;
      --gradient: linear-gradient(135deg, #58a6ff, #bc8cff);
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family:
        Inter, -apple-system, BlinkMacSystemFont, "Segoe UI",
        Roboto, Helvetica, Arial, sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: min(1100px, 92%);
      margin: auto;
    }

    /* NAVIGATION */

    nav {
      position: sticky;
      top: 0;
      z-index: 100;
      background: rgba(13, 17, 23, 0.88);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid var(--border);
    }

    .nav-inner {
      height: 70px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .logo {
      font-size: 1.2rem;
      font-weight: 800;
      letter-spacing: -0.5px;
    }

    .logo span {
      color: var(--green);
    }

    .nav-links {
      display: flex;
      gap: 28px;
      list-style: none;
    }

    .nav-links a {
      color: var(--muted);
      font-size: 0.95rem;
      transition: 0.2s;
    }

    .nav-links a:hover {
      color: var(--text);
    }

    /* HERO */

    .hero {
      min-height: 720px;
      display: flex;
      align-items: center;
      position: relative;
      overflow: hidden;
    }

    .hero::before {
      content: "";
      position: absolute;
      width: 500px;
      height: 500px;
      background: #58a6ff;
      opacity: 0.08;
      filter: blur(120px);
      border-radius: 50%;
      top: 100px;
      right: -100px;
    }

    .hero-content {
      position: relative;
      z-index: 2;
      max-width: 850px;
    }

    .badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 7px 13px;
      border: 1px solid var(--border);
      border-radius: 999px;
      color: var(--green);
      background: rgba(63, 185, 80, 0.06);
      margin-bottom: 25px;
      font-size: 0.9rem;
    }

    .status-dot {
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background: var(--green);
      box-shadow: 0 0 12px var(--green);
    }

    h1 {
      font-size: clamp(3.3rem, 8vw, 6.5rem);
      line-height: 0.95;
      letter-spacing: -5px;
      margin-bottom: 25px;
    }

    .gradient-text {
      background: var(--gradient);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }

    .hero p {
      color: var(--muted);
      font-size: 1.25rem;
      max-width: 680px;
      margin-bottom: 35px;
    }

    .buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 14px;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      padding: 12px 20px;
      border-radius: 8px;
      font-weight: 700;
      border: 1px solid var(--border);
      transition: 0.25s;
    }

    .btn-primary {
      background: var(--text);
      color: #0d1117;
    }

    .btn-primary:hover {
      transform: translateY(-2px);
      box-shadow: 0 10px 30px rgba(255,255,255,0.08);
    }

    .btn-secondary {
      color: var(--text);
      background: var(--bg-light);
    }

    .btn-secondary:hover {
      border-color: var(--blue);
      color: var(--blue);
    }

    /* TERMINAL */

    .terminal {
      margin-top: 70px;
      background: #010409;
      border: 1px solid var(--border);
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 30px 80px rgba(0,0,0,0.35);
    }

    .terminal-header {
      display: flex;
      align-items: center;
      gap: 7px;
      padding: 12px 15px;
      border-bottom: 1px solid var(--border);
      background: #161b22;
    }

    .terminal-dot {
      width: 11px;
      height: 11px;
      border-radius: 50%;
    }

    .red { background: #ff5f56; }
    .yellow { background: #ffbd2e; }
    .green { background: #27c93f; }

    .terminal-body {
      padding: 25px;
      font-family: "Courier New", monospace;
      color: #c9d1d9;
      overflow-x: auto;
    }

    .prompt {
      color: var(--green);
    }

    .command {
      color: var(--blue);
    }

    /* SECTIONS */

    section {
      padding: 100px 0;
    }

    .section-label {
      color: var(--green);
      font-family: monospace;
      margin-bottom: 10px;
      font-size: 0.95rem;
    }

    h2 {
      font-size: clamp(2rem, 5vw, 3.3rem);
      letter-spacing: -2px;
      margin-bottom: 15px;
    }

    .section-description {
      color: var(--muted);
      max-width: 650px;
      margin-bottom: 45px;
    }

    /* STATS */

    .stats {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 15px;
      margin-top: 50px;
    }

    .stat {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 25px;
      text-align: center;
    }

    .stat strong {
      display: block;
      font-size: 2rem;
      color: var(--text);
    }

    .stat span {
      color: var(--muted);
      font-size: 0.9rem;
    }

    /* PROJECTS */

    .projects {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .project {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 25px;
      transition: 0.3s;
    }

    .project:hover {
      transform: translateY(-6px);
      border-color: #58a6ff;
      box-shadow: 0 15px 40px rgba(0,0,0,0.25);
    }

    .project-icon {
      font-size: 1.8rem;
      margin-bottom: 20px;
    }

    .project h3 {
      margin-bottom: 10px;
    }

    .project p {
      color: var(--muted);
      font-size: 0.93rem;
      margin-bottom: 20px;
    }

    .tags {
      display: flex;
      flex-wrap: wrap;
      gap: 7px;
    }

    .tag {
      color: var(--blue);
      background: rgba(88,166,255,0.1);
      padding: 4px 8px;
      border-radius: 5px;
      font-size: 0.75rem;
      font-family: monospace;
    }

    /* SKILLS */

    .skills {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 18px;
    }

    .skill {
      padding: 20px;
      border: 1px solid var(--border);
      background: var(--card);
      border-radius: 10px;
    }

    .skill-top {
      display: flex;
      justify-content: space-between;
      margin-bottom: 12px;
    }

    .skill-top span:last-child {
      color: var(--muted);
      font-family: monospace;
    }

    .bar {
      height: 7px;
      background: #21262d;
      border-radius: 20px;
      overflow: hidden;
    }

    .bar span {
      display: block;
      height: 100%;
      background: var(--gradient);
      border-radius: inherit;
    }

    /* ABOUT */

    .about-grid {
      display: grid;
      grid-template-columns: 1.2fr 0.8fr;
      gap: 50px;
      align-items: center;
    }

    .about-text p {
      color: var(--muted);
      margin-bottom: 18px;
      font-size: 1.05rem;
    }

    .highlight {
      color: var(--text);
      font-weight: 700;
    }

    .code-card {
      background: #010409;
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 25px;
      font-family: monospace;
      color: #c9d1d9;
    }

    .code-card .key {
      color: #ff7b72;
    }

    .code-card .value {
      color: #a5d6ff;
    }

    /* CTA */

    .cta {
      text-align: center;
      padding: 100px 30px;
      border: 1px solid var(--border);
      border-radius: 18px;
      background:
        radial-gradient(circle at center, rgba(88,166,255,0.1), transparent 55%),
        var(--card);
    }

    .cta p {
      color: var(--muted);
      max-width: 600px;
      margin: 0 auto 30px;
    }

    /* FOOTER */

    footer {
      border-top: 1px solid var(--border);
      padding: 30px 0;
      color: var(--muted);
    }

    .footer-inner {
      display: flex;
      justify-content: space-between;
      gap: 20px;
    }

    /* MOBILE */

    @media (max-width: 800px) {
      .nav-links {
        display: none;
      }

      h1 {
        letter-spacing: -3px;
      }

      .stats,
      .projects {
        grid-template-columns: 1fr 1fr;
      }

      .about-grid {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 550px) {
      .hero {
        min-height: 620px;
      }

      section {
        padding: 70px 0;
      }

      .stats,
      .projects,
      .skills {
        grid-template-columns: 1fr;
      }

      .footer-inner {
        flex-direction: column;
      }
    }
  </style>
</head>

<body>

  <!-- NAVIGATION -->
  <nav>
    <div class="container nav-inner">
      <a href="#" class="logo">Jake<span>M</span>.dev</a>

      <ul class="nav-links">
        <li><a href="#about">About</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </div>
  </nav>

  <!-- HERO -->
  <main>
    <section class="hero">
      <div class="container">
        <div class="hero-content">

          <div class="badge">
            <span class="status-dot"></span>
            Available for new projects
          </div>

          <h1>
            Jake M.<br />
            <span class="gradient-text">Builds the future.</span>
          </h1>

          <p>
            Software developer, problem solver, and technology enthusiast.
            Jake turns complex ideas into fast, reliable, and beautiful
            digital experiences.
          </p>

          <div class="buttons">
            <a href="#projects" class="btn btn-primary">
              View Projects →
            </a>

            <a href="https://github.com/" target="_blank" class="btn btn-secondary">
              GitHub ↗
            </a>
          </div>

          <!-- TERMINAL -->
          <div class="terminal">
            <div class="terminal-header">
              <span class="terminal-dot red"></span>
              <span class="terminal-dot yellow"></span>
              <span class="terminal-dot green"></span>
            </div>

            <div class="terminal-body">
              <div>
                <span class="prompt">jake@dev</span>:~$ 
                <span class="command">whoami</span>
              </div>

              <div>Jake M — Developer & Problem Solver</div>
              <br />

              <div>
                <span class="prompt">jake@dev</span>:~$ 
                <span class="command">npm run build</span>
              </div>

              <div>✓ Turning ideas into products...</div>
              <div>✓ Writing clean code...</div>
              <div>✓ Solving difficult problems...</div>
              <div>✓ Shipping something great.</div>
            </div>
          </div>

        </div>
      </div>
    </section>

    <!-- ABOUT -->
    <section id="about">
      <div class="container">

        <div class="section-label">// ABOUT_JAKE</div>

        <div class="about-grid">

          <div class="about-text">
            <h2>A developer who thinks beyond the code.</h2>

            <p>
              Jake M is focused on building software that is not only
              functional, but fast, intuitive, and enjoyable to use.
            </p>

            <p>
              From ambitious side projects to production-ready applications,
              Jake approaches every challenge with <span class="highlight">
              curiosity, precision, and persistence.</span>
            </p>

            <p>
              The goal is simple: write better software, learn something new,
              and leave every project better than it started.
            </p>
          </div>

          <div class="code-card">
<pre>{
  <span class="key">"name"</span>:
    <span class="value">"Jake M"</span>,

  <span class="key">"role"</span>:
    <span class="value">"Software Developer"</span>,

  <span class="key">"focus"</span>: [
    <span class="value">"Web Development"</span>,
    <span class="value">"AI & Automation"</span>,
    <span class="value">"Open Source"</span>
  ],

  <span class="key">"mindset"</span>:
    <span class="value">"Build. Learn. Improve."</span>
}</pre>
          </div>

        </div>

        <div class="stats">
          <div class="stat">
            <strong>50+</strong>
            <span>Projects Built</span>
          </div>

          <div class="stat">
            <strong>10K+</strong>
            <span>Lines of Code</span>
          </div>

          <div class="stat">
            <strong>15+</strong>
            <span>Technologies</span>
          </div>

          <div class="stat">
            <strong>∞</strong>
            <span>Ideas to Build</span>
          </div>
        </div>

      </div>
    </section>

    <!-- PROJECTS -->
    <section id="projects">
      <div class="container">

        <div class="section-label">// FEATURED_WORK</div>

        <h2>Things Jake has built.</h2>

        <p class="section-description">
          A selection of fictional showcase projects demonstrating Jake's
          approach to modern software development.
        </p>

        <div class="projects">

          <article class="project">
            <div class="project-icon">⚡</div>
            <h3>Pulse AI</h3>
            <p>
              An intelligent productivity platform designed to automate
              repetitive workflows and help teams work smarter.
            </p>

            <div class="tags">
              <span class="tag">JavaScript</span>
              <span class="tag">AI</span>
              <span class="tag">Node.js</span>
            </div>
          </article>

          <article class="project">
            <div class="project-icon">🚀</div>
            <h3>LaunchPad</h3>
            <p>
              A developer-focused dashboard for monitoring projects,
              deployments, performance, and application health.
            </p>

            <div class="tags">
              <span class="tag">React</span>
              <span class="tag">API</span>
              <span class="tag">Cloud</span>
            </div>
          </article>

          <article class="project">
            <div class="project-icon">🔐</div>
            <h3>Vault</h3>
            <p>
              A modern security-focused application concept built around
              privacy, simplicity, and reliable data management.
            </p>

            <div class="tags">
              <span class="tag">Python</span>
              <span class="tag">Security</span>
              <span class="tag">SQL</span>
            </div>
          </article>

          <article class="project">
            <div class="project-icon">🌎</div>
            <h3>OpenWorld</h3>
            <p>
              An open-source platform concept connecting developers to
              collaborative coding projects.
            </p>

            <div class="tags">
              <span class="tag">Open Source</span>
              <span class="tag">Git</span>
              <span class="tag">React</span>
            </div>
          </article>

          <article class="project">
            <div class="project-icon">📊</div>
            <h3>DataFlow</h3>
            <p>
              A clean analytics dashboard concept for turning complicated
              datasets into useful visual insights.
            </p>

            <div class="tags">
              <span class="tag">Python</span>
              <span class="tag">Data</span>
              <span class="tag">Charts</span>
            </div>
          </article>

          <article class="project">
            <div class="project-icon">🤖</div>
            <h3>CodePilot</h3>
            <p>
              An experimental developer assistant concept designed to make
              everyday coding faster and more productive.
            </p>

            <div class="tags">
              <span class="tag">AI</span>
              <span class="tag">TypeScript</span>
              <span class="tag">Automation</span>
            </div>
          </article>

        </div>
      </div>
    </section>

    <!-- SKILLS -->
    <section id="skills">
      <div class="container">

        <div class="section-label">// TECH_STACK</div>

        <h2>Tools of the trade.</h2>

        <p class="section-description">
          A fictional showcase of Jake's core development strengths.
        </p>

        <div class="skills">

          <div class="skill">
            <div class="skill-top">
              <span>JavaScript / TypeScript</span>
              <span>95%</span>
            </div>
            <div class="bar">
              <span style="width:95%"></span>
            </div>
          </div>

          <div class="skill">
            <div class="skill-top">
              <span>Python</span>
              <span>92%</span>
            </div>
            <div class="bar">
              <span style="width:92%"></span>
            </div>
          </div>

          <div class="skill">
            <div class="skill-top">
              <span>React</span>
              <span>94%</span>
            </div>
            <div class="bar">
              <span style="width:94%"></span>
            </div>
          </div>

          <div class="skill">
            <div class="skill-top">
              <span>Node.js</span>
              <span>90%</span>
            </div>
            <div class="bar">
              <span style="width:90%"></span>
            </div>
          </div>

          <div class="skill">
            <div class="skill-top">
              <span>Git & GitHub</span>
              <span>98%</span>
            </div>
            <div class="bar">
              <span style="width:98%"></span>
            </div>
          </div>

          <div class="skill">
            <div class="skill-top">
              <span>Problem Solving</span>
              <span>99%</span>
            </div>
            <div class="bar">
              <span style="width:99%"></span>
            </div>
          </div>

        </div>
      </div>
    </section>

    <!-- CTA -->
    <section id="contact">
      <div class="container">

        <div class="cta">
          <div class="section-label">// LET'S_BUILD</div>

          <h2>Have an idea?</h2>

          <p>
            Great software starts with a good idea. Jake's next project
            could be the one that turns yours into something real.
          </p>

          <div class="buttons" style="justify-content:center;">
            <a
              href="https://github.com/"
              target="_blank"
              class="btn btn-primary"
            >
              Visit GitHub →
            </a>

            <a
              href="mailto:hello@example.com"
              class="btn btn-secondary"
            >
              Get in Touch
            </a>
          </div>
        </div>

      </div>
    </section>

  </main>

  <!-- FOOTER -->
  <footer>
    <div class="container footer-inner">
      <span>© 2026 Jake M. Built with code.</span>
      <span>GitHub • Open Source • Innovation</span>
    </div>
  </footer>

</body>
</html>