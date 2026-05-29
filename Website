<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>KUEL Conditioning — True Healing</title>
<link rel="manifest" href="manifest.json">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;1,400;1,600&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg:       #0e0f0d;
    --bg2:      #141510;
    --bg3:      #1a1c17;
    --gold:     #c9a84c;
    --gold-lt:  #e8c96b;
    --gold-dk:  #8a6f2e;
    --sage:     #7a9e7e;
    --sage-lt:  #a8c7ab;
    --cream:    #f0e9d6;
    --cream-dk: #c8bda0;
    --text:     #ede8df;
    --text-2:   #b0a992;
    --text-3:   #6b6555;
    --border:   rgba(201,168,76,0.18);
    --radius:   4px;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--bg);
    color: var(--text);
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* ── PAGE ROUTING ── */
  .page { display: none; }
  .page.active { display: block; }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 2.5rem;
    height: 70px;
    background: rgba(14,15,13,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 0.5px solid var(--border);
  }

  .nav-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 22px;
    font-weight: 600;
    color: var(--gold);
    cursor: pointer;
    letter-spacing: 0.05em;
    text-decoration: none;
  }
  .nav-logo span { color: var(--cream); }

  .nav-links { display: flex; gap: 2rem; list-style: none; }
  .nav-links a {
    font-size: 13px;
    font-weight: 400;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--text-2);
    text-decoration: none;
    cursor: pointer;
    transition: color 0.2s;
  }
  .nav-links a:hover,
  .nav-links a.active { color: var(--gold); }

  .nav-cta {
    font-size: 12px;
    font-weight: 500;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--bg);
    background: var(--gold);
    padding: 9px 20px;
    border-radius: var(--radius);
    text-decoration: none;
    cursor: pointer;
    transition: background 0.2s;
  }
  .nav-cta:hover { background: var(--gold-lt); }

  .nav-mobile-btn {
    display: none;
    flex-direction: column; gap: 5px; cursor: pointer; padding: 4px;
  }
  .nav-mobile-btn span {
    display: block; width: 22px; height: 1.5px;
    background: var(--text-2); transition: 0.2s;
  }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    display: flex; flex-direction: column;
    align-items: center; justify-content: center;
    padding: 8rem 2rem 4rem;
    position: relative;
    text-align: center;
    overflow: hidden;
  }

  .hero-bg {
    position: absolute; inset: 0;
    background:
      radial-gradient(ellipse 70% 60% at 50% 40%, rgba(201,168,76,0.07) 0%, transparent 70%),
      radial-gradient(ellipse 40% 40% at 20% 80%, rgba(122,158,126,0.06) 0%, transparent 60%),
      radial-gradient(ellipse 50% 50% at 80% 20%, rgba(122,158,126,0.04) 0%, transparent 60%);
  }

  .hero-symbol {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(80px, 12vw, 140px);
    font-weight: 400;
    font-style: italic;
    color: transparent;
    -webkit-text-stroke: 1px rgba(201,168,76,0.25);
    line-height: 1;
    margin-bottom: 1.5rem;
    letter-spacing: -0.02em;
    user-select: none;
  }

  .hero-eyebrow {
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 0.25em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 1.25rem;
  }

  .hero h1 {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(42px, 7vw, 80px);
    font-weight: 500;
    line-height: 1.08;
    color: var(--cream);
    margin-bottom: 1.5rem;
    max-width: 800px;
  }

  .hero h1 em {
    font-style: italic;
    color: var(--gold);
  }

  .hero-sub {
    font-size: 16px;
    font-weight: 300;
    line-height: 1.75;
    color: var(--text-2);
    max-width: 560px;
    margin-bottom: 2.5rem;
  }

  .hero-actions { display: flex; gap: 1rem; flex-wrap: wrap; justify-content: center; }

  .btn-primary {
    display: inline-flex; align-items: center; gap: 8px;
    background: var(--gold);
    color: var(--bg);
    font-size: 12px; font-weight: 500;
    letter-spacing: 0.1em; text-transform: uppercase;
    padding: 14px 28px;
    border-radius: var(--radius);
    text-decoration: none; cursor: pointer; border: none;
    transition: background 0.2s, transform 0.15s;
  }
  .btn-primary:hover { background: var(--gold-lt); transform: translateY(-1px); }

  .btn-ghost {
    display: inline-flex; align-items: center; gap: 8px;
    background: transparent;
    color: var(--cream-dk);
    font-size: 12px; font-weight: 500;
    letter-spacing: 0.1em; text-transform: uppercase;
    padding: 14px 28px;
    border-radius: var(--radius);
    border: 0.5px solid var(--border);
    text-decoration: none; cursor: pointer;
    transition: border-color 0.2s, color 0.2s;
  }
  .btn-ghost:hover { border-color: var(--gold); color: var(--gold); }

  .hero-scroll {
    position: absolute; bottom: 2.5rem; left: 50%; transform: translateX(-50%);
    display: flex; flex-direction: column; align-items: center; gap: 8px;
    color: var(--text-3);
    font-size: 10px; letter-spacing: 0.2em; text-transform: uppercase;
  }
  .hero-scroll::after {
    content: '';
    display: block; width: 1px; height: 40px;
    background: linear-gradient(to bottom, var(--gold-dk), transparent);
  }

  /* ── DIVIDER ── */
  .divider {
    width: 48px; height: 1px;
    background: linear-gradient(to right, transparent, var(--gold), transparent);
    margin: 0 auto;
  }

  /* ── SECTION BASE ── */
  section { padding: 5rem 2rem; }

  .section-inner {
    max-width: 1100px;
    margin: 0 auto;
  }

  .section-label {
    font-size: 10px;
    font-weight: 500;
    letter-spacing: 0.3em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 1rem;
  }

  .section-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(30px, 4vw, 48px);
    font-weight: 500;
    line-height: 1.15;
    color: var(--cream);
    margin-bottom: 1.5rem;
  }
  .section-title em { font-style: italic; color: var(--gold); }

  .section-body {
    font-size: 15px;
    font-weight: 300;
    line-height: 1.85;
    color: var(--text-2);
    max-width: 640px;
  }

  /* ── MISSION ── */
  .mission {
    background: var(--bg2);
    border-top: 0.5px solid var(--border);
    border-bottom: 0.5px solid var(--border);
  }

  .mission-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: center;
  }

  .mission-quote {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(22px, 3vw, 32px);
    font-style: italic;
    font-weight: 400;
    line-height: 1.5;
    color: var(--cream);
    border-left: 2px solid var(--gold);
    padding-left: 1.75rem;
    margin-bottom: 2rem;
  }

  /* ── PILLARS ── */
  .pillars-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5px;
    margin-top: 3rem;
    border: 1.5px solid var(--border);
    border-radius: var(--radius);
    overflow: hidden;
  }

  .pillar {
    background: var(--bg3);
    padding: 2rem 1.75rem;
    transition: background 0.2s;
  }
  .pillar:hover { background: #1e2019; }

  .pillar-icon {
    font-family: 'Cormorant Garamond', serif;
    font-size: 36px;
    font-style: italic;
    color: var(--gold);
    margin-bottom: 1rem;
    line-height: 1;
  }

  .pillar h3 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 20px;
    font-weight: 600;
    color: var(--cream);
    margin-bottom: 0.75rem;
    letter-spacing: 0.02em;
  }

  .pillar p {
    font-size: 13px;
    font-weight: 300;
    line-height: 1.7;
    color: var(--text-2);
  }

  /* ── COURSE ── */
  .course { background: var(--bg2); }

  .weeks-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
    margin-top: 3rem;
  }

  .week-card {
    background: var(--bg3);
    border: 0.5px solid var(--border);
    border-radius: var(--radius);
    padding: 1.5rem;
    transition: border-color 0.2s, transform 0.15s;
    cursor: default;
  }
  .week-card:hover {
    border-color: rgba(201,168,76,0.45);
    transform: translateY(-2px);
  }

  .week-num {
    font-size: 10px;
    font-weight: 500;
    letter-spacing: 0.25em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 0.5rem;
  }

  .week-card h3 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 18px;
    font-weight: 600;
    color: var(--cream);
    margin-bottom: 0.75rem;
    line-height: 1.3;
  }

  .week-card ul {
    list-style: none;
    display: flex; flex-direction: column; gap: 4px;
  }

  .week-card ul li {
    font-size: 12px;
    font-weight: 300;
    color: var(--text-2);
    padding-left: 12px;
    position: relative;
  }
  .week-card ul li::before {
    content: '·';
    position: absolute; left: 0;
    color: var(--gold-dk);
  }

  /* ── ABOUT ── */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1.4fr;
    gap: 5rem;
    align-items: start;
  }

  .about-card {
    background: var(--bg3);
    border: 0.5px solid var(--border);
    border-radius: var(--radius);
    padding: 2rem;
    text-align: center;
  }

  .about-avatar {
    width: 80px; height: 80px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--gold-dk), var(--sage));
    display: flex; align-items: center; justify-content: center;
    font-family: 'Cormorant Garamond', serif;
    font-size: 28px; font-weight: 600;
    color: var(--cream);
    margin: 0 auto 1.25rem;
  }

  .about-card h3 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 22px; font-weight: 600;
    color: var(--cream);
    margin-bottom: 4px;
  }

  .about-card .role {
    font-size: 12px; font-weight: 400;
    letter-spacing: 0.1em; text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 1.25rem;
  }

  .about-card .divider { margin: 1rem auto; }

  .about-contact-item {
    font-size: 13px; color: var(--text-2);
    margin-top: 8px;
  }
  .about-contact-item a { color: var(--gold); text-decoration: none; }
  .about-contact-item a:hover { text-decoration: underline; }

  /* ── CTA BANNER ── */
  .cta-banner {
    background: linear-gradient(135deg, var(--bg3) 0%, #1a1d16 100%);
    border-top: 0.5px solid var(--border);
    border-bottom: 0.5px solid var(--border);
    text-align: center;
  }

  /* ── VIDEOS PAGE ── */
  .videos-hero {
    padding: 8rem 2rem 3rem;
    text-align: center;
    background: var(--bg2);
    border-bottom: 0.5px solid var(--border);
  }

  .playlist-wrap {
    max-width: 900px;
    margin: 0 auto;
    border-radius: var(--radius);
    overflow: hidden;
    border: 0.5px solid var(--border);
    background: #000;
  }

  .playlist-wrap iframe {
    width: 100%;
    aspect-ratio: 16/9;
    display: block;
    border: none;
  }

  .videos-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 1.5rem;
    margin-top: 3rem;
  }

  .video-card {
    background: var(--bg3);
    border: 0.5px solid var(--border);
    border-radius: var(--radius);
    overflow: hidden;
    transition: border-color 0.2s, transform 0.15s;
  }
  .video-card:hover { border-color: rgba(201,168,76,0.4); transform: translateY(-2px); }

  .video-thumb {
    position: relative;
    aspect-ratio: 16/9;
    background: #1a1c17;
    overflow: hidden;
    cursor: pointer;
  }
  .video-thumb img { width: 100%; height: 100%; object-fit: cover; display: block; }
  .video-play-btn {
    position: absolute; inset: 0;
    display: flex; align-items: center; justify-content: center;
    background: rgba(0,0,0,0.4);
    transition: background 0.2s;
  }
  .video-thumb:hover .video-play-btn { background: rgba(0,0,0,0.2); }
  .video-play-btn svg { width: 48px; height: 48px; filter: drop-shadow(0 2px 8px rgba(0,0,0,0.5)); }

  .video-info { padding: 1rem 1.25rem; }
  .video-info h3 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 17px; font-weight: 600;
    color: var(--cream);
    margin-bottom: 4px;
    line-height: 1.3;
  }
  .video-info p { font-size: 12px; color: var(--text-3); }

  /* ── FOOTER ── */
  footer {
    background: var(--bg2);
    border-top: 0.5px solid var(--border);
    padding: 3rem 2rem;
    text-align: center;
  }

  .footer-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 28px; font-weight: 600;
    color: var(--gold);
    margin-bottom: 0.5rem;
    letter-spacing: 0.05em;
  }

  .footer-tagline {
    font-size: 12px; letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--text-3);
    margin-bottom: 1.5rem;
  }

  .footer-links {
    display: flex; gap: 1.5rem; justify-content: center;
    list-style: none; margin-bottom: 2rem;
  }
  .footer-links a {
    font-size: 12px; color: var(--text-2);
    text-decoration: none; cursor: pointer;
    transition: color 0.2s;
  }
  .footer-links a:hover { color: var(--gold); }

  .footer-bottom {
    font-size: 11px; color: var(--text-3);
    padding-top: 1.5rem;
    border-top: 0.5px solid rgba(201,168,76,0.08);
  }

  /* ── RESPONSIVE ── */
  @media (max-width: 768px) {
    .nav-links, .nav-cta { display: none; }
    .nav-mobile-btn { display: flex; }
    .mission-grid, .about-grid { grid-template-columns: 1fr; gap: 2.5rem; }
    .pillars-grid, .weeks-grid { grid-template-columns: 1fr; }
    .hero h1 { font-size: 36px; }
  }
