<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>KUEL Conditioning — True Healing</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;1,400;1,600&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
:root {
  --bg:#0e0f0d; --bg2:#141510; --bg3:#1a1c17;
  --gold:#c9a84c; --gold-lt:#e8c96b; --gold-dk:#8a6f2e;
  --sage:#7a9e7e; --cream:#f0e9d6; --cream-dk:#c8bda0;
  --text:#ede8df; --text-2:#b0a992; --text-3:#6b6555;
  --border:rgba(201,168,76,0.18); --radius:4px;
}
html { scroll-behavior:smooth; }
body { font-family:'DM Sans',sans-serif; background:var(--bg); color:var(--text); min-height:100vh; overflow-x:hidden; }
.page { display:none; }
.page.active { display:block; }

/* NAV */
nav { position:fixed; top:0; left:0; right:0; z-index:200; display:flex; align-items:center; justify-content:space-between; padding:0 2.5rem; height:70px; background:rgba(14,15,13,0.95); backdrop-filter:blur(12px); border-bottom:0.5px solid var(--border); }
.nav-logo { font-family:'Cormorant Garamond',serif; font-size:22px; font-weight:600; color:var(--gold); cursor:pointer; letter-spacing:.05em; }
.nav-logo span { color:var(--cream); }
.nav-links { display:flex; gap:2rem; list-style:none; }
.nav-links a { font-size:13px; font-weight:400; letter-spacing:.08em; text-transform:uppercase; color:var(--text-2); cursor:pointer; transition:color .2s; }
.nav-links a:hover, .nav-links a.active { color:var(--gold); }
.nav-cta { font-size:12px; font-weight:500; letter-spacing:.1em; text-transform:uppercase; color:var(--bg); background:var(--gold); padding:9px 20px; border-radius:var(--radius); cursor:pointer; transition:background .2s; }
.nav-cta:hover { background:var(--gold-lt); }

/* SHARED */
.divider { width:48px; height:1px; background:linear-gradient(to right,transparent,var(--gold),transparent); margin:0 auto; }
section { padding:5rem 2rem; }
.section-inner { max-width:1100px; margin:0 auto; }
.section-label { font-size:10px; font-weight:500; letter-spacing:.3em; text-transform:uppercase; color:var(--gold); margin-bottom:1rem; }
.section-title { font-family:'Cormorant Garamond',serif; font-size:clamp(30px,4vw,48px); font-weight:500; line-height:1.15; color:var(--cream); margin-bottom:1.5rem; }
.section-title em { font-style:italic; color:var(--gold); }
.section-body { font-size:15px; font-weight:300; line-height:1.85; color:var(--text-2); max-width:640px; }
.btn-primary { display:inline-flex; align-items:center; gap:8px; background:var(--gold); color:var(--bg); font-size:12px; font-weight:500; letter-spacing:.1em; text-transform:uppercase; padding:12px 24px; border-radius:var(--radius); border:none; cursor:pointer; transition:background .2s; text-decoration:none; }
.btn-primary:hover { background:var(--gold-lt); }
.btn-ghost { display:inline-flex; align-items:center; gap:8px; background:transparent; color:var(--cream-dk); font-size:12px; font-weight:500; letter-spacing:.1em; text-transform:uppercase; padding:12px 24px; border-radius:var(--radius); border:0.5px solid var(--border); cursor:pointer; transition:border-color .2s, color .2s; }
.btn-ghost:hover { border-color:var(--gold); color:var(--gold); }

/* HERO */
.hero { min-height:100vh; display:flex; flex-direction:column; align-items:center; justify-content:center; padding:8rem 2rem 4rem; position:relative; text-align:center; overflow:hidden; }
.hero-bg { position:absolute; inset:0; background:radial-gradient(ellipse 70% 60% at 50% 40%,rgba(201,168,76,.07) 0%,transparent 70%),radial-gradient(ellipse 40% 40% at 20% 80%,rgba(122,158,126,.06) 0%,transparent 60%); }
.hero-symbol { font-family:'Cormorant Garamond',serif; font-size:clamp(80px,12vw,140px); font-weight:400; font-style:italic; color:transparent; -webkit-text-stroke:1px rgba(201,168,76,.25); line-height:1; margin-bottom:1.5rem; }
.hero-eyebrow { font-size:11px; font-weight:500; letter-spacing:.25em; text-transform:uppercase; color:var(--gold); margin-bottom:1.25rem; }
.hero h1 { font-family:'Cormorant Garamond',serif; font-size:clamp(42px,7vw,80px); font-weight:500; line-height:1.08; color:var(--cream); margin-bottom:1.5rem; max-width:800px; }
.hero h1 em { font-style:italic; color:var(--gold); }
.hero-sub { font-size:16px; font-weight:300; line-height:1.75; color:var(--text-2); max-width:560px; margin-bottom:2.5rem; }
.hero-actions { display:flex; gap:1rem; flex-wrap:wrap; justify-content:center; }
.hero-scroll { position:absolute; bottom:2.5rem; left:50%; transform:translateX(-50%); display:flex; flex-direction:column; align-items:center; gap:8px; color:var(--text-3); font-size:10px; letter-spacing:.2em; text-transform:uppercase; }
.hero-scroll::after { content:''; display:block; width:1px; height:40px; background:linear-gradient(to bottom,var(--gold-dk),transparent); }

/* MISSION */
.mission { background:var(--bg2); border-top:0.5px solid var(--border); border-bottom:0.5px solid var(--border); }
.mission-grid { display:grid; grid-template-columns:1fr 1fr; gap:4rem; align-items:center; }
.mission-quote { font-family:'Cormorant Garamond',serif; font-size:clamp(22px,3vw,32px); font-style:italic; font-weight:400; line-height:1.5; color:var(--cream); border-left:2px solid var(--gold); padding-left:1.75rem; margin-bottom:2rem; }

