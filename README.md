<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Tech Is Not Utopia — A Static Manifesto</title>
  <meta name="description" content="A short static webpage exploring why technology alone won't create a perfect society — it amplifies human choices, for better and worse." />
  <link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Crect width='100' height='100' fill='%230f172a'/%3E%3Ctext x='50' y='58' font-size='50' text-anchor='middle' fill='%23fff' font-family='Arial'%3ET%3C/text%3E%3C/svg%3E">
  <style>
    :root{
      --bg:#0f172a; --card:#0b1220; --muted:#94a3b8; --accent:#7c3aed; --glass: rgba(255,255,255,0.04);
      --maxw:1100px; --radius:18px;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0; font-family:Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      background: radial-gradient(1200px 600px at 10% 10%, rgba(124,58,237,0.08), transparent),
                  linear-gradient(180deg,#071026 0%,var(--bg) 60%);
      color:#e6eef8; -webkit-font-smoothing:antialiased; -moz-osx-font-smoothing:grayscale;
      line-height:1.45; padding:48px 24px;
      display:flex; justify-content:center;
    }
    .container{max-width:var(--maxw); width:100%;}

    header{display:flex;align-items:center;justify-content:space-between;margin-bottom:28px}
    .brand{display:flex;gap:12px;align-items:center}
    .logo{width:56px;height:56px;border-radius:12px;background:linear-gradient(135deg,var(--accent),#06b6d4);display:flex;align-items:center;justify-content:center;box-shadow:0 6px 20px rgba(12,18,38,0.6)}
    .logo svg{width:32px;height:32px}
    h1.site-title{font-size:18px;margin:0}
    p.tag{margin:0;color:var(--muted);font-size:13px}

    nav a{color:var(--muted);text-decoration:none;margin-left:18px;font-size:14px}

    .hero{display:grid;grid-template-columns:1fr 420px;gap:28px;align-items:center;margin-bottom:36px}
    .card{background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent); padding:28px;border-radius:var(--radius);box-shadow:0 10px 30px rgba(2,6,23,0.6);backdrop-filter: blur(6px);}

    .kicker{display:inline-block;padding:6px 10px;border-radius:999px;background:var(--glass);color:var(--accent);font-weight:600;font-size:13px}
    h2{font-size:36px;margin:14px 0 10px}
    p.lead{color:var(--muted);font-size:16px;margin:0}

    /* SVG scene */
    .scene{width:100%;height:100%;display:flex;align-items:center;justify-content:center}
    .scene svg{max-width:100%;height:auto;display:block}

    /* Arguments grid */
    .grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px;margin-top:18px}
    .pill{padding:18px;border-radius:12px;background:linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.02));border:1px solid rgba(255,255,255,0.03)}
    .pill h3{margin:0 0 8px}
    .pill p{margin:0;color:var(--muted);font-size:14px}

    /* Examples / cards */
    .examples{display:grid;grid-template-columns:1fr 1fr;gap:16px;margin-top:18px}
    .example{padding:16px;border-radius:12px;background:linear-gradient(90deg, rgba(255,255,255,0.015), transparent);border:1px solid rgba(255,255,255,0.025)}
    .example h4{margin:0 0 8px}
    .example p{margin:0;color:var(--muted);font-size:14px}

    footer{margin-top:30px;color:var(--muted);font-size:13px;display:flex;justify-content:space-between;align-items:center}

    /* responsive */
    @media (max-width:980px){
      .hero{grid-template-columns:1fr}
      .grid{grid-template-columns:1fr}
      .examples{grid-template-columns:1fr}
    }

    /* small niceties */
    .cta{display:inline-block;margin-top:12px;padding:10px 14px;border-radius:10px;background:linear-gradient(90deg,var(--accent),#06b6d4);color:#061024;font-weight:700;text-decoration:none}
    .muted{color:var(--muted)}

    /* accessibility */
    @media (prefers-reduced-motion: reduce){*{animation:none!important;transition:none!important}}

    /* subtle animated glitch for the word 'UTOPIA' */
    .glitch{position:relative;display:inline-block}
    .glitch::before,.glitch::after{content:attr(data-text);position:absolute;left:0;top:0;mix-blend-mode:screen;opacity:0.9}
    .glitch::before{color:#ffb86b;transform:translate(-1px, -1px);clip-path:polygon(0 0,100% 0,100% 40%,0 40%)}
    .glitch::after{color:#7ef0c7;transform:translate(1px,1px);clip-path:polygon(0 60%,100% 60%,100% 100%,0 100%)}
    @media (prefers-reduced-motion: no-preference){
      .glitch::before{animation:glitchTop 2.1s infinite linear}
      .glitch::after{animation:glitchBottom 2.5s infinite linear}
    }
    @keyframes glitchTop{0%{transform:translate(0,0)}20%{transform:translate(-2px,-2px)}40%{transform:translate(0,0)}60%{transform:translate(-1px,-1px)}100%{transform:translate(0,0)}}
    @keyframes glitchBottom{0%{transform:translate(0,0)}25%{transform:translate(2px,2px)}50%{transform:translate(0,0)}75%{transform:translate(1px,1px)}100%{transform:translate(0,0)}}

    /* small print / print-friendly */
    @media print{body{background:white;color:black} .card{background:transparent;box-shadow:none;border-radius:0}}
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo" aria-hidden="true">
          <svg viewBox="0 0 24 24" fill="none" aria-hidden="true"><rect x="3" y="3" width="18" height="18" rx="5" fill="white" opacity="0.06"/><path d="M7 13h10M7 8h10" stroke="#fff" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round" opacity="0.95"/></svg>
        </div>
        <div>
          <h1 class="site-title">Tech Is Not Utopia</h1>
          <p class="tag">A brief, honest look at technology's limits and responsibilities</p>
        </div>
      </div>
      <nav aria-label="Main navigation">
        <a href="#why">Why it fails</a>
        <a href="#examples">Examples</a>
        <a href="#act">Act</a>
      </nav>
    </header>

    <main class="hero">
      <section class="card" aria-labelledby="hero-heading">
        <span class="kicker">Manifesto</span>
        <h2 id="hero-heading">When we say <span class="glitch" data-text="UTOPIA">UTOPIA</span>, we mean human choices — amplified.</h2>
        <p class="lead">Technology doesn't arrive with built-in ethics. It scales values: it can liberate and it can exclude, it can heal and it can surveil. This page collects the reasons we should treat tech with caution, care, and democratic stewardship.</p>

        <div class="grid" id="why" aria-label="Main arguments">
          <article class="pill" aria-labelledby="p1"><h3 id="p1">1. Tech Amplifies Power</h3><p>Tools magnify intent. Without checks, systems entrench those who already hold resources and influence.</p></article>
          <article class="pill" aria-labelledby="p2"><h3 id="p2">2. Not Everyone Benefits</h3><p>Design choices and access barriers create winners and losers — often along existing social divides.</p></article>
          <article class="pill" aria-labelledby="p3"><h3 id="p3">3. Environmental & Human Cost</h3><p>Behind every data center and device lie resource extraction, energy use, and labor — costs that aren't free.</p></article>
        </div>

        <div class="examples" id="examples" aria-label="Concrete examples">
          <div class="example"><h4>Surveillance at scale</h4><p class="muted">Data-driven monitoring can deter crime but also chill speech and target minorities when used without oversight.</p></div>
          <div class="example"><h4>Algorithmic bias</h4><p class="muted">Machine learning trained on biased data reproduces and sometimes amplifies discrimination in hiring, lending, and policing.</p></div>
        </div>

        <a class="cta" href="#act">How to act — read on</a>
      </section>

      <aside class="card scene" aria-hidden="false">
        <!-- SVG illustration: stylized city + glitch/clouds to convey imperfect tech -->
        <svg viewBox="0 0 600 400" role="img" aria-label="Illustration: stylized cityscape with data lines and cracks">
          <defs>
            <linearGradient id="gA" x1="0" x2="1"><stop offset="0" stop-color="#7c3aed" stop-opacity="0.9"/><stop offset="1" stop-color="#06b6d4" stop-opacity="0.9"/></linearGradient>
          </defs>
          <rect width="600" height="400" rx="16" fill="url(#gA)" opacity="0.08"/>
          <!-- buildings -->
          <g transform="translate(40,60)" fill="#081226">
            <rect x="0" y="80" width="60" height="160" rx="4"/>
            <rect x="80" y="40" width="48" height="200" rx="4"/>
            <rect x="150" y="100" width="100" height="140" rx="4"/>
            <rect x="270" y="60" width="70" height="180" rx="4"/>
            <rect x="360" y="90" width="60" height="150" rx="4"/>
          </g>
          <!-- data streams -->
          <g stroke="#9be7ff" stroke-opacity="0.85" stroke-width="1.6" fill="none" stroke-linecap="round">
            <path d="M20 200 C 180 110, 260 140, 560 60" stroke-opacity="0.12" />
            <path d="M20 230 C 160 150, 300 170, 560 120" stroke-opacity="0.08" />
            <g stroke-opacity="0.6">
              <path d="M60 190 L80 180 L100 190 L130 170 L170 175"/>
            </g>
          </g>
          <!-- cracks / glitch -->
          <g stroke="#ffb86b" stroke-width="2" stroke-opacity="0.9" fill="none">
            <path d="M200 300 L220 285 L240 295 L260 274" stroke-opacity="0.9"/>
            <path d="M320 320 L340 305 L360 315" stroke-opacity="0.7"/>
          </g>
          <!-- foreground text -->
          <g transform="translate(40,270)" fill="#e6eef8" font-family="Segoe UI, Roboto, Arial">
            <text x="0" y="0" font-size="26">Tech</text>
            <text x="0" y="28" font-size="18" fill="#b7c2d6">is a lever — not a destiny</text>
          </g>
        </svg>
      </aside>
    </main>

    <section class="card" aria-labelledby="act">
      <h2 id="act">What we can do</h2>
      <p class="muted">Skepticism isn't nihilism. It means building institutions, policies, and habits that steer technology toward shared benefit.</p>
      <ul>
        <li><strong>Regulate and audit:</strong> independent audits and clear rules for high-impact systems.</li>
        <li><strong>Design for inclusion:</strong> participatory design, accessible interfaces, and data that represent many lives.</li>
        <li><strong>Measure externalities:</strong> account for environmental and labor costs in product decisions.</li>
      </ul>

      <p class="muted">Want to use this page as a handout or start a conversation? Copy, remix, and share. This is intentionally minimal — a seed for discussion, not an answer.</p>
    </section>

    <footer>
      <div>© <span id="year">2025</span> Tech Is Not Utopia</div>
      <div class="muted">Built with honesty • Accessible • Static</div>
    </footer>
  </div>

  <script>
    // small runtime: update year and provide a focus outline improvement
    document.getElementById('year').textContent = new Date().getFullYear();

    // keyboard-visible focus for better accessibility
    (function(){
      function handleFirstTab(e){ if(e.key === 'Tab'){ document.documentElement.classList.add('user-is-tabbing'); window.removeEventListener('keydown', handleFirstTab); }}
      window.addEventListener('keydown', handleFirstTab);
    })();
  </script>
</body>
</html>