</style>
</head>
<body>

<!-- NAVIGATION -->
<nav>
  <a class="nav-logo" onclick="showPage('home')">KUEL <span>Conditioning</span></a>
  <ul class="nav-links">
    <li><a onclick="showPage('home')" id="nav-home" class="active">Home</a></li>
    <li><a onclick="showPage('home'); scrollTo('course')">The Course</a></li>
    <li><a onclick="showPage('home'); scrollTo('about')">About</a></li>
    <li><a onclick="showPage('videos')" id="nav-videos">Videos</a></li>
  </ul>
  <a class="nav-cta" onclick="showPage('home'); scrollTo('contact')">Get Started</a>
  <div class="nav-mobile-btn" onclick="toggleMobileMenu()" aria-label="Menu">
    <span></span><span></span><span></span>
  </div>
</nav>

<!-- ══════════════════════════════════════════
     HOME PAGE
═══════════════════════════════════════════ -->
<div id="page-home" class="page active">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-bg"></div>
    <div class="hero-eyebrow">Bay City, MI · Spiritual Coaching · Non-Profit</div>
    <div class="hero-symbol">K</div>
    <h1>True <em>Healing</em><br>Starts Within</h1>
    <p class="hero-sub">KUEL Conditioning is a non-profit spiritual coaching program that helps individuals reconnect with themselves, resolve unmet needs, and discover lasting inner peace — across mind, body, and spirit.</p>
    <div class="hero-actions">
      <a class="btn-primary" onclick="scrollTo('course')">Explore the 6-Week Course</a>
      <a class="btn-ghost" onclick="showPage('videos')">Watch Our Videos</a>
    </div>
    <div class="hero-scroll">Scroll</div>
  </div>

  <!-- MISSION -->
  <section class="mission" id="mission">
    <div class="section-inner">
      <div class="mission-grid">
        <div>
          <div class="section-label">Our Foundation</div>
          <div class="mission-quote">"Once people get their needs met, they will find a level of peace that prevents relapse into the mental disorder response to trauma."</div>
          <div class="divider"></div>
        </div>
        <div>
          <div class="section-label">Mission</div>
          <h2 class="section-title">Helping People <em>Access</em> Their Own Capacity to Heal</h2>
          <p class="section-body">We believe that many psychological symptoms are not solely disorders to be treated, but signals guiding individuals toward unmet needs and unresolved experiences. By helping people reconnect to themselves, their values, and their inner peace — lasting healing becomes not only possible, but inevitable.</p>
          <br>
          <p class="section-body">Rooted in psychology, philosophy, and spiritual development, KUEL Conditioning creates environments of safety, understanding, and genuine support so every individual can thrive.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- PILLARS -->
  <section id="pillars">
    <div class="section-inner">
      <div class="section-label">What We Work On</div>
      <h2 class="section-title">The Three <em>Pillars</em></h2>
      <p class="section-body">KUEL Conditioning addresses the whole person — not just symptoms. Every aspect of your wellbeing is assessed, nurtured, and transformed.</p>
      <div class="pillars-grid">
        <div class="pillar">
          <div class="pillar-icon">B</div>
          <h3>Body</h3>
          <p>BMI, nutrition, exercise, sleep, general living, medical conditions, and all physical needs that form the foundation of wellbeing.</p>
        </div>
        <div class="pillar">
          <div class="pillar-icon">M</div>
          <h3>Mind</h3>
          <p>Attention, focus, repetitive thought patterns (both helpful and harmful), cognitive restructuring, and mental maintenance practices.</p>
        </div>
        <div class="pillar">
          <div class="pillar-icon">S</div>
          <h3>Spirit</h3>
          <p>Connection to self, others, and nature. Esteem, emotional intelligence, inner fortitude, and the energy that animates your life.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- COURSE -->
  <section class="course" id="course">
    <div class="section-inner">
      <div class="section-label">The Program</div>
      <h2 class="section-title">KUEL Konditioning Kourse<br><em>6-Week Transformation</em></h2>
      <p class="section-body">A structured, deeply personal journey through self-assessment, shadow work, spiritual awakening, and lasting reset. Each week builds on the last — guiding you from where you are to where you're capable of being.</p>
      <div class="weeks-grid">
        <div class="week-card">
          <div class="week-num">Week 01</div>
          <h3>Introduction &amp; Assessment</h3>
          <ul>
            <li>Sign contracts &amp; expectations</li>
            <li>Course overview &amp; intentions</li>
            <li>Mind / Body / Spirit self-assessment</li>
            <li>Goal &amp; intention setting</li>
            <li>Journaling &amp; reflection routines</li>
          </ul>
        </div>
        <div class="week-card">
          <div class="week-num">Week 02</div>
          <h3>Shadow Work</h3>
          <ul>
            <li>Identify triggers &amp; habitual responses</li>
            <li>Cognitive Behavioral Therapy tools</li>
            <li>7-step problem-solving process</li>
            <li>Self-care assessment (12 Pillars)</li>
            <li>Esteem, boundaries &amp; mantra writing</li>
          </ul>
        </div>
        <div class="week-card">
          <div class="week-num">Week 03</div>
          <h3>Wakening &amp; Spiritual Warfare</h3>
          <ul>
            <li>Deep dive into the psyche</li>
            <li>Perception, openness &amp; brain waves</li>
            <li>Art of War principles</li>
            <li>Law of Attraction</li>
            <li>Needs &amp; goals re-evaluation</li>
          </ul>
        </div>
        <div class="week-card">
          <div class="week-num">Week 04</div>
          <h3>Calcination &amp; Resetting</h3>
          <ul>
            <li>Remaking the soul</li>
            <li>Cognitive restructuring</li>
            <li>The Way — philosophical framework</li>
            <li>Mushroom Therapy preparation</li>
            <li>Support team &amp; safety planning</li>
          </ul>
        </div>
        <div class="week-card">
          <div class="week-num">Week 05</div>
          <h3>Detox &amp; Nature</h3>
          <ul>
            <li>Energy, vibration &amp; frequency</li>
            <li>Fasting &amp; alkaline nutrition</li>
            <li>Nature immersion &amp; grounding</li>
            <li>Mushroom Therapy experience</li>
            <li>Mind / Body / Spirit preparation</li>
          </ul>
        </div>
        <div class="week-card">
          <div class="week-num">Week 06</div>
          <h3>Test &amp; Evaluate</h3>
          <ul>
            <li>Integration &amp; reflection</li>
            <li>Evaluate at Day 2, 7, 30, 90, 180, 360</li>
            <li>Health review across all pillars</li>
            <li>Re-assess needs &amp; reset goals</li>
            <li>Schedule ongoing follow-ups</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section id="about">
    <div class="section-inner">
      <div class="about-grid">
        <div>
          <div class="about-card">
            <div class="about-avatar">LP</div>
            <h3>Luke Pawlaczyk</h3>
            <div class="role">Founder · KUEL Conditioning</div>
            <div class="divider"></div>
            <p style="font-size:13px; color:var(--text-2); line-height:1.7; margin-top:1rem;">
              Bay City, MI · Psychology Degree<br>Human Behavior, Philosophy &amp; Spiritual Development
            </p>
            <div style="margin-top:1.25rem;">
              <div class="about-contact-item">📧 <a href="mailto:kuelconditioning@gmail.com">kuelconditioning@gmail.com</a></div>
              <div class="about-contact-item">📞 <a href="tel:9892454676">(989) 245-4676</a></div>
            </div>
          </div>
        </div>
        <div>
          <div class="section-label">About the Founder</div>
          <h2 class="section-title">Driven by <em>Purpose</em>,<br>Grounded in Science</h2>
          <p class="section-body">Luke Pawlaczyk holds a degree in Psychology and has spent years studying human behavior, philosophy, and spiritual development. His work is built on the conviction that true healing emerges when people are given the right environment, support, and understanding to access their own innate capacity to heal.</p>
          <br>
          <p class="section-body">Based in Bay City, MI, Luke's vision is to work alongside those seeking healing — from the self-directed to the most vulnerable — and to bring compassionate, evidence-informed guidance that meets people exactly where they are.</p>
          <br>
          <p style="font-size:13px; font-style:italic; color:var(--gold); line-height:1.7;">"My purpose is to help individuals access the innate capacity to heal themselves when given the right environment, support, and understanding."</p>
          <br>
          <a class="btn-primary" id="contact" href="mailto:kuelconditioning@gmail.com" style="display:inline-flex;">Contact Us</a>
        </div>
      </div>
    </div>
  </section>

  <!-- CTA BANNER -->
  <section class="cta-banner">
    <div class="section-inner" style="text-align:center;">
      <div class="section-label">Ready to Begin?</div>
      <h2 class="section-title">Your <em>Transformation</em> Starts Here</h2>
      <p class="section-body" style="margin: 0 auto 2rem;">Take the first step toward true healing. Reach out to learn more about the KUEL Konditioning Kourse and whether it's right for you.</p>
      <div style="display:flex; gap:1rem; justify-content:center; flex-wrap:wrap;">
        <a class="btn-primary" href="mailto:kuelconditioning@gmail.com">Email Us Today</a>
        <a class="btn-ghost" onclick="showPage('videos')">Watch Our Videos</a>
      </div>
    </div>
  </section>