/* PILLARS */
.pillars-grid { display:grid; grid-template-columns:repeat(3,1fr); gap:1.5px; margin-top:3rem; border:1.5px solid var(--border); border-radius:var(--radius); overflow:hidden; }
.pillar { background:var(--bg3); padding:2rem 1.75rem; transition:background .2s; }
.pillar:hover { background:#1e2019; }
.pillar-icon { font-family:'Cormorant Garamond',serif; font-size:36px; font-style:italic; color:var(--gold); margin-bottom:1rem; }
.pillar h3 { font-family:'Cormorant Garamond',serif; font-size:20px; font-weight:600; color:var(--cream); margin-bottom:.75rem; }
.pillar p { font-size:13px; font-weight:300; line-height:1.7; color:var(--text-2); }

/* COURSE */
.course { background:var(--bg2); }
.weeks-grid { display:grid; grid-template-columns:repeat(3,1fr); gap:1rem; margin-top:3rem; }
.week-card { background:var(--bg3); border:0.5px solid var(--border); border-radius:var(--radius); padding:1.5rem; transition:border-color .2s, transform .15s; }
.week-card:hover { border-color:rgba(201,168,76,.45); transform:translateY(-2px); }
.week-num { font-size:10px; font-weight:500; letter-spacing:.25em; text-transform:uppercase; color:var(--gold); margin-bottom:.5rem; }
.week-card h3 { font-family:'Cormorant Garamond',serif; font-size:18px; font-weight:600; color:var(--cream); margin-bottom:.75rem; }
.week-card ul { list-style:none; display:flex; flex-direction:column; gap:4px; }
.week-card ul li { font-size:12px; font-weight:300; color:var(--text-2); padding-left:12px; position:relative; }
.week-card ul li::before { content:'·'; position:absolute; left:0; color:var(--gold-dk); }

/* ABOUT */
.about-grid { display:grid; grid-template-columns:1fr 1.4fr; gap:5rem; align-items:start; }
.about-card { background:var(--bg3); border:0.5px solid var(--border); border-radius:var(--radius); padding:2rem; text-align:center; }
.about-avatar { width:80px; height:80px; border-radius:50%; background:linear-gradient(135deg,var(--gold-dk),var(--sage)); display:flex; align-items:center; justify-content:center; font-family:'Cormorant Garamond',serif; font-size:28px; font-weight:600; color:var(--cream); margin:0 auto 1.25rem; }
.about-card h3 { font-family:'Cormorant Garamond',serif; font-size:22px; font-weight:600; color:var(--cream); margin-bottom:4px; }
.about-card .role { font-size:12px; letter-spacing:.1em; text-transform:uppercase; color:var(--gold); margin-bottom:1.25rem; }
.about-contact-item { font-size:13px; color:var(--text-2); margin-top:8px; }
.about-contact-item a { color:var(--gold); text-decoration:none; }
.cta-banner { background:linear-gradient(135deg,var(--bg3) 0%,#1a1d16 100%); border-top:0.5px solid var(--border); border-bottom:0.5px solid var(--border); text-align:center; }

/* VIDEOS PAGE */
.videos-hero { padding:8rem 2rem 3rem; text-align:center; background:var(--bg2); border-bottom:0.5px solid var(--border); }
.playlist-wrap { max-width:900px; margin:0 auto; border-radius:var(--radius); overflow:hidden; border:0.5px solid var(--border); background:#000; }
.playlist-wrap iframe { width:100%; aspect-ratio:16/9; display:block; border:none; }

/* ─── RESOURCES PAGE ─── */
.resources-hero { padding:8rem 2rem 4rem; text-align:center; background:var(--bg2); border-bottom:0.5px solid var(--border); }

/* Featured docs top row */
.featured-docs { display:grid; grid-template-columns:repeat(3,1fr); gap:1.5rem; margin-top:2.5rem; }
.doc-featured-card { background:var(--bg3); border:0.5px solid var(--border); border-radius:var(--radius); overflow:hidden; transition:border-color .2s, transform .15s; display:flex; flex-direction:column; }
.doc-featured-card:hover { border-color:rgba(201,168,76,.5); transform:translateY(-2px); }
.doc-featured-badge { background:var(--gold); color:var(--bg); font-size:10px; font-weight:500; letter-spacing:.2em; text-transform:uppercase; padding:6px 14px; }
.doc-featured-body { padding:1.5rem; flex:1; display:flex; flex-direction:column; }
.doc-num { font-size:11px; color:var(--gold); font-weight:500; letter-spacing:.15em; margin-bottom:.4rem; }
.doc-featured-body h3 { font-family:'Cormorant Garamond',serif; font-size:20px; font-weight:600; color:var(--cream); margin-bottom:.6rem; line-height:1.3; }
.doc-featured-body p { font-size:12px; color:var(--text-2); line-height:1.65; margin-bottom:1.25rem; flex:1; }
.doc-featured-actions { display:flex; gap:.6rem; flex-wrap:wrap; }
.doc-open-btn { display:inline-flex; align-items:center; gap:6px; background:var(--gold); color:var(--bg); font-size:11px; font-weight:500; letter-spacing:.08em; text-transform:uppercase; padding:9px 16px; border-radius:var(--radius); border:none; cursor:pointer; transition:background .2s; }
.doc-open-btn:hover { background:var(--gold-lt); }
.doc-link-btn { display:inline-flex; align-items:center; gap:6px; background:transparent; color:var(--text-2); font-size:11px; font-weight:400; letter-spacing:.08em; text-transform:uppercase; padding:9px 14px; border-radius:var(--radius); border:0.5px solid var(--border); cursor:pointer; text-decoration:none; transition:color .2s, border-color .2s; }
.doc-link-btn:hover { color:var(--gold); border-color:var(--gold); }

/* Resource list 4-10 */
.resources-list { display:flex; flex-direction:column; gap:10px; margin-top:2rem; }
.resource-row { background:var(--bg3); border:0.5px solid var(--border); border-radius:var(--radius); display:flex; align-items:center; gap:1.25rem; padding:1.1rem 1.5rem; transition:border-color .2s; }
.resource-row:hover { border-color:rgba(201,168,76,.4); }
.resource-num { font-family:'Cormorant Garamond',serif; font-size:28px; font-style:italic; color:var(--gold-dk); min-width:36px; text-align:center; line-height:1; }
.resource-info { flex:1; }
.resource-info h4 { font-size:14px; font-weight:500; color:var(--cream); margin-bottom:2px; }
.resource-info p { font-size:12px; color:var(--text-3); }
.resource-type { font-size:10px; font-weight:500; letter-spacing:.15em; text-transform:uppercase; padding:3px 8px; border-radius:3px; background:rgba(201,168,76,.1); color:var(--gold-dk); }
.resource-link { display:inline-flex; align-items:center; gap:6px; font-size:11px; font-weight:500; letter-spacing:.08em; text-transform:uppercase; color:var(--text-2); text-decoration:none; padding:8px 14px; border:0.5px solid var(--border); border-radius:var(--radius); transition:color .2s, border-color .2s; }
.resource-link:hover { color:var(--gold); border-color:var(--gold); }

/* DOC MODAL */
.doc-modal-overlay { position:fixed; inset:0; z-index:500; background:rgba(8,9,7,.92); backdrop-filter:blur(6px); display:none; overflow-y:auto; padding:1.5rem; }
.doc-modal-overlay.open { display:block; }
.doc-modal { max-width:820px; margin:0 auto; background:#f8f5ef; border-radius:6px; overflow:hidden; box-shadow:0 20px 80px rgba(0,0,0,.7); }
.doc-modal-toolbar { background:#1a1c17; border-bottom:1px solid rgba(201,168,76,.2); padding:12px 20px; display:flex; align-items:center; justify-content:space-between; gap:12px; position:sticky; top:0; z-index:10; }
.doc-modal-title { font-size:13px; font-weight:500; color:var(--gold); letter-spacing:.05em; }
.doc-modal-actions { display:flex; gap:8px; }
.modal-print-btn { background:var(--gold); color:var(--bg); border:none; font-size:11px; font-weight:500; letter-spacing:.1em; text-transform:uppercase; padding:7px 16px; border-radius:3px; cursor:pointer; }
.modal-print-btn:hover { background:var(--gold-lt); }
.modal-close-btn { background:transparent; color:var(--text-3); border:0.5px solid rgba(201,168,76,.2); font-size:18px; width:32px; height:32px; border-radius:3px; cursor:pointer; display:flex; align-items:center; justify-content:center; transition:color .2s; }
.modal-close-btn:hover { color:var(--cream); }
.doc-modal-body { padding:3rem 3.5rem; background:#f8f5ef; color:#1a1a1a; }
.doc-body-title { font-family:'Cormorant Garamond',serif; font-size:26px; font-weight:600; color:#1a1a1a; text-align:center; margin-bottom:.5rem; }
.doc-body-subtitle { font-size:12px; text-align:center; color:#666; margin-bottom:2rem; letter-spacing:.05em; }
.doc-section-title { font-size:13px; font-weight:600; color:#1a1a1a; margin:1.5rem 0 .5rem; text-transform:uppercase; letter-spacing:.08em; }
.doc-body-text { font-size:13px; line-height:1.8; color:#333; margin-bottom:.75rem; }
.doc-fill-field { display:inline-block; border:none; border-bottom:1.5px solid #8a6f2e; background:transparent; font-size:13px; font-family:'DM Sans',sans-serif; color:#1a1a1a; padding:2px 6px; min-width:160px; outline:none; transition:border-color .2s; }
.doc-fill-field:focus { border-color:#c9a84c; background:rgba(201,168,76,.07); }
.doc-fill-field.wide { min-width:240px; }
.doc-fill-field.short { min-width:80px; }
.doc-sig-block { display:grid; grid-template-columns:1fr 1fr; gap:2rem; margin-top:2.5rem; padding-top:1.5rem; border-top:1px solid #ddd; }
.doc-sig-col .sig-line { border-bottom:1.5px solid #333; height:40px; margin-bottom:6px; }
.doc-sig-col label { font-size:11px; color:#666; }
.doc-sig-col input { width:100%; border:none; border-bottom:1.5px solid #8a6f2e; background:transparent; font-size:13px; padding:2px 4px; margin-top:4px; outline:none; color:#1a1a1a; }
.doc-sig-col input:focus { border-color:#c9a84c; background:rgba(201,168,76,.07); }
.doc-bullet { font-size:13px; line-height:1.8; color:#333; padding-left:1.25rem; position:relative; margin-bottom:.3rem; }
.doc-bullet::before { content:'—'; position:absolute; left:0; color:#8a6f2e; }
.doc-strong { font-weight:600; }
.doc-note { background:rgba(201,168,76,.08); border-left:3px solid #c9a84c; padding:10px 14px; border-radius:0 3px 3px 0; margin:1rem 0; font-size:12px; color:#555; line-height:1.7; }

/* PRINT */
@media print {
  nav, .doc-modal-toolbar, .doc-featured-actions, .hero-scroll, footer { display:none !important; }
  .doc-modal-overlay { position:static !important; background:white !important; padding:0 !important; }
  .doc-modal { box-shadow:none !important; max-width:100% !important; }
  .doc-modal-body { padding:1.5rem 2rem !important; }
  body > *:not(.doc-modal-overlay) { display:none !important; }
  .doc-fill-field { border-bottom:1px solid #000 !important; min-width:180px; }
}

/* FOOTER */
footer { background:var(--bg2); border-top:0.5px solid var(--border); padding:3rem 2rem; text-align:center; }
.footer-logo { font-family:'Cormorant Garamond',serif; font-size:28px; font-weight:600; color:var(--gold); margin-bottom:.5rem; }
.footer-tagline { font-size:12px; letter-spacing:.15em; text-transform:uppercase; color:var(--text-3); margin-bottom:1.5rem; }
.footer-links { display:flex; gap:1.5rem; justify-content:center; list-style:none; margin-bottom:2rem; }
.footer-links a { font-size:12px; color:var(--text-2); cursor:pointer; transition:color .2s; }
.footer-links a:hover { color:var(--gold); }
.footer-bottom { font-size:11px; color:var(--text-3); padding-top:1.5rem; border-top:0.5px solid rgba(201,168,76,.08); }

@media (max-width:768px) {
  .nav-links, .nav-cta { display:none; }
  .mission-grid, .about-grid { grid-template-columns:1fr; gap:2.5rem; }
  .pillars-grid, .weeks-grid, .featured-docs { grid-template-columns:1fr; }
  .doc-modal-body { padding:2rem 1.5rem; }
  .doc-sig-block { grid-template-columns:1fr; gap:1rem; }
  nav { padding:0 1.5rem; }
}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo" onclick="showPage('home')">KUEL <span>Conditioning</span></div>
  <ul class="nav-links">
    <li><a id="nav-home" class="active" onclick="showPage('home')">Home</a></li>
    <li><a id="nav-course" onclick="showPage('course')">The Course</a></li>
    <li><a id="nav-resources" onclick="showPage('resources')">Resources</a></li>
    <li><a id="nav-videos" onclick="showPage('videos')">Videos</a></li>
    <li><a id="nav-coach" onclick="showPage('coach')">Life Coach</a></li>
  </ul>
  <div class="nav-cta" onclick="showPage('coach')">Life Coach</div>

  <!-- Hamburger dropdown -->
  <div style="position:relative;margin-left:12px;">
    <button id="hamburger-btn" onclick="toggleDropdown()" aria-label="Menu" style="background:transparent;border:0.5px solid rgba(201,168,76,0.3);border-radius:var(--radius);width:38px;height:38px;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:5px;cursor:pointer;padding:0;transition:border-color .2s;">
      <span style="display:block;width:18px;height:1.5px;background:var(--text-2);border-radius:2px;transition:.2s;"></span>
      <span style="display:block;width:18px;height:1.5px;background:var(--text-2);border-radius:2px;transition:.2s;"></span>
      <span style="display:block;width:18px;height:1.5px;background:var(--text-2);border-radius:2px;transition:.2s;"></span>
    </button>
    <div id="dropdown-menu" style="display:none;position:absolute;top:calc(100% + 10px);right:0;background:rgba(14,15,13,0.98);border:0.5px solid rgba(201,168,76,0.25);border-radius:var(--radius);min-width:180px;z-index:999;backdrop-filter:blur(12px);overflow:hidden;box-shadow:0 8px 32px rgba(0,0,0,0.5);">
      <div onclick="showPage('home');toggleDropdown()" style="padding:12px 20px;font-size:13px;color:var(--text-2);cursor:pointer;letter-spacing:.06em;transition:background .15s;border-bottom:0.5px solid rgba(201,168,76,0.08);" onmouseover="this.style.background='rgba(201,168,76,0.08)';this.style.color='var(--gold)'" onmouseout="this.style.background='transparent';this.style.color='var(--text-2)'">Home</div>
      <div onclick="showPage('course');toggleDropdown()" style="padding:12px 20px;font-size:13px;color:var(--text-2);cursor:pointer;letter-spacing:.06em;transition:background .15s;border-bottom:0.5px solid rgba(201,168,76,0.08);" onmouseover="this.style.background='rgba(201,168,76,0.08)';this.style.color='var(--gold)'" onmouseout="this.style.background='transparent';this.style.color='var(--text-2)'">The Course</div>
      <div onclick="showPage('resources');toggleDropdown()" style="padding:12px 20px;font-size:13px;color:var(--text-2);cursor:pointer;letter-spacing:.06em;transition:background .15s;border-bottom:0.5px solid rgba(201,168,76,0.08);" onmouseover="this.style.background='rgba(201,168,76,0.08)';this.style.color='var(--gold)'" onmouseout="this.style.background='transparent';this.style.color='var(--text-2)'">Resources</div>
      <div onclick="showPage('videos');toggleDropdown()" style="padding:12px 20px;font-size:13px;color:var(--text-2);cursor:pointer;letter-spacing:.06em;transition:background .15s;border-bottom:0.5px solid rgba(201,168,76,0.08);" onmouseover="this.style.background='rgba(201,168,76,0.08)';this.style.color='var(--gold)'" onmouseout="this.style.background='transparent';this.style.color='var(--text-2)'">Videos</div>
      <div onclick="showPage('coach');toggleDropdown()" style="padding:12px 20px;font-size:13px;color:var(--gold);cursor:pointer;letter-spacing:.06em;font-weight:500;transition:background .15s;" onmouseover="this.style.background='rgba(201,168,76,0.08)'" onmouseout="this.style.background='transparent'">Life Coach</div>
    </div>
  </div>
</nav>

<!-- ═══════════════ HOME PAGE ═══════════════ -->
<div id="page-home" class="page active">
  <div class="hero">
    <div class="hero-bg"></div>
    <div style="width:clamp(160px,20vw,220px);margin:0 auto 1.5rem;border-radius:50%;overflow:hidden;position:relative;">
      <div style="width:100%;padding-top:100%;position:relative;overflow:hidden;">
        <img src="kuel-logo.jpg" alt="KUEL Conditioning Logo" style="position:absolute;top:50%;left:50%;transform:translate(-50%,-50%) scale(1.06);width:100%;height:100%;object-fit:cover;object-position:center center;" />
      </div>
    </div>
    <h1>True <em>Healing</em><br>Starts Within</h1>
    <p class="hero-sub">KUEL Conditioning is a non-profit spiritual coaching program helping individuals reconnect with themselves, resolve unmet needs, and discover lasting inner peace — across mind, body, and spirit.</p>

  </div>

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
          <p class="section-body">We believe many psychological symptoms are signals guiding individuals toward unmet needs. By helping people reconnect to themselves, their values, and inner peace — lasting healing becomes not only possible, but inevitable.</p>
        </div>
      </div>
    </div>
  </section>

  <section id="pillars">
    <div class="section-inner">
      <div class="section-label">What We Work On</div>
      <h2 class="section-title">The Three <em>Pillars</em></h2>
      <div class="pillars-grid">
        <div class="pillar"><h3>Body</h3><p>BMI, nutrition, exercise, sleep, general living, and all physical needs that form the foundation of wellbeing.</p></div>
        <div class="pillar"><h3>Mind</h3><p>Attention, focus, repetitive thought patterns, cognitive restructuring, and mental maintenance practices.</p></div>
        <div class="pillar"><h3>Spirit</h3><p>Connection to self, others, and nature. Esteem, emotional intelligence, inner fortitude, and life energy.</p></div>
      </div>
    </div>
  </section>

  <section class="cta-banner">
    <div class="section-inner">
      <div class="section-label">Ready to Begin?</div>
      <h2 class="section-title">Your <em>Transformation</em> Starts Here</h2>
      <p class="section-body" style="margin:0 auto 2rem;">The KUEL A.I. Agent leverages the Human Hierarchy of Needs based on your self-assessment, then pulls your wants and goals so that it can give you specific advice to help you move towards your best life. The Agent has a hedonistic approach to happiness where it is important to make the most out of life without harming yourself or others.</p>
      <div style="display:flex;gap:1rem;justify-content:center;flex-wrap:wrap;">
        <div style="display:flex;flex-direction:column;align-items:center;gap:6px;">
          <a class="btn-primary" href="https://claude.ai/public/artifacts/df7873d5-05fc-41a1-adbc-8b7f41def6b2" target="_blank" rel="noopener">KUEL Life Coach ↗</a>
          <span style="font-size:11px;color:var(--text-3);font-style:italic;">(free claude.ai account required)</span>
        </div>
        <div class="btn-ghost" onclick="showPage('resources')">View Resources</div>
      </div>
    </div>
  </section>
</div>

<!-- ═══════════════ COURSE PAGE ═══════════════ -->
<div id="page-course" class="page">
  <div class="videos-hero">
    <div class="section-label">The Program</div>
    <h1 class="section-title" style="max-width:700px;margin:0 auto .75rem;">KUEL Konditioning Kourse<br><em>6-Week Transformation</em></h1>
    <p class="section-body" style="margin:0 auto;">A structured, deeply personal journey through self-assessment, shadow work, spiritual awakening, and lasting reset. Each week builds on the last — guiding you from where you are to where you're capable of being.</p>
  </div>
  <section>
    <div class="section-inner">
      <div class="weeks-grid">
        <div class="week-card"><div class="week-num">Week 01</div><h3>Introduction &amp; Assessment</h3><ul><li>Sign contracts &amp; expectations</li><li>Mind / Body / Spirit self-assessment</li><li>Goal &amp; intention setting</li><li>Journaling &amp; reflection routines</li></ul></div>
        <div class="week-card"><div class="week-num">Week 02</div><h3>Shadow Work</h3><ul><li>Identify triggers &amp; habitual responses</li><li>Cognitive Behavioral Therapy tools</li><li>7-step problem-solving process</li><li>Esteem, boundaries &amp; mantra writing</li></ul></div>
        <div class="week-card"><div class="week-num">Week 03</div><h3>Wakening &amp; Spiritual Warfare</h3><ul><li>Deep dive into the psyche</li><li>Brain waves &amp; perception</li><li>Art of War principles</li><li>Law of Attraction</li></ul></div>
        <div class="week-card"><div class="week-num">Week 04</div><h3>Calcination &amp; Resetting</h3><ul><li>Remaking the soul</li><li>Cognitive restructuring</li><li>The Way — philosophical framework</li><li>Support team &amp; safety planning</li></ul></div>
        <div class="week-card"><div class="week-num">Week 05</div><h3>Detox &amp; Nature</h3><ul><li>Energy, vibration &amp; frequency</li><li>Fasting &amp; alkaline nutrition</li><li>Nature immersion &amp; grounding</li><li>Mushroom Therapy experience</li></ul></div>
        <div class="week-card"><div class="week-num">Week 06</div><h3>Test &amp; Evaluate</h3><ul><li>Integration &amp; reflection</li><li>Evaluate at Day 2, 7, 30, 90, 180, 360</li><li>Re-assess needs &amp; reset goals</li><li>Schedule ongoing follow-ups</li></ul></div>
      </div>
      <div style="display:flex;gap:1rem;flex-wrap:wrap;margin-top:3rem;">
        <a class="btn-primary" href="mailto:kuelconditioning@gmail.com">Enroll Today</a>
        <div class="btn-ghost" onclick="showPage('resources')">View Resources ↗</div>
      </div>
    </div>
  </section>
</div>

<!-- ═══════════════ RESOURCES PAGE ═══════════════ -->
<div id="page-resources" class="page">
  <div class="resources-hero">
    <div class="section-label">DIY Toolkit</div>
    <h1 class="section-title" style="max-width:700px;margin:0 auto .75rem;">Course <em>Resources</em> &amp; Documents</h1>
    <p class="section-body" style="margin:0 auto;">All contracts, worksheets, outlines, and lesson materials for the KUEL Konditioning Kourse. Fill out documents directly on this page and print with your answers.</p>
  </div>

  <section>
    <div class="section-inner">

      <!-- FEATURED DOCS 1, 2, 3 -->
      <div class="section-label">Start Here — Fill Out &amp; Print</div>
      <h2 class="section-title">Required <em>Agreements</em> &amp; Foundational Texts</h2>
      <p class="section-body">Click "Open &amp; Fill" to complete these documents right here on the website. Type your answers in the fields and print — your answers will appear on the printed copy.</p>

      <div class="featured-docs">

        <!-- DOC 1 -->
        <div class="doc-featured-card">
          <div class="doc-featured-badge">✦ Featured · Week 1</div>
          <div class="doc-featured-body">
            <h3>Kode of Konduct Kontract</h3>
            <p>The foundational agreement between Coach and Client outlining ethical principles, responsibilities, boundaries, and expectations for the coaching relationship.</p>
            <div class="doc-featured-actions">
              <button class="doc-open-btn" onclick="openModal('doc1')">✏ Open &amp; Fill</button>
              <a class="doc-link-btn" href="https://docs.google.com/document/d/1czaUrZSoh7TwyFKOPuIRtSbNULMQ3e6slJgXwVdQAO0/edit" target="_blank">Open in Drive ↗</a>
            </div>
          </div>
        </div>

        <!-- DOC 2 -->
        <div class="doc-featured-card">
          <div class="doc-featured-badge">✦ Featured · Week 1</div>
          <div class="doc-featured-body">
            <h3>Confidentiality Agreement</h3>
            <p>A formal agreement ensuring all personal, emotional, spiritual, and psychological information shared during coaching sessions remains strictly confidential.</p>
            <div class="doc-featured-actions">
              <button class="doc-open-btn" onclick="openModal('doc2')">✏ Open &amp; Fill</button>
              <a class="doc-link-btn" href="https://docs.google.com/document/d/1JQe7wBe4IEqbAswqbKK5gS8Mk1L4Bo2GsxLK2el3CeY/edit" target="_blank">Open in Drive ↗</a>
            </div>
          </div>
        </div>

        <!-- DOC 3 (Needs-Goals) -->
        <div class="doc-featured-card">
          <div class="doc-featured-badge">✦ Featured · Week 1</div>
          <div class="doc-featured-body">
            <h3>Needs Assessment &amp; Goal Setting</h3>
            <p>Maslow's hierarchy self-assessment — score each need 1–10, identify gaps, then set daily, monthly, yearly &amp; long-term goals to manifest your best life.</p>
            <div class="doc-featured-actions">
              <button class="doc-open-btn" onclick="openModal('doc4')">✏ Open &amp; Fill</button>
              <a class="doc-link-btn" href="https://drive.google.com/file/d/1vsRHALVx3J_lJWnPNAvaYBJa1po3kdmP/view" target="_blank">Open in Drive ↗</a>
            </div>
          </div>
        </div>
      </div>

      <!-- DOCS 3 & 5-10 -->
      <div style="margin-top:4rem;">
        <div class="resources-list">
          <div class="resource-row">
            <div class="resource-info"><h4>The Way</h4><p>Musashi's 9 principles, philosophical frameworks from Buddha, Confucius, and Plato — foundational wisdom for Week 4</p></div>
            <div style="display:flex;flex-direction:column;gap:6px;align-items:center;">
              <a class="resource-link" href="https://youtu.be/cUDA6tXtzbw?si=hBIHiN3RnHBkh82H" target="_blank" style="flex-direction:column;align-items:center;gap:2px;padding:8px 14px;">Open<span style="font-size:10px;letter-spacing:.08em;text-transform:uppercase;color:var(--gold);">Video</span></a>
              <a class="resource-link" href="https://docs.google.com/document/d/1bAWWlb6sSPKD279LLPwjHJJhGA_2mmiBhNyLILMtL04/edit" target="_blank" style="flex-direction:column;align-items:center;gap:2px;padding:8px 14px;">Open<span style="font-size:10px;letter-spacing:.08em;text-transform:uppercase;color:var(--gold);">Outline</span></a>
            </div>
          </div>
          <div class="resource-row">
            <div class="resource-info"><h4>Finding Your Soul</h4><p>Journaling techniques, the soul across religious &amp; philosophical traditions, remaking &amp; renewing the soul</p></div>
            <div style="display:flex;flex-direction:column;gap:6px;align-items:center;">
              <a class="resource-link" href="https://youtu.be/SsYwEa26uus?si=4VvCaO4DdbGHpo7o" target="_blank" style="flex-direction:column;align-items:center;gap:2px;padding:8px 14px;">Open<span style="font-size:10px;letter-spacing:.08em;text-transform:uppercase;color:var(--gold);">Video</span></a>
              <a class="resource-link" href="https://docs.google.com/document/d/1F4O8932BXA4iUeCoN7N2CeCNA64ufqJ_4iUPIdb0Lto/edit" target="_blank" style="flex-direction:column;align-items:center;gap:2px;padding:8px 14px;">Open<span style="font-size:10px;letter-spacing:.08em;text-transform:uppercase;color:var(--gold);">Outline</span></a>
            </div>
          </div>
          <div class="resource-row">
            <div class="resource-info"><h4>Spiritual Warfare</h4><p>Universal Laws of Vibration &amp; Energy, manipulation vs alignment, good vs bad energy dynamics</p></div>
            <div style="display:flex;flex-direction:column;gap:6px;align-items:center;">
              <a class="resource-link" href="https://youtu.be/HgGzTxEI7zc?si=W00BdS0AqLeihla_" target="_blank" style="flex-direction:column;align-items:center;gap:2px;padding:8px 14px;">Open<span style="font-size:10px;letter-spacing:.08em;text-transform:uppercase;color:var(--gold);">Video</span></a>
              <a class="resource-link" href="https://docs.google.com/document/d/1bWj3Yy9JS2kWdG-mr7B60GvRE9YyCB6ov_JoZMTYv9s/edit" target="_blank" style="flex-direction:column;align-items:center;gap:2px;padding:8px 14px;">Open<span style="font-size:10px;letter-spacing:.08em;text-transform:uppercase;color:var(--gold);">Outline</span></a>
            </div>
          </div>
          <div class="resource-row">
            <div class="resource-info"><h4>Spiritual Warfare (Dark Psychology)</h4><p>Dark psychology techniques, manipulation in relationships, cognitive-behavioral protection strategies</p></div>
            <a class="resource-link" href="https://docs.google.com/document/d/1A6QtvsVdVdodq5U8AdS4rkTn0Xz9iT7vt5WINsOYdv0/edit" target="_blank" style="flex-direction:column;align-items:center;gap:2px;padding:8px 14px;">Open<span style="font-size:10px;letter-spacing:.08em;text-transform:uppercase;color:var(--gold);">Notes</span></a>
          </div>
          <div class="resource-row">
            <div class="resource-info"><h4>Journaling</h4><p>Types of journaling, goal-setting journal templates, visualization techniques for focus &amp; accountability</p></div>
            <a class="resource-link" href="https://docs.google.com/document/d/1FabR3Wq3YNLz77v4y1BeR55FFTLTPfwELDbF1rTxaS0/edit" target="_blank" style="flex-direction:column;align-items:center;gap:2px;padding:8px 14px;">Open<span style="font-size:10px;letter-spacing:.08em;text-transform:uppercase;color:var(--gold);">Notes</span></a>
          </div>
          <div class="resource-row">
            <div class="resource-info"><h4>Nutrition</h4><p>Alkaline diet principles, food pH science, fasting protocols, nutrition lesson plan for Week 5</p></div>
            <a class="resource-link" href="https://docs.google.com/document/d/1SNsy-TddZl7z1ZEUBB5fWAivo5YgPBCfPzuk6BMNdQM/edit" target="_blank" style="flex-direction:column;align-items:center;gap:2px;padding:8px 14px;">Open<span style="font-size:10px;letter-spacing:.08em;text-transform:uppercase;color:var(--gold);">Notes</span></a>
          </div>
          <div class="resource-row">
            <div class="resource-info"><h4>Power</h4><p>The Art of War &amp; spiritual warfare, Sun Tzu's principles applied to inner battles, strategy &amp; discernment</p></div>
            <a class="resource-link" href="https://docs.google.com/document/d/10s8_Lx_pq6pSUddy2X8eagO0ipqTonxfkh_jma1QumQ/edit" target="_blank" style="flex-direction:column;align-items:center;gap:2px;padding:8px 14px;">Open<span style="font-size:10px;letter-spacing:.08em;text-transform:uppercase;color:var(--gold);">Notes</span></a>
          </div>
          <div class="resource-row">
            <div class="resource-info"><h4>Self-Care</h4><p>50 self-care practices across physical, emotional, mental, social, and spiritual dimensions of wellness</p></div>
            <a class="resource-link" href="https://docs.google.com/document/d/1WyqGHhx80-HcZFWuROxm4NFDCoDVZo_YusUPRnDB1vk/edit" target="_blank" style="flex-direction:column;align-items:center;gap:2px;padding:8px 14px;">Open<span style="font-size:10px;letter-spacing:.08em;text-transform:uppercase;color:var(--gold);">Notes</span></a>
          </div>
          <div class="resource-row">
            <div class="resource-info"><h4>Mushies</h4><p>KKK legal, medical, and other practical business framework with A2 and Ypsi's formal Resolutions.</p></div>
            <a class="resource-link" href="https://drive.google.com/drive/folders/1ZDAthi6E4MSrvI1TSedMSlbuMVX6W3Po" target="_blank" style="flex-direction:column;align-items:center;gap:2px;padding:8px 14px;">Open<span style="font-size:10px;letter-spacing:.08em;text-transform:uppercase;color:var(--gold);">Notes</span></a>
          </div>
        </div>
      </div>

    </div>
  </section>
</div>

<!-- ═══════════════ VIDEOS PAGE ═══════════════ -->
<div id="page-videos" class="page">
  <div class="videos-hero">
    <div class="section-label">Media</div>
    <h1 class="section-title" style="max-width:600px;margin:0 auto 1rem;">KUEL Konditioning Kourse<br><em>Video Library</em></h1>
    <p class="section-body" style="margin:0 auto 2.5rem;">Explore our full video series — teachings on true healing, spiritual conditioning, and the transformative practices at the heart of the course.</p>
  </div>
  <section>
    <div class="section-inner">
      <div style="display:grid;grid-template-columns:repeat(auto-fill,minmax(480px,1fr));gap:2rem;">

          <div style="background:var(--bg3);border:0.5px solid var(--border);border-radius:var(--radius);overflow:hidden;">
            <div style="aspect-ratio:16/9;background:#000;">
              <iframe width="100%" height="100%" src="https://www.youtube.com/embed/cKK12aczfvc?list=PLQY9UNiB9VdWiDhiZUnNiGYkGmZMGMDGC?rel=0&modestbranding=1" title="KKK Overview" allowfullscreen allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" style="display:block;border:none;"></iframe>
            </div>
            <div style="padding:1rem 1.25rem;">
              <div style="font-family:'Cormorant Garamond',serif;font-size:18px;font-weight:600;color:var(--cream);margin-bottom:6px;">KKK Overview</div>
              <div style="font-size:13px;color:var(--text-2);line-height:1.7;">Overview of 6-week spiritual coaching program designed to help people improve their lives through self-assessment, shadow work, mindset shifts, spiritual exploration, and lifestyle changes. Participants move through weekly themes—from goal setting and cognitive tools to detox, nature immersion, and long-term reflection—with the aim of resolving unmet needs, building inner peace, and creating lasting personal transformation.</div>
            </div>
          </div>

          <div style="background:var(--bg3);border:0.5px solid var(--border);border-radius:var(--radius);overflow:hidden;">
            <div style="aspect-ratio:16/9;background:#000;">
              <iframe width="100%" height="100%" src="https://www.youtube.com/embed/2xXozhSFoRI?rel=0&modestbranding=1" title="Needs Assessment &amp; Goal Setting" allowfullscreen allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" style="display:block;border:none;"></iframe>
            </div>
            <div style="padding:1rem 1.25rem;">
              <div style="font-family:'Cormorant Garamond',serif;font-size:18px;font-weight:600;color:var(--cream);margin-bottom:6px;">Needs Assessment &amp; Goal Setting</div>
              <div style="font-size:13px;color:var(--text-2);line-height:1.7;">Helps identify which foundational areas of life—such as physical health, safety, relationships, esteem, and purpose—may be underdeveloped, allowing you to focus energy on what is most likely to improve your well-being and stability. Goal setting then turns that awareness into action by creating a clear path toward growth, helping you build habits, track progress, and intentionally move toward the life you want.</div>
            </div>
          </div>

          <div style="background:var(--bg3);border:0.5px solid var(--border);border-radius:var(--radius);overflow:hidden;">
            <div style="aspect-ratio:16/9;background:#000;">
              <iframe width="100%" height="100%" src="https://www.youtube.com/embed/cUDA6tXtzbw?rel=0&modestbranding=1" title="The Way" allowfullscreen allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" style="display:block;border:none;"></iframe>
            </div>
            <div style="padding:1rem 1.25rem;">
              <div style="font-family:'Cormorant Garamond',serif;font-size:18px;font-weight:600;color:var(--cream);margin-bottom:6px;">The Way</div>
              <div style="font-size:13px;color:var(--text-2);line-height:1.7;">Drawing from Musashi's 9 Principles, the 10 Abilities, and the 7 Arts, this lesson explores what it means to master not just a skill but an entire way of living. Weaving together the philosophies of Confucius, Buddha, and Plato, it challenges you to live honestly, train relentlessly, and see what others cannot — turning strategy and wisdom into a daily spiritual practice.</div>
            </div>
          </div>

          <div style="background:var(--bg3);border:0.5px solid var(--border);border-radius:var(--radius);overflow:hidden;">
            <div style="aspect-ratio:16/9;background:#000;">
              <iframe width="100%" height="100%" src="https://www.youtube.com/embed/SsYwEa26uus?rel=0&modestbranding=1" title="Finding Your Soul" allowfullscreen allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" style="display:block;border:none;"></iframe>
            </div>
            <div style="padding:1rem 1.25rem;">
              <div style="font-family:'Cormorant Garamond',serif;font-size:18px;font-weight:600;color:var(--cream);margin-bottom:6px;">Finding Your Soul</div>
              <div style="font-size:13px;color:var(--text-2);line-height:1.7;">This lesson dives into the soul — what it is across religion, philosophy, and psychology — and how to begin the process of remaking it. Through journaling, shadow work, and the principles of spiritual alchemy, you'll learn how to confront suppressed emotions, release past wounds, and reconnect with your authentic self. It also explores the role of psilocybin as a catalyst for deep inner transformation when used with intention and care.</div>
            </div>
          </div>

          <div style="background:var(--bg3);border:0.5px solid var(--border);border-radius:var(--radius);overflow:hidden;">
            <div style="aspect-ratio:16/9;background:#000;">
              <iframe width="100%" height="100%" src="https://www.youtube.com/embed/Zdgl4d-jYt8?rel=0&modestbranding=1" title="Mushroom Intro" allowfullscreen allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" style="display:block;border:none;"></iframe>
            </div>
            <div style="padding:1rem 1.25rem;">
              <div style="font-family:'Cormorant Garamond',serif;font-size:18px;font-weight:600;color:var(--cream);margin-bottom:6px;">Mushroom Intro</div>
              <div style="font-size:13px;color:var(--text-2);line-height:1.7;">Intro to psychedelic mushrooms with a quick overview of a study of the health risks and benefits of psilocybin for depression in terminal patients.</div>
            </div>
          </div>

          <div style="background:var(--bg3);border:0.5px solid var(--border);border-radius:var(--radius);overflow:hidden;">
            <div style="aspect-ratio:16/9;background:#000;">
              <iframe width="100%" height="100%" src="https://www.youtube.com/embed/HgGzTxEI7zc?rel=0&modestbranding=1" title="Spiritual Warfare" allowfullscreen allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" style="display:block;border:none;"></iframe>
            </div>
            <div style="padding:1rem 1.25rem;">
              <div style="font-family:'Cormorant Garamond',serif;font-size:18px;font-weight:600;color:var(--cream);margin-bottom:6px;">Spiritual Warfare</div>
              <div style="font-size:13px;color:var(--text-2);line-height:1.7;">An unflinching look at the unseen battle of energies, intentions, and influence that shape your reality every day. This lesson covers the Universal Laws of Vibration, Karma, Attraction, and Divine Oneness alongside the dark side — manipulation, NLP, gaslighting, the Dark Triad, and The Art of War. Understanding both sides of this warfare is the first step to protecting your energy, raising your vibration, and refusing to be a pawn in someone else's game.</div>
            </div>
          </div>

      </div>
    </div>
  </section>
</div>

<!-- ═══════════════ LIFE COACH PAGE ═══════════════ -->
<div id="page-coach" class="page">

  <div class="videos-hero">
    <div class="section-label">AI-Powered Guidance</div>
    <h1 class="section-title" style="max-width:700px;margin:0 auto .75rem;">KUEL <em>Life Coach</em></h1>
    <p class="section-body" style="margin:0 auto 2rem;">Your personal AI life coach — powered by Maslow's Hierarchy of Needs, hedonistic philosophy, and practical goal-setting to help you build your best life.</p>
    <div style="display:flex;flex-direction:column;align-items:center;gap:8px;">
      <a class="btn-primary" href="https://claude.ai/public/artifacts/df7873d5-05fc-41a1-adbc-8b7f41def6b2" target="_blank" rel="noopener" style="font-size:14px;padding:14px 36px;">Launch KUEL Life Coach ↗</a>
      <span style="font-size:11px;color:var(--text-3);font-style:italic;">(free claude.ai account required)</span>
    </div>
  </div>

  <section>
    <div class="section-inner">

      <!-- What it is -->
      <div style="margin-bottom:4rem;">
        <div class="section-label">What It Is</div>
        <h2 class="section-title">Your Personal <em>AI Guide</em></h2>
        <p class="section-body">The KUEL Life Coach is an AI agent that leverages Maslow's Human Hierarchy of Needs alongside your personal self-assessment, wants, and goals to deliver specific, personalized advice for moving toward your best life.</p>
        <br>
        <p class="section-body">It takes a <em style="color:var(--gold);">hedonistic approach to happiness</em> — helping you make the most out of life in ways that lift you up without harming yourself or others.</p>
        <br>
        <div style="display:grid;grid-template-columns:1fr 1fr;gap:1rem;margin-top:.5rem;">
          <div style="background:var(--bg3);border:0.5px solid var(--border);border-radius:var(--radius);padding:1.25rem 1.5rem;">
            <div style="font-size:22px;margin-bottom:.5rem;">📋</div>
            <div style="font-family:'Cormorant Garamond',serif;font-size:18px;font-weight:600;color:var(--cream);margin-bottom:.4rem;">Needs Assessment</div>
            <p style="font-size:13px;color:var(--text-2);line-height:1.65;">Score yourself across all five levels of Maslow's hierarchy — physical, security, belonging, esteem, and self-actualization — to reveal exactly where your growth opportunities lie.</p>
          </div>
          <div style="background:var(--bg3);border:0.5px solid var(--border);border-radius:var(--radius);padding:1.25rem 1.5rem;">
            <div style="font-size:22px;margin-bottom:.5rem;">🎯</div>
            <div style="font-family:'Cormorant Garamond',serif;font-size:18px;font-weight:600;color:var(--cream);margin-bottom:.4rem;">Goal Setting</div>
            <p style="font-size:13px;color:var(--text-2);line-height:1.65;">Define your dreams, long-term targets, short-term milestones, and daily habits. The coach uses everything you share to build a plan tailored specifically to you.</p>
          </div>
        </div>
      </div>

      <!-- Features highlight -->
      <div style="background:var(--bg2);border:0.5px solid var(--border);border-radius:var(--radius);padding:2rem 2.5rem;margin-bottom:3rem;">
        <div class="section-label">What You'll Receive</div>
        <div style="display:grid;grid-template-columns:1fr 1fr;gap:1rem;margin-top:1rem;">
          <div style="display:flex;gap:.75rem;align-items:flex-start;">
            <span style="color:var(--gold);font-size:16px;margin-top:2px;">📅</span>
            <div>
              <div style="font-size:13px;font-weight:500;color:var(--cream);margin-bottom:3px;">Calendar & Phone Integration</div>
              <div style="font-size:12px;color:var(--text-2);line-height:1.6;">Specific tips for Google Calendar, Apple Calendar, phone alarms, and habit-tracking apps — built around your actual goals.</div>
            </div>
          </div>
          <div style="display:flex;gap:.75rem;align-items:flex-start;">
            <span style="color:var(--gold);font-size:16px;margin-top:2px;">⏰</span>
            <div>
              <div style="font-size:13px;font-weight:500;color:var(--cream);margin-bottom:3px;">Scheduled Hour Blocks</div>
              <div style="font-size:12px;color:var(--text-2);line-height:1.6;">Dedicated time blocks for each goal with a curated list of ideas on how to achieve greatness during each session.</div>
            </div>
          </div>
          <div style="display:flex;gap:.75rem;align-items:flex-start;">
            <span style="color:var(--gold);font-size:16px;margin-top:2px;">🎯</span>
            <div>
              <div style="font-size:13px;font-weight:500;color:var(--cream);margin-bottom:3px;">Short-Term → Long-Term Roadmap</div>
              <div style="font-size:12px;color:var(--text-2);line-height:1.6;">Each short-term goal is connected to a long-term target with concrete actions, a timeframe, and a clear success metric.</div>
            </div>
          </div>
          <div style="display:flex;gap:.75rem;align-items:flex-start;">
            <span style="color:var(--gold);font-size:16px;margin-top:2px;">💬</span>
            <div>
              <div style="font-size:13px;font-weight:500;color:var(--cream);margin-bottom:3px;">Personal AI Coaching Chat</div>
              <div style="font-size:12px;color:var(--text-2);line-height:1.6;">An ongoing conversation that knows your needs, goals, and plan — ready to help you push through obstacles and stay on track.</div>
            </div>
          </div>
        </div>
      </div>

      <!-- CTA -->
      <div style="text-align:center;padding:2rem 0 1rem;">
        <div class="section-label" style="text-align:center;">Ready to Begin?</div>
        <h2 class="section-title" style="text-align:center;margin-bottom:1rem;">Start Your <em>Journey</em> Today</h2>
        <div style="display:flex;flex-direction:column;align-items:center;gap:8px;">
          <a class="btn-primary" href="https://claude.ai/public/artifacts/df7873d5-05fc-41a1-adbc-8b7f41def6b2" target="_blank" rel="noopener" style="font-size:14px;padding:14px 40px;">Launch KUEL Life Coach ↗</a>
          <span style="font-size:11px;color:var(--text-3);font-style:italic;">(free claude.ai account required)</span>
        </div>
      </div>

    </div>
  </section>
</div>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">KUEL Conditioning</div>
  <ul class="footer-links">
    <li><a onclick="showPage('home')">Home</a></li>
    <li><a onclick="showPage('course')">The Course</a></li>
    <li><a onclick="showPage('resources')">Resources</a></li>
    <li><a onclick="showPage('videos')">Videos</a></li>
    <li><a onclick="showPage('coach')">Life Coach</a></li>
  </ul>
  <div class="footer-bottom">© 2025 KUEL Conditioning<br><span style="font-size:10px;margin-top:4px;display:block;">kuelconditioning@gmail.com</span></div>
</footer>

<!-- ═══════════════ DOC MODALS ═══════════════ -->

<!-- MODAL: Doc 1 - Kode of Konduct -->
<div id="modal-doc1" class="doc-modal-overlay">
  <div class="doc-modal">
    <div class="doc-modal-toolbar">
      <span class="doc-modal-title">Document 1 — Kode of Konduct Kontract</span>
      <div class="doc-modal-actions">
        <button class="modal-print-btn" onclick="printModal('modal-doc1')">🖨 Print with Answers</button>
        <button class="modal-close-btn" onclick="closeModal('modal-doc1')">✕</button>
      </div>
    </div>
    <div class="doc-modal-body">
      <div class="doc-body-title">Kode of Konduct Kontract</div>
      <div class="doc-body-subtitle">KUEL Conditioning — Fill in all fields below, then print</div>

      <p class="doc-body-text">This Code of Conduct Contract is an agreement between <input class="doc-fill-field wide" placeholder="Spiritual Coach's Name" /> (the "Coach") and <input class="doc-fill-field wide" placeholder="Client's Name" /> (the "Client").</p>

      <div class="doc-section-title">1. Purpose</div>
      <p class="doc-body-text">The purpose of this Code of Conduct is to establish the ethical guidelines and professional standards that will govern the coaching relationship between the Coach and the Client.</p>

      <div class="doc-section-title">2. Ethical Principles</div>
      <p class="doc-body-text">The Coach and Client agree to adhere to the following ethical principles:</p>
      <p class="doc-bullet"><span class="doc-strong">Respect:</span> Treat one another with dignity, respect, and compassion, regardless of their background, beliefs, or circumstances.</p>
      <p class="doc-bullet"><span class="doc-strong">Confidentiality:</span> Maintain strict confidentiality of all information provided, except with explicit consent outlined in the Confidentiality Agreement.</p>
      <p class="doc-bullet"><span class="doc-strong">Integrity:</span> Act with honesty, integrity, and transparency in all professional dealings.</p>
      <p class="doc-bullet"><span class="doc-strong">Beneficence:</span> The Coach will work to promote the well-being of the Client and avoid causing harm.</p>
      <p class="doc-bullet"><span class="doc-strong">Dual Relationships:</span> The Coach will avoid dual relationships with the Client that could compromise professional judgment.</p>
      <p class="doc-bullet"><span class="doc-strong">Power Dynamics:</span> Be mindful of the power dynamics in the coaching relationship and avoid exploiting the Client.</p>
      <p class="doc-bullet"><span class="doc-strong">Conflict of Interest:</span> Disclose any potential conflicts of interest that could affect the coaching relationship.</p>

      <div class="doc-section-title">3. Client Responsibilities</div>
      <p class="doc-body-text">The Client agrees to:</p>
      <p class="doc-bullet"><span class="doc-strong">Respect for the Coach:</span> Treat the Coach with dignity, respect, and compassion.</p>
      <p class="doc-bullet"><span class="doc-strong">Openness and Honesty:</span> Communicate openly and honestly with the Coach, sharing relevant information and feelings. The goal is to see yourself clearly.</p>
      <p class="doc-bullet"><span class="doc-strong">Active Participation:</span> Actively participate in the coaching process, taking responsibility for their own growth and development.</p>
      <p class="doc-bullet"><span class="doc-strong">Substance Use:</span> Fast from mind and body altering substances during designated times that could impair judgment or ability to benefit from the coaching process.</p>
      <p class="doc-bullet"><span class="doc-strong">Respect for Boundaries:</span> Respect the boundaries established by the Coach, both professionally and personally.</p>
      <p class="doc-bullet"><span class="doc-strong">Scheduling:</span> Respect the Coach's time and make every effort to arrive on time for scheduled sessions.</p>
      <p class="doc-bullet"><span class="doc-strong">Cancellation Policy:</span> Follow the Coach's cancellation policy and provide timely notice if rescheduling or cancelling.</p>

      <div class="doc-section-title">4. Termination</div>
      <p class="doc-body-text">Either party may terminate the coaching relationship at any time. The Coach will terminate the coaching relationship when it is no longer beneficial or appropriate.</p>

      <div class="doc-section-title">5. Amendments</div>
      <p class="doc-body-text">This Code of Conduct may be amended in writing by mutual agreement of both parties.</p>
      <p class="doc-body-text" style="margin-top:1rem;">By signing below, the Coach and the Client acknowledge that they have read, understood, and agreed to the terms of this Code of Conduct.</p>

      <div class="doc-sig-block">
        <div class="doc-sig-col">
          <div class="sig-line"></div>
          <label>Coach's Signature</label>
          <input placeholder="Coach's Full Name" />
          <input type="date" style="margin-top:8px;" />
        </div>
        <div class="doc-sig-col">
          <div class="sig-line"></div>
          <label>Client's Signature</label>
          <input placeholder="Client's Full Name" />
          <input type="date" style="margin-top:8px;" />
        </div>
      </div>
    </div>
  </div>
</div>

<!-- MODAL: Doc 2 - Confidentiality Agreement -->
<div id="modal-doc2" class="doc-modal-overlay">
  <div class="doc-modal">
    <div class="doc-modal-toolbar">
      <span class="doc-modal-title">Document 2 — Confidentiality Agreement</span>
      <div class="doc-modal-actions">
        <button class="modal-print-btn" onclick="printModal('modal-doc2')">🖨 Print with Answers</button>
        <button class="modal-close-btn" onclick="closeModal('modal-doc2')">✕</button>
      </div>
    </div>
    <div class="doc-modal-body">
      <div class="doc-body-title">Confidentiality Agreement</div>
      <div class="doc-body-subtitle">KUEL Conditioning — Fill in all fields below, then print</div>

      <p class="doc-body-text">This Confidentiality Agreement ("Agreement") is made and entered into on this <input class="doc-fill-field short" placeholder="day" /> day of <input class="doc-fill-field" placeholder="Month" />, 20<input class="doc-fill-field short" placeholder="YY" />, by and between:</p>

      <p class="doc-body-text" style="margin-top:1rem;"><span class="doc-strong"><input class="doc-fill-field wide" placeholder="Coach's Full Name" /></span>, a professional Spirituality Coach, having their principal place of business at <input class="doc-fill-field wide" placeholder="Business Address" />, hereinafter referred to as the "Coach," and</p>

      <p class="doc-body-text"><span class="doc-strong"><input class="doc-fill-field wide" placeholder="Client's Full Name" /></span>, residing at <input class="doc-fill-field wide" placeholder="Client's Address" />, hereinafter referred to as the "Client."</p>

      <div class="doc-section-title">1. Purpose</div>
      <p class="doc-body-text">The purpose of this Agreement is to ensure that all information disclosed by the Client to the Coach during the coaching relationship, whether verbal, written, or in any other form, will be kept confidential and used solely for the benefit of the Client within the professional coaching relationship.</p>

      <div class="doc-section-title">2. Confidential Information</div>
      <p class="doc-body-text">"Confidential Information" means any personal, emotional, spiritual, or psychological information disclosed by the Client during coaching sessions. This includes discussions regarding the Client's spiritual beliefs, personal development goals, life experiences, and any materials shared by the Client that are not publicly known or available.</p>

      <div class="doc-section-title">3. Obligations of the Coach</div>
      <p class="doc-body-text">The Coach agrees to:</p>
      <p class="doc-bullet">Maintain the strict confidentiality of all Confidential Information shared by the Client.</p>
      <p class="doc-bullet">Not disclose any Confidential Information to any third party without the prior written consent of the Client, except as required by law.</p>
      <p class="doc-bullet">Use Confidential Information solely for the purpose of providing professional spiritual coaching services to the Client.</p>

      <div class="doc-section-title">4. Exceptions to Confidentiality</div>
      <p class="doc-body-text">This Agreement does not apply to information that:</p>
      <p class="doc-bullet">Is or becomes publicly available through no fault of the Coach.</p>
      <p class="doc-bullet">Is disclosed with the prior written consent of the Client.</p>
      <p class="doc-bullet">Is required to be disclosed by law, court order, or governmental regulation.</p>

      <div class="doc-section-title">5. Term of Confidentiality</div>
      <p class="doc-body-text">The confidentiality obligations will remain in effect for the duration of the coaching relationship and continue indefinitely after termination of coaching services, unless otherwise specified by law.</p>

      <div class="doc-section-title">6. Breach of Agreement</div>
      <p class="doc-body-text">In the event of a breach of this Agreement by the Coach, the Client may pursue any legal or equitable remedies available, including injunctive relief.</p>

      <div class="doc-section-title">7. Termination</div>
      <p class="doc-body-text">Either party may terminate this Agreement with prior written notice. Termination does not release the Coach from confidentiality obligations regarding information disclosed during the term of the Agreement.</p>

      <div class="doc-section-title">8. Governing Law</div>
      <p class="doc-body-text">This Agreement shall be governed by and construed in accordance with the laws of the state of <input class="doc-fill-field" placeholder="State" />, without regard to its conflict of law principles.</p>

      <div class="doc-section-title">9. Entire Agreement</div>
      <p class="doc-body-text">This Agreement constitutes the entire understanding between the parties with respect to the subject matter hereof and supersedes all prior discussions, agreements, or understandings of any kind.</p>

      <p class="doc-body-text" style="margin-top:1.5rem;"><span class="doc-strong">IN WITNESS WHEREOF</span>, the parties hereto have executed this Confidentiality Agreement as of the date first above written.</p>

      <div class="doc-sig-block">
        <div class="doc-sig-col">
          <div class="sig-line"></div>
          <label>Coach's Signature</label>
          <input placeholder="Coach's Full Name" />
          <input type="date" style="margin-top:8px;" />
        </div>
        <div class="doc-sig-col">
          <div class="sig-line"></div>
          <label>Client's Signature</label>
          <input placeholder="Client's Full Name" />
          <input type="date" style="margin-top:8px;" />
        </div>
      </div>
    </div>
  </div>
</div>

<!-- MODAL: Doc 4 - Needs Assessment & Goal Setting -->
<div id="modal-doc4" class="doc-modal-overlay">
  <div class="doc-modal">
    <div class="doc-modal-toolbar">
      <span class="doc-modal-title">Document 4 — Needs Assessment &amp; Goal Setting</span>
      <div class="doc-modal-actions">
        <button class="modal-print-btn" onclick="printModal('modal-doc4')">🖨 Print with Answers</button>
        <button class="modal-close-btn" onclick="closeModal('modal-doc4')">✕</button>
      </div>
    </div>
    <div class="doc-modal-body">
      <div class="doc-body-title">Needs Assessment</div>
      <div class="doc-body-subtitle">KUEL Conditioning · Score each need 1–10, then build your goals below</div>

      <p class="doc-body-text">Maslow's hierarchy of needs suggests people are motivated to fulfill fundamental needs in a hierarchical order — starting with basic physiological and safety needs before moving to higher-level needs for belonging, esteem, and self-actualization.</p>
      <p class="doc-body-text" style="font-style:italic;color:#8a6f2e;margin-top:.5rem;">How well are you meeting these needs? Score each 1–10.</p>

      <div style="display:grid;grid-template-columns:1fr 1fr;gap:1.5rem;margin-top:1.5rem;">

        <div style="background:rgba(201,168,76,.04);border:1px solid rgba(201,168,76,.2);border-radius:4px;padding:1.25rem;">
          <div class="doc-section-title" style="margin-top:0;">Physical Needs</div>
          <p class="doc-body-text" style="margin-bottom:.75rem;font-size:12px;color:#666;">Overall Score: <input class="doc-fill-field short" placeholder="1–10" /></p>
          <div style="display:flex;flex-direction:column;gap:6px;">
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Breathing</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Water</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Food</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Sleep</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Clothing</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Shelter</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
          </div>
        </div>

        <div style="background:rgba(201,168,76,.04);border:1px solid rgba(201,168,76,.2);border-radius:4px;padding:1.25rem;">
          <div class="doc-section-title" style="margin-top:0;">Security Needs</div>
          <p class="doc-body-text" style="margin-bottom:.75rem;font-size:12px;color:#666;">Overall Score: <input class="doc-fill-field short" placeholder="1–10" /></p>
          <div style="display:flex;flex-direction:column;gap:6px;">
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Health</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Personal Safety</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Employment</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Property</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Resources</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
          </div>
        </div>

        <div style="background:rgba(201,168,76,.04);border:1px solid rgba(201,168,76,.2);border-radius:4px;padding:1.25rem;">
          <div class="doc-section-title" style="margin-top:0;">Belonging Needs</div>
          <p class="doc-body-text" style="margin-bottom:.75rem;font-size:12px;color:#666;">Overall Score: <input class="doc-fill-field short" placeholder="1–10" /></p>
          <div style="display:flex;flex-direction:column;gap:6px;">
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Friendship</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Family</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Community</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Intimacy</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Sense of Connection</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
          </div>
        </div>

        <div style="background:rgba(201,168,76,.04);border:1px solid rgba(201,168,76,.2);border-radius:4px;padding:1.25rem;">
          <div class="doc-section-title" style="margin-top:0;">Esteem Needs</div>
          <p class="doc-body-text" style="margin-bottom:.75rem;font-size:12px;color:#666;">Overall Score: <input class="doc-fill-field short" placeholder="1–10" /></p>
          <div style="display:flex;flex-direction:column;gap:6px;">
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Achievements</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Self-Respect</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>External Admiration</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Strength</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Confidence</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Freedom</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
          </div>
        </div>

        <div style="background:rgba(201,168,76,.04);border:1px solid rgba(201,168,76,.2);border-radius:4px;padding:1.25rem;grid-column:1/-1;">
          <div class="doc-section-title" style="margin-top:0;">Self-Actualization</div>
          <p class="doc-body-text" style="margin-bottom:.75rem;font-size:12px;color:#666;">Overall Score: <input class="doc-fill-field short" placeholder="1–10" /></p>
          <div style="display:grid;grid-template-columns:repeat(3,1fr);gap:6px;">
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Morality</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Acceptance</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Creativity</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Find Meaning in Life</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Live with Purpose</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Being Present</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
            <div style="display:flex;justify-content:space-between;align-items:center;font-size:13px;"><span>Realize Fullest Potential</span><input class="doc-fill-field short" placeholder="1–10" style="min-width:60px;text-align:center;" /></div>
          </div>
        </div>
      </div>

      <p class="doc-body-text" style="margin-top:1.5rem;padding:10px 14px;background:rgba(201,168,76,.08);border-left:3px solid #c9a84c;border-radius:0 3px 3px 0;">If any of these fall below a 7 they can potentially be the cause of physical or emotional distress. Once you identify gaps, create a plan to ensure all your needs get met on the path to lasting happiness.</p>

      <div class="doc-section-title" style="margin-top:2rem;">Areas to Improve (scores below 7)</div>
      <textarea placeholder="List the needs where you scored below 7 and briefly describe why..." style="width:100%;min-height:70px;border:1.5px solid #c9a84c;border-radius:3px;padding:8px;resize:vertical;font-family:'DM Sans',sans-serif;font-size:13px;color:#1a1a1a;background:rgba(201,168,76,.04);outline:none;"></textarea>

      <div class="doc-body-title" style="font-size:20px;margin-top:2.5rem;">Goal Setting</div>
      <p class="doc-body-text" style="margin-top:.5rem;">Goals should help meet your needs, improve yourself, and elevate your community. Set 3 or more goals for each timeframe below.</p>

      <div class="doc-section-title" style="margin-top:1.5rem;">Dreams to Manifest</div>
      <p class="doc-body-text" style="font-size:12px;color:#666;margin-bottom:.5rem;">Visions of your best life to create in reality.</p>
      <textarea placeholder="Write your dreams and visions here..." style="width:100%;min-height:80px;border:1.5px solid #c9a84c;border-radius:3px;padding:8px;resize:vertical;font-family:'DM Sans',sans-serif;font-size:13px;color:#1a1a1a;background:rgba(201,168,76,.04);outline:none;"></textarea>

      <div class="doc-section-title" style="margin-top:1.25rem;">Long Term Goals</div>
      <p class="doc-body-text" style="font-size:12px;color:#666;margin-bottom:.5rem;">Goals to add to shorter term goals in due time.</p>
      <textarea placeholder="1. &#10;2. &#10;3. " style="width:100%;min-height:80px;border:1.5px solid #c9a84c;border-radius:3px;padding:8px;resize:vertical;font-family:'DM Sans',sans-serif;font-size:13px;color:#1a1a1a;background:rgba(201,168,76,.04);outline:none;"></textarea>

      <div class="doc-section-title" style="margin-top:1.25rem;">Short Term Goals</div>
      <p class="doc-body-text" style="font-size:12px;color:#666;margin-bottom:.5rem;">Prioritize what you must or might complete in the near future.</p>
      <textarea placeholder="1. &#10;2. &#10;3. " style="width:100%;min-height:80px;border:1.5px solid #c9a84c;border-radius:3px;padding:8px;resize:vertical;font-family:'DM Sans',sans-serif;font-size:13px;color:#1a1a1a;background:rgba(201,168,76,.04);outline:none;"></textarea>

      <div class="doc-section-title" style="margin-top:1.25rem;">Daily Tasks</div>
      <p class="doc-body-text" style="font-size:12px;color:#666;margin-bottom:.5rem;">Better your quality of life through responsibility to self and community. Reset daily.</p>
      <textarea placeholder="1. &#10;2. &#10;3. " style="width:100%;min-height:80px;border:1.5px solid #c9a84c;border-radius:3px;padding:8px;resize:vertical;font-family:'DM Sans',sans-serif;font-size:13px;color:#1a1a1a;background:rgba(201,168,76,.04);outline:none;"></textarea>

      <div style="margin-top:1.5rem;display:flex;gap:1rem;align-items:center;">
        <span style="font-size:12px;color:#888;">Name:</span>
        <input class="doc-fill-field" placeholder="Your name" style="flex:1;" />
        <span style="font-size:12px;color:#888;">Date:</span>
        <input type="date" class="doc-fill-field" style="flex:1;" />
      </div>
    </div>
  </div>
</div>

<script>
function toggleDropdown() {
  const menu = document.getElementById('dropdown-menu');
  menu.style.display = menu.style.display === 'block' ? 'none' : 'block';
}
function closeDropdown() {
  document.getElementById('dropdown-menu').style.display = 'none';
}
document.addEventListener('click', function(e) {
  const btn = document.getElementById('hamburger-btn');
  const menu = document.getElementById('dropdown-menu');
  if (menu && btn && !btn.contains(e.target) && !menu.contains(e.target)) {
    menu.style.display = 'none';
  }
});
function showPage(id) {
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.getElementById('page-' + id).classList.add('active');
  document.querySelectorAll('.nav-links a').forEach(a => a.classList.remove('active'));
  const el = document.getElementById('nav-' + id);
  if (el) el.classList.add('active');
  window.scrollTo({ top: 0, behavior: 'smooth' });
}
function scrollSec(id) {
  setTimeout(() => {
    const el = document.getElementById(id);
    if (el) el.scrollIntoView({ behavior: 'smooth', block: 'start' });
  }, 120);
}
function openModal(id) {
  document.getElementById('modal-' + id).classList.add('open');
  document.body.style.overflow = 'hidden';
}
function closeModal(id) {
  document.getElementById('modal-' + id).classList.remove('open');
  document.body.style.overflow = '';
}
function printModal(modalId) {
  const modal = document.getElementById(modalId);
  const body = modal.querySelector('.doc-modal-body').innerHTML;
  const title = modal.querySelector('.doc-modal-title').textContent;
  const w = window.open('', '_blank');
  w.document.write(`<!DOCTYPE html><html><head><title>${title}</title>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500&family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;1,400&display=swap" rel="stylesheet">
  <style>
    *{box-sizing:border-box;margin:0;padding:0;}
    body{font-family:'DM Sans',sans-serif;padding:2rem 3rem;color:#1a1a1a;background:#fff;}
    .doc-body-title{font-family:'Cormorant Garamond',serif;font-size:26px;font-weight:600;text-align:center;margin-bottom:.5rem;}
    .doc-body-subtitle{font-size:11px;text-align:center;color:#666;margin-bottom:2rem;letter-spacing:.05em;}
    .doc-section-title{font-size:12px;font-weight:600;margin:1.5rem 0 .5rem;text-transform:uppercase;letter-spacing:.08em;}
    .doc-body-text{font-size:13px;line-height:1.8;color:#333;margin-bottom:.6rem;}
    .doc-fill-field{display:inline-block;border:none;border-bottom:1px solid #333;background:transparent;font-size:13px;font-family:'DM Sans',sans-serif;color:#1a1a1a;padding:2px 4px;min-width:160px;}
    .doc-fill-field.wide{min-width:220px;}
    .doc-fill-field.short{min-width:60px;}
    .doc-bullet{font-size:13px;line-height:1.8;color:#333;padding-left:1.25rem;position:relative;margin-bottom:.3rem;}
    .doc-bullet::before{content:'—';position:absolute;left:0;color:#8a6f2e;}
    .doc-strong{font-weight:600;}
    .doc-sig-block{display:grid;grid-template-columns:1fr 1fr;gap:2rem;margin-top:2.5rem;padding-top:1.5rem;border-top:1px solid #ddd;}
    .doc-sig-col .sig-line{border-bottom:1px solid #333;height:40px;margin-bottom:6px;}
    .doc-sig-col label{font-size:11px;color:#666;}
    .doc-sig-col input{width:100%;border:none;border-bottom:1px solid #333;background:transparent;font-size:13px;padding:2px 4px;color:#1a1a1a;}
    textarea{width:100%;border:1px solid #ccc;padding:6px;font-size:13px;font-family:'DM Sans',sans-serif;resize:none;background:rgba(201,168,76,.04);}
    @media print{body{padding:1rem 2rem;}}
  </style></head><body>${body}<script>window.onload=function(){window.print();}<\/script></body></html>`);
  w.document.close();
}
// Close modal on overlay click
document.querySelectorAll('.doc-modal-overlay').forEach(overlay => {
  overlay.addEventListener('click', function(e) {
    if (e.target === this) closeModal(this.id.replace('modal-',''));
  });
});

// ESC key
document.addEventListener('keydown', e => {
  if (e.key === 'Escape') {
    document.querySelectorAll('.doc-modal-overlay.open').forEach(m => {
      closeModal(m.id.replace('modal-',''));
    });
  }
});
</script>
</body>
</html>
