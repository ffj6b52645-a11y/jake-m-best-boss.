<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <title>Jake M. — The One Who Shows Up</title>

  <meta
    name="description"
    content="The story of Jake M., a fictional hero defined by courage, compassion, and resolve."
  />

  <style>
    :root {
      --bg: #070b12;
      --bg-light: #101827;
      --card: rgba(255, 255, 255, 0.06);
      --card-border: rgba(255, 255, 255, 0.12);
      --text: #f5f7fb;
      --muted: #aab4c4;
      --accent: #f4b942;
      --accent-light: #ffd778;
      --blue: #5da9ff;
      --max-width: 1180px;
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
        Inter,
        ui-sans-serif,
        system-ui,
        -apple-system,
        BlinkMacSystemFont,
        "Segoe UI",
        sans-serif;

      background:
        radial-gradient(
          circle at 20% 10%,
          rgba(93, 169, 255, 0.12),
          transparent 35%
        ),
        radial-gradient(
          circle at 80% 30%,
          rgba(244, 185, 66, 0.09),
          transparent 35%
        ),
        var(--bg);

      color: var(--text);
      line-height: 1.6;
      overflow-x: hidden;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    img {
      max-width: 100%;
      display: block;
    }

    section {
      padding: 110px 20px;
    }

    .container {
      width: min(var(--max-width), 100%);
      margin: auto;
    }

    /* =========================
       NAVIGATION
    ========================= */

    .nav {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 1000;

      background: rgba(7, 11, 18, 0.75);
      backdrop-filter: blur(16px);

      border-bottom: 1px solid rgba(255, 255, 255, 0.08);
    }

    .nav-inner {
      width: min(var(--max-width), calc(100% - 40px));
      margin: auto;

      height: 72px;

      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .logo {
      font-size: 1.2rem;
      font-weight: 900;
      letter-spacing: -0.03em;
    }

    .logo span {
      color: var(--accent);
    }

    .nav-links {
      display: flex;
      gap: 28px;
      list-style: none;
    }

    .nav-links a {
      color: var(--muted);
      font-size: 0.9rem;
      font-weight: 600;
      transition: 0.25s ease;
    }

    .nav-links a:hover {
      color: white;
    }

    /* =========================
       HERO
    ========================= */

    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;

      position: relative;
      overflow: hidden;

      padding-top: 120px;
    }

    .hero::before {
      content: "";

      position: absolute;
      inset: 0;

      background:
        linear-gradient(
          90deg,
          rgba(7, 11, 18, 0.98) 0%,
          rgba(7, 11, 18, 0.8) 45%,
          rgba(7, 11, 18, 0.3) 100%
        );

      z-index: 1;
    }

    .hero-glow {
      position: absolute;
      width: 600px;
      height: 600px;

      right: -200px;
      top: 50%;

      transform: translateY(-50%);

      background: rgba(244, 185, 66, 0.12);
      filter: blur(100px);
      border-radius: 50%;
    }

    .hero-content {
      position: relative;
      z-index: 2;

      width: min(var(--max-width), 100%);
      margin: auto;

      padding: 0 20px;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 8px;

      color: var(--accent);
      font-size: 0.78rem;
      font-weight: 800;

      letter-spacing: 0.16em;
      text-transform: uppercase;

      margin-bottom: 24px;
    }

    .eyebrow::before {
      content: "";

      width: 30px;
      height: 2px;

      background: var(--accent);
    }

    .hero h1 {
      max-width: 850px;

      font-size: clamp(4rem, 10vw, 8.5rem);
      line-height: 0.86;

      letter-spacing: -0.075em;
      font-weight: 950;

      margin-bottom: 35px;
    }

    .hero h1 span {
      color: var(--accent);
    }

    .hero-description {
      max-width: 620px;

      color: #c7cfdb;
      font-size: 1.15rem;

      margin-bottom: 35px;
    }

    .hero-buttons {
      display: flex;
      gap: 14px;
      flex-wrap: wrap;
    }

    .button {
      display: inline-flex;
      align-items: center;
      justify-content: center;

      padding: 14px 22px;

      border-radius: 999px;

      font-weight: 800;
      font-size: 0.9rem;

      transition:
        transform 0.25s ease,
        background 0.25s ease;
    }

    .button:hover {
      transform: translateY(-3px);
    }

    .button-primary {
      background: var(--accent);
      color: #111;
    }

    .button-primary:hover {
      background: var(--accent-light);
    }

    .button-secondary {
      border: 1px solid rgba(255, 255, 255, 0.16);
      background: rgba(255, 255, 255, 0.04);
    }

    .button-secondary:hover {
      background: rgba(255, 255, 255, 0.09);
    }

    .fiction-note {
      margin-top: 28px;

      color: #7e8a9d;
      font-size: 0.78rem;

      max-width: 520px;
    }

    /* =========================
       SECTION HEADERS
    ========================= */

    .section-header {
      max-width: 720px;
      margin-bottom: 55px;
    }

    .section-label {
      color: var(--accent);

      text-transform: uppercase;
      letter-spacing: 0.15em;

      font-size: 0.75rem;
      font-weight: 900;

      margin-bottom: 14px;
    }

    .section-header h2 {
      font-size: clamp(2.5rem, 6vw, 5rem);
      line-height: 0.95;
      letter-spacing: -0.06em;

      margin-bottom: 20px;
    }

    .section-header p {
      color: var(--muted);
      font-size: 1.05rem;
    }

    /* =========================
       STORY
    ========================= */

    .story-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 60px;

      align-items: center;
    }

    .story-text p {
      color: #bdc7d5;
      margin-bottom: 20px;
      font-size: 1.05rem;
    }

    .quote {
      border-left: 3px solid var(--accent);

      padding: 25px 0 25px 25px;

      font-size: 1.5rem;
      font-weight: 700;

      color: white;
    }

    .portrait {
      position: relative;

      border-radius: 30px;
      overflow: hidden;

      border: 1px solid var(--card-border);

      background: #101723;

      min-height: 500px;

      display: flex;
      align-items: center;
      justify-content: center;
    }

    .portrait::after {
      content: "";

      position: absolute;
      inset: 0;

      background:
        linear-gradient(
          180deg,
          transparent 40%,
          rgba(7, 11, 18, 0.75)
        );
    }

    .portrait svg {
      width: 100%;
      height: 100%;
      min-height: 500px;
    }

    /* =========================
       VALUES
    ========================= */

    .values {
      background:
        linear-gradient(
          180deg,
          transparent,
          rgba(255, 255, 255, 0.025),
          transparent
        );
    }

    .value-grid {
      display: grid;

      grid-template-columns: repeat(3, 1fr);

      gap: 18px;
    }

    .value-card {
      padding: 35px;

      border-radius: 24px;

      border: 1px solid var(--card-border);

      background: var(--card);

      transition:
        transform 0.3s ease,
        border-color 0.3s ease;
    }

    .value-card:hover {
      transform: translateY(-8px);
      border-color: rgba(244, 185, 66, 0.4);
    }

    .value-number {
      color: var(--accent);

      font-size: 0.75rem;
      font-weight: 900;

      letter-spacing: 0.15em;

      margin-bottom: 50px;
    }

    .value-card h3 {
      font-size: 1.6rem;
      margin-bottom: 12px;
    }

    .value-card p {
      color: var(--muted);
    }

    /* =========================
       TIMELINE
    ========================= */

    .timeline {
      max-width: 900px;
    }

    .timeline-item {
      display: grid;

      grid-template-columns: 150px 1fr;

      gap: 35px;

      padding: 35px 0;

      border-top: 1px solid rgba(255, 255, 255, 0.1);
    }

    .timeline-year {
      color: var(--accent);

      font-size: 0.85rem;
      font-weight: 900;

      letter-spacing: 0.1em;
    }

    .timeline-item h3 {
      font-size: 1.5rem;
      margin-bottom: 8px;
    }

    .timeline-item p {
      color: var(--muted);
    }

    /* =========================
       GALLERY
    ========================= */

    .gallery-grid {
      display: grid;

      grid-template-columns: 1.3fr 1fr;

      gap: 18px;
    }

    .gallery-card {
      min-height: 400px;

      border-radius: 26px;

      overflow: hidden;

      border: 1px solid var(--card-border);

      background: #0e1520;

      position: relative;
    }

    .gallery-card:first-child {
      min-height: 600px;
    }

    .gallery-card svg {
      width: 100%;
      height: 100%;
    }

    .gallery-label {
      position: absolute;

      left: 22px;
      bottom: 20px;

      padding: 9px 13px;

      border-radius: 999px;

      background: rgba(7, 11, 18, 0.75);
      backdrop-filter: blur(10px);

      font-size: 0.75rem;
      font-weight: 800;

      border: 1px solid rgba(255, 255, 255, 0.1);
    }

    /* =========================
       VIDEO
    ========================= */

    .video-section {
      background: #05080d;
    }

    .video-grid {
      display: grid;

      grid-template-columns: repeat(2, 1fr);

      gap: 20px;
    }

    .video-card {
      background: #0d131c;

      border: 1px solid var(--card-border);

      border-radius: 24px;

      overflow: hidden;
    }

    .video-card video {
      width: 100%;
      aspect-ratio: 16 / 9;

      display: block;

      background: black;
    }

    .video-info {
      padding: 22px;
    }

    .video-info h3 {
      margin-bottom: 7px;
    }

    .video-info p {
      color: var(--muted);
      font-size: 0.9rem;
    }

    /* =========================
       CTA
    ========================= */

    .cta {
      text-align: center;
    }

    .cta-box {
      border-radius: 35px;

      padding: 90px 30px;

      background:
        radial-gradient(
          circle at 50% 0%,
          rgba(244, 185, 66, 0.18),
          transparent 45%
        ),
        rgba(255, 255, 255, 0.04);

      border: 1px solid var(--card-border);
    }

    .cta-box h2 {
      font-size: clamp(2.8rem, 7vw, 6rem);

      line-height: 0.9;

      letter-spacing: -0.07em;

      margin-bottom: 25px;
    }

    .cta-box p {
      max-width: 600px;

      margin: 0 auto 30px;

      color: var(--muted);
    }

    /* =========================
       FOOTER
    ========================= */

    footer {
      padding: 35px 20px;

      border-top: 1px solid rgba(255, 255, 255, 0.08);

      color: #718096;

      font-size: 0.8rem;
    }

    .footer-inner {
      width: min(var(--max-width), 100%);
      margin: auto;

      display: flex;

      justify-content: space-between;
      align-items: center;

      gap: 20px;
    }

    /* =========================
       ANIMATIONS
    ========================= */

    @keyframes fadeUp {
      from {
        opacity: 0;
        transform: translateY(30px);
      }

      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .hero-content {
      animation: fadeUp 1s ease both;
    }

    /* =========================
       MOBILE
    ========================= */

    @media (max-width: 800px) {
      section {
        padding: 80px 18px;
      }

      .nav-inner {
        width: calc(100% - 30px);
      }

      .nav-links {
        gap: 13px;
      }

      .nav-links a {
        font-size: 0.72rem;
      }

      .hero {
        min-height: 90vh;
      }

      .hero h1 {
        font-size: clamp(3.5rem, 18vw, 6rem);
      }

      .story-grid {
        grid-template-columns: 1fr;
      }

      .portrait {
        min-height: 400px;
      }

      .portrait svg {
        min-height: 400px;
      }

      .value-grid {
        grid-template-columns: 1fr;
      }

      .timeline-item {
        grid-template-columns: 1fr;
        gap: 8px;
      }

      .gallery-grid {
        grid-template-columns: 1fr;
      }

      .gallery-card,
      .gallery-card:first-child {
        min-height: 420px;
      }

      .video-grid {
        grid-template-columns: 1fr;
      }

      .footer-inner {
        flex-direction: column;
        text-align: center;
      }
    }
  </style>
</head>

<body>

  <!-- =========================
       NAVIGATION
  ========================== -->

  <nav class="nav">
    <div class="nav-inner">

      <a href="#top" class="logo">
        JAKE<span>M.</span>
      </a>

      <ul class="nav-links">
        <li>
          <a href="#story">Story</a>
        </li>

        <li>
          <a href="#values">Values</a>
        </li>

        <li>
          <a href="#moments">Moments</a>
        </li>

        <li>
          <a href="#reel">Reel</a>
        </li>
      </ul>

    </div>
  </nav>


  <!-- =========================
       HERO
  ========================== -->

  <main id="top">

    <section class="hero">

      <div class="hero-glow"></div>

      <div class="hero-content">

        <div class="eyebrow">
          The story of a modern hero
        </div>

        <h1>
          Jake M.<br>
          <span>Shows Up.</span>
        </h1>

        <p class="hero-description">
          He doesn't wear a cape. He doesn't wait for permission.
          When someone needs help, Jake M. is already moving.
        </p>

        <div class="hero-buttons">

          <a href="#story" class="button button-primary">
            Discover His Story
          </a>

          <a href="#reel" class="button button-secondary">
            Watch the Reel
          </a>

        </div>

        <p class="fiction-note">
          Fictional character and AI concept website. The stories,
          artwork, and events presented here are creative fiction.
        </p>

      </div>

    </section>


    <!-- =========================
         STORY
    ========================== -->

    <section id="story">

      <div class="container">

        <div class="section-header">

          <div class="section-label">
            The Story
          </div>

          <h2>
            Heroism isn't a title.
          </h2>

          <p>
            It's what you do when nobody is watching.
          </p>

        </div>


        <div class="story-grid">

          <div class="story-text">

            <p>
              Jake M. is the kind of person who notices what everyone
              else walks past. A stranger struggling with a heavy box.
              A kid standing alone. A neighbor who needs someone to
              knock on the door and ask, "Are you okay?"
            </p>

            <p>
              His greatest strength isn't physical power. It's the
              decision to act when action matters.
            </p>

            <p>
              Jake believes that courage doesn't always look dramatic.
              Sometimes courage is simply being the person who stays.
            </p>

            <div class="quote">
              "You don't have to be fearless.
              You just have to move forward."
            </div>

          </div>


          <div class="portrait">

            <!-- AI-STYLE SVG PORTRAIT -->

            <svg
              viewBox="0 0 600 700"
              xmlns="http://www.w3.org/2000/svg"
              role="img"
              aria-label="AI concept portrait of fictional hero Jake M."
            >

              <defs>

                <linearGradient
                  id="portraitBackground"
                  x1="0"
                  y1="0"
                  x2="1"
                  y2="1"
                >
                  <stop offset="0%" stop-color="#17263a"/>
                  <stop offset="55%" stop-color="#0c1625"/>
                  <stop offset="100%" stop-color="#05080d"/>
                </linearGradient>

                <linearGradient
                  id="jacket"
                  x1="0"
                  y1="0"
                  x2="1"
                  y2="1"
                >
                  <stop offset="0%" stop-color="#25364b"/>
                  <stop offset="100%" stop-color="#0c131d"/>
                </linearGradient>

                <radialGradient id="light">
                  <stop offset="0%" stop-color="#ffd986"/>
                  <stop offset="100%" stop-color="#d58e2e"/>
                </radialGradient>

              </defs>

              <rect
                width="600"
                height="700"
                fill="url(#portraitBackground)"
              />

              <circle
                cx="470"
                cy="120"
                r="160"
                fill="url(#light)"
                opacity="0.15"
              />

              <!-- shoulders -->

              <path
                d="M80 700
                   C105 555 180 500 300 500
                   C420 500 495 555 520 700Z"
                fill="url(#jacket)"
              />

              <!-- neck -->

              <path
                d="M255 430 L255 520
                         Q300 550 345 520
                         L345 430Z"
                fill="#9b694c"
              />

              <!-- face -->

              <path
                d="M190 175
                         Q300 80 410 175
                         L395 350
                         Q370 445 300 470
                         Q230 445 205 350Z"
                fill="#b97956"
              />

              <!-- hair -->

              <path
                d="M190 220
                         Q165 120 245 80
                         Q340 30 415 115
                         Q430 155 405 220
                         Q375 170 345 150
                         Q285 180 190 220Z"
                fill="#11161e"
              />

              <!-- ear -->

              <ellipse
                cx="195"
                cy="290"
                rx="22"
                ry="38"
                fill="#a66e50"
              />

              <ellipse
                cx="405"
                cy="290"
                rx="22"
                ry="38"
                fill="#a66e50"
              />

              <!-- eyes -->

              <ellipse
                cx="250"
                cy="280"
                rx="15"
                ry="9"
                fill="#10151c"
              />

              <ellipse
                cx="350"
                cy="280"
                rx="15"
                ry="9"
                fill="#10151c"
              />

              <!-- eyebrows -->

              <path
                d="M225 250 Q250 235 275 250"
                fill="none"
                stroke="#211817"
                stroke-width="10"
                stroke-linecap="round"
              />

              <path
                d="M325 250 Q350 235 375 250"
                fill="none"
                stroke="#211817"
                stroke-width="10"
                stroke-linecap="round"
              />

              <!-- nose -->

              <path
                d="M300 285 L285 345 Q300 355 315 345"
                fill="none"
                stroke="#85533e"
                stroke-width="8"
                stroke-linecap="round"
              />

              <!-- mouth -->

              <path
                d="M265 380 Q300 400 335 380"
                fill="none"
                stroke="#5e342c"
                stroke-width="7"
                stroke-linecap="round"
              />

              <!-- shirt -->

              <path
                d="M240 510 L300 565 L360 510
                         L410 700 L190 700Z"
                fill="#101923"
              />

              <!-- jacket seams -->

              <path
                d="M120 700 L205 530"
                stroke="#496077"
                stroke-width="7"
                opacity="0.7"
              />

              <path
                d="M480 700 L395 530"
                stroke="#496077"
                stroke-width="7"
                opacity="0.7"
              />

              <!-- small hero emblem -->

              <path
                d="M300 550 L322 592 L300 625 L278 592Z"
                fill="#f4b942"
              />

            </svg>

          </div>

        </div>

      </div>

    </section>


    <!-- =========================
         VALUES
    ========================== -->

    <section id="values" class="values">

      <div class="container">

        <div class="section-header">

          <div class="section-label">
            What Defines Him
          </div>

          <h2>
            Three things matter.
          </h2>

          <p>
            Jake's philosophy is simple enough to remember
            and difficult enough to live.
          </p>

        </div>


        <div class="value-grid">

          <article class="value-card">

            <div class="value-number">
              01 — COURAGE
            </div>

            <h3>
              Move toward the problem.
            </h3>

            <p>
              Fear is allowed. Standing still isn't.
              Jake believes courage begins the moment
              you decide someone needs you.
            </p>

          </article>


          <article class="value-card">

            <div class="value-number">
              02 — COMPASSION
            </div>

            <h3>
              See the person.
            </h3>

            <p>
              Every problem has a human being behind it.
              Jake listens first and helps second.
            </p>

          </article>


          <article class="value-card">

            <div class="value-number">
              03 — RESOLVE
            </div>

            <h3>
              Finish what you start.
            </h3>

            <p>
              When the easy choice is to walk away,
              Jake stays until the job is done.
            </p>

          </article>

        </div>

      </div>

    </section>


    <!-- =========================
         MOMENTS
    ========================== -->

    <section id="moments">

      <div class="container">

        <div class="section-header">

          <div class="section-label">
            Heroic Moments
          </div>

          <h2>
            The moments that define him.
          </h2>

          <p>
            Small decisions can create enormous consequences.
          </p>

        </div>


        <div class="timeline">

          <div class="timeline-item">

            <div class="timeline-year">
              06:42 AM
            </div>

            <div>

              <h3>
                The Empty Highway
              </h3>

              <p>
                Jake spots a stranded driver on an empty
                highway before sunrise. He pulls over,
                calls for help, and stays until the tow truck arrives.
              </p>

            </div>

          </div>


          <div class="timeline-item">

            <div class="timeline-year">
              12:18 PM
            </div>

            <div>

              <h3>
                The Lost Kid
              </h3>

              <p>
                At a crowded community festival, Jake notices
                a frightened child searching through the crowd.
                He stays calm and helps reunite the child with family.
              </p>

            </div>

          </div>


          <div class="timeline-item">

            <div class="timeline-year">
              09:37 PM
            </div>

            <div>

              <h3>
                The Last Light
              </h3>

              <p>
                When a neighborhood loses power during a storm,
                Jake organizes volunteers, checks on elderly neighbors,
                and makes sure everyone has what they need.
              </p>

            </div>

          </div>


          <div class="timeline-item">

            <div class="timeline-year">
              02:11 AM
            </div>

            <div>

              <h3>
                The Choice
              </h3>

              <p>
                The hardest moments are rarely the loudest.
                Sometimes being a hero means answering the phone
                when everyone else has gone to sleep.
              </p>

            </div>

          </div>

        </div>

      </div>

    </section>


    <!-- =========================
         AI ART GALLERY
    ========================== -->

    <section>

      <div class="container">

        <div class="section-header">

          <div class="section-label">
            Visual Archive
          </div>

          <h2>
            A hero in two frames.
          </h2>

          <p>
            Original AI-style concept artwork created for this fictional
            character.
          </p>

        </div>


        <div class="gallery-grid">

          <!-- IMAGE 1 -->

          <div class="gallery-card">

            <svg
              viewBox="0 0 900 600"
              xmlns="http://www.w3.org/2000/svg"
              aria-label="AI concept artwork of Jake M. overlooking a city"
            >

              <defs>

                <linearGradient
                  id="citySky"
                  x1="0"
                  y1="0"
                  x2="0"
                  y2="1"
                >
                  <stop offset="0%" stop-color="#182d49"/>
                  <stop offset="60%" stop-color="#392d36"/>
                  <stop offset="100%" stop-color="#d08b4a"/>
                </linearGradient>

              </defs>

              <rect
                width="900"
                height="600"
                fill="url(#citySky)"
              />

              <!-- sun -->

              <circle
                cx="700"
                cy="210"
                r="90"
                fill="#ffd987"
                opacity="0.8"
              />

              <!-- skyline -->

              <path
                d="
                  M0 450
                  L0 370
                  L70 370
                  L70 420
                  L120 420
                  L120 320
                  L180 320
                  L180 410
                  L230 410
                  L230 280
                  L300 280
                  L300 410
                  L350 410
                  L350 340
                  L410 340
                  L410 390
                  L470 390
                  L470 260
                  L530 260
                  L530 410
                  L600 410
                  L600 310
                  L665 310
                  L665 410
                  L720 410
                  L720 290
                  L790 290
                  L790 400
                  L850 400
                  L850 340
                  L900 340
                  L900 600
                  L0 600Z
                "
                fill="#101724"
              />

              <!-- foreground hero silhouette -->

              <path
                d="
                  M365 600
                  C380 510 410 455 450 420
                  C490 455 520 510 535 600Z
                "
                fill="#080b11"
              />

              <circle
                cx="450"
                cy="385"
                r="48"
                fill="#080b11"
              />

              <path
                d="
                  M408 355
                  Q450 320
                  492 355
                  L480 375
                  Q450 350
                  420 375Z
                "
                fill="#05070a"
              />

              <!-- coat -->

              <path
                d="
                  M400 440
                  L450 500
                  L500 440
                  L535 600
                  L365 600Z
                "
                fill="#080b11"
              />

              <!-- moonlight -->

              <path
                d="
                  M450 337
                  L450 500
                "
                stroke="#ffd987"
                stroke-width="3"
                opacity="0.5"
              />

            </svg>

            <div class="gallery-label">
              Watchman — Concept I
            </div>

          </div>


          <!-- IMAGE 2 -->

          <div class="gallery-card">

            <svg
              viewBox="0 0 600 600"
              xmlns="http://www.w3.org/2000/svg"
              aria-label="AI concept artwork of fictional Jake M."
            >

              <defs>

                <linearGradient
                  id="night"
                  x1="0"
                  y1="0"
                  x2="1"
                  y2="1"
                >

                  <stop
                    offset="0%"
                    stop-color="#0c1728"
                  />

                  <stop
                    offset="100%"
                    stop-color="#020408"
                  />

                </linearGradient>

              </defs>

              <rect
                width="600"
                height="600"
                fill="url(#night)"
              />

              <!-- city lights -->

              <g
                fill="#f4b942"
                opacity="0.75"
              >

                <circle cx="80" cy="100" r="3"/>
                <circle cx="150" cy="180" r="3"/>
                <circle cx="230" cy="90" r="3"/>
                <circle cx="320" cy="140" r="3"/>
                <circle cx="450" cy="80" r="3"/>
                <circle cx="520" cy="180" r="3"/>
                <circle cx="390" cy="250" r="3"/>
                <circle cx="100" cy="310" r="3"/>

              </g>

              <!-- body -->

              <path
                d="
                  M110 600
                  C125 450 190 380 300 370
                  C410 380 475 450 490 600Z
                "
                fill="#111b29"
              />

              <!-- face -->

              <ellipse
                cx="300"
                cy="290"
                rx="90"
                ry="115"
                fill="#a96f51"
              />

              <!-- hair -->

              <path
                d="
                  M215 285
                  Q200 175
                  285 145
                  Q390 115
                  395 250
                  Q350 205
                  310 215
                  Q265 220
                  215 285Z
                "
                fill="#0a0d13"
              />

              <!-- eyes -->

              <circle
                cx="265"
                cy="290"
                r="7"
                fill="#111"
              />

              <circle
                cx="335"
                cy="290"
                r="7"
                fill="#111"
              />

              <!-- jaw shadow -->

              <path
                d="
                  M245 350
                  Q300 390
                  355 350
                "
                fill="none"
                stroke="#754938"
                stroke-width="8"
                stroke-linecap="round"
              />

              <!-- jacket -->

              <path
                d="
                  M205 420
                  L300 510
                  L395 420
                  L455 600
                  L145 600Z
                "
                fill="#182638"
              />

              <!-- emblem -->

              <path
                d="
                  M300 470
                  L325 515
                  L300 550
                  L275 515Z
                "
                fill="#f4b942"
              />

            </svg>

            <div class="gallery-label">
              After the Storm — Concept II
            </div>

          </div>

        </div>

      </div>

    </section>


    <!-- =========================
         VIDEO REEL
    ========================== -->

    <section id="reel" class="video-section">

      <div class="container">

        <div class="section-header">

          <div class="section-label">
            The Reel
          </div>

          <h2>
            See the story move.
          </h2>

          <p>
            These videos are demonstration clips. Replace them with
            your own footage or AI-generated videos when you're ready.
          </p>

        </div>


        <div class="video-grid">

          <!-- VIDEO 1 -->

          <article class="video-card">

            <video
              controls
              preload="metadata"
              poster=""
            >

              <source
                src="https://interactive-examples.mdn.mozilla.net/media/cc0-videos/flower.mp4"
                type="video/mp4"
              />

              Your browser does not support video playback.

            </video>

            <div class="video-info">

              <h3>
                Quiet Moments
              </h3>

              <p>
                A placeholder cinematic clip for the hero's visual reel.
              </p>

            </div>

          </article>


          <!-- VIDEO 2 -->

          <article class="video-card">

            <video
              controls
              preload="metadata"
            >

              <source
                src="https://www.w3schools.com/html/mov_bbb.mp4"
                type="video/mp4"
              />

              Your browser does not support video playback.

            </video>

            <div class="video-info">

              <h3>
                Keep Moving
              </h3>

              <p>
                Replace this demonstration video with your own hero footage.
              </p>

            </div>

          </article>

        </div>

      </div>

    </section>


    <!-- =========================
         FINAL CTA
    ========================== -->

    <section class="cta">

      <div class="container">

        <div class="cta-box">

          <h2>
            Be the person<br>
            who shows up.
          </h2>

          <p>
            Jake M. isn't a hero because he's perfect.
            He's a hero because when the moment arrives,
            he chooses to help.
          </p>

          <a
            href="#story"
            class="button button-primary"
          >
            Read His Story
          </a>

        </div>

      </div>

    </section>

  </main>


  <!-- =========================
       FOOTER
  ========================== -->

  <footer>

    <div class="footer-inner">

      <div>
        © 2026 Jake M. — Fictional Hero Concept
      </div>

      <div>
        Built as an AI concept website
      </div>

    </div>

  </footer>


  <!-- =========================
       SMALL JAVASCRIPT
  ========================== -->

  <script>

    // Smooth navigation for older browsers

    document.querySelectorAll('a[href^="#"]').forEach(link => {

      link.addEventListener("click", function(event) {

        const target = document.querySelector(
          this.getAttribute("href")
        );

        if (target) {

          event.preventDefault();

          target.scrollIntoView({
            behavior: "smooth",
            block: "start"
          });

        }

      });

    });


    // Add a subtle navigation effect when scrolling

    const nav = document.querySelector(".nav");

    window.addEventListener("scroll", () => {

      if (window.scrollY > 40) {

        nav.style.background =
          "rgba(4, 7, 12, 0.94)";

      } else {

        nav.style.background =
          "rgba(7, 11, 18, 0.75)";

      }

    });

  </script>

</body>
</html>