</div><!-- /page-home -->


<!-- ══════════════════════════════════════════
     VIDEOS PAGE
═══════════════════════════════════════════ -->
<div id="page-videos" class="page">

  <div class="videos-hero">
    <div class="section-label">Media</div>
    <h1 class="section-title" style="max-width:600px; margin:0 auto 1rem;">KUEL Konditioning Kourse<br><em>Video Library</em></h1>
    <p class="section-body" style="margin: 0 auto 2.5rem;">Explore our full video series — teachings on true healing, spiritual conditioning, and the transformative practices at the heart of the KUEL Konditioning Kourse.</p>
  </div>

  <section>
    <div class="section-inner">
      <div class="section-label">Full Playlist</div>
      <h2 class="section-title" style="margin-bottom:1.5rem;">Watch the <em>Series</em></h2>
      <div class="playlist-wrap">
        <iframe
          src="https://www.youtube.com/embed/videoseries?list=PLQY9UNiB9VdWiDhiZUnNiGYkGmZMGMDGC&rel=0&modestbranding=1"
          title="KUEL Konditioning Kourse Playlist"
          allowfullscreen
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture">
        </iframe>
      </div>
      <p style="font-size:13px; color:var(--text-3); margin-top:1rem; text-align:center;">
        7 videos · KUEL Conditioning · Use the playlist controls to navigate between episodes
      </p>

      <div style="margin-top:4rem;">
        <div class="section-label">Also Available On</div>
        <h2 class="section-title" style="margin-bottom:1.5rem;">Visit Our <em>YouTube Channel</em></h2>
        <div style="display:flex; gap:1rem; flex-wrap:wrap;">
          <a class="btn-primary" href="https://www.youtube.com/playlist?list=PLQY9UNiB9VdWiDhiZUnNiGYkGmZMGMDGC" target="_blank" rel="noopener">
            Open on YouTube ↗
          </a>
          <a class="btn-ghost" onclick="showPage('home')">← Back to Home</a>
        </div>
      </div>
    </div>
  </section>

</div><!-- /page-videos -->


<!-- FOOTER (shared) -->
<footer>
  <div class="footer-logo">KUEL Conditioning</div>
  <div class="footer-tagline">Knot a Kult · True Healing · Bay City, MI</div>
  <ul class="footer-links">
    <li><a onclick="showPage('home')">Home</a></li>
    <li><a onclick="showPage('home'); scrollTo('course')">The Course</a></li>
    <li><a onclick="showPage('videos')">Videos</a></li>
    <li><a href="mailto:kuelconditioning@gmail.com">Contact</a></li>
  </ul>
  <div class="footer-bottom">
    © 2025 KUEL Conditioning · Non-Profit Spiritual Coaching · Bay City, Michigan<br>
    <span style="color:var(--text-3); font-size:10px; margin-top:4px; display:block;">kuelconditioning@gmail.com · (989) 245-4676</span>
  </div>
</footer>


<script>
  function showPage(id) {
    document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
    document.getElementById('page-' + id).classList.add('active');
    document.querySelectorAll('.nav-links a').forEach(a => a.classList.remove('active'));
    const navEl = document.getElementById('nav-' + id);
    if (navEl) navEl.classList.add('active');
    window.scrollTo({ top: 0, behavior: 'smooth' });
  }

  function scrollTo(id) {
    setTimeout(() => {
      const el = document.getElementById(id);
      if (el) el.scrollIntoView({ behavior: 'smooth', block: 'start' });
    }, 100);
  }

  function toggleMobileMenu() {
    const links = document.querySelector('.nav-links');
    const cta = document.querySelector('.nav-cta');
    const showing = links.style.display === 'flex';
    if (showing) {
      links.style.display = '';
      cta.style.display = '';
    } else {
      links.style.cssText = 'display:flex; flex-direction:column; position:fixed; top:70px; left:0; right:0; background:rgba(14,15,13,0.97); padding:1.5rem 2rem; gap:1.25rem; border-bottom:0.5px solid rgba(201,168,76,0.18);';
      cta.style.cssText = 'display:block; position:fixed; top:calc(70px + 200px); left:2rem; right:2rem; text-align:center;';
    }
  }
</script>
</body>
</html>
