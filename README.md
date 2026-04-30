# ukaverse
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ukaverse — Yiheng (Uka) Zhu</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;0,9..144,500;1,9..144,300;1,9..144,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">

<style>
:root {
  --bg: #fafaf8;
  --bg-warm: #f5f3ee;
  --text: #111010;
  --text-mid: #444340;
  --text-light: #888785;
  --text-xlight: #bbb9b5;
  --accent: #d4500a;
  --accent-dim: rgba(212,80,10,0.08);
  --border: #e8e5df;
  --border-mid: #d4d0c9;
}

* { margin: 0; padding: 0; box-sizing: border-box; }

html { scroll-behavior: smooth; }

body {
  font-family: 'DM Sans', sans-serif;
  background: var(--bg);
  color: var(--text);
  font-size: 16px;
  line-height: 1.6;
  -webkit-font-smoothing: antialiased;
}

/* ── NAV ── */
nav {
  position: fixed; top: 0; left: 0; right: 0; z-index: 100;
  padding: 1.1rem 2.5rem;
  display: flex; align-items: center; justify-content: space-between;
  background: rgba(250,250,248,0.9);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid var(--border);
}
.nav-logo {
  font-family: 'DM Sans', sans-serif;
  font-weight: 500; font-size: 0.95rem;
  color: var(--text); text-decoration: none;
  letter-spacing: -0.01em;
}
.nav-logo span { color: var(--accent); }
.nav-links { display: flex; gap: 2rem; list-style: none; }
.nav-links a {
  color: var(--text-light); text-decoration: none;
  font-size: 0.85rem; font-weight: 400;
  transition: color 0.2s;
}
.nav-links a:hover { color: var(--text); }

/* ── WRAPPER ── */
.page { max-width: 760px; margin: 0 auto; padding: 0 2.5rem; }

/* ── HERO ── */
.hero {
  padding: 9rem 0 5rem;
  border-bottom: 1px solid var(--border);
}
.hero-tag {
  display: inline-flex; align-items: center; gap: 0.5rem;
  font-size: 0.75rem; font-weight: 500; letter-spacing: 0.08em;
  text-transform: uppercase; color: var(--text-light);
  margin-bottom: 2rem;
}
.hero-tag::before {
  content: '';
  display: inline-block; width: 20px; height: 1px;
  background: var(--accent);
}
.hero h1 {
  font-family: 'Fraunces', serif;
  font-size: clamp(2rem, 5vw, 3.2rem);
  font-weight: 300; line-height: 1.18;
  letter-spacing: -0.03em;
  color: var(--text);
  margin-bottom: 1.5rem;
  max-width: 640px;
}
.hero h1 em {
  font-style: italic;
  color: var(--accent);
}
.hero-sub {
  font-size: 1rem; color: var(--text-mid);
  max-width: 480px; line-height: 1.7;
  margin-bottom: 2.5rem;
  font-weight: 300;
}
.hero-sub strong { color: var(--text); font-weight: 500; }
.hero-actions { display: flex; gap: 1rem; align-items: center; flex-wrap: wrap; }
.btn-primary {
  display: inline-flex; align-items: center; gap: 0.4rem;
  padding: 0.65rem 1.4rem;
  background: var(--text); color: var(--bg);
  font-family: 'DM Sans', sans-serif;
  font-size: 0.85rem; font-weight: 500;
  border-radius: 4px; text-decoration: none;
  transition: background 0.2s, transform 0.15s;
  letter-spacing: 0.01em;
}
.btn-primary:hover { background: var(--accent); transform: translateY(-1px); }
.btn-ghost {
  display: inline-flex; align-items: center; gap: 0.4rem;
  padding: 0.65rem 1.4rem;
  border: 1px solid var(--border-mid); color: var(--text-mid);
  font-family: 'DM Sans', sans-serif;
  font-size: 0.85rem; font-weight: 400;
  border-radius: 4px; text-decoration: none;
  transition: border-color 0.2s, color 0.2s;
}
.btn-ghost:hover { border-color: var(--text); color: var(--text); }

/* ── SECTION BASE ── */
section { padding: 4.5rem 0; border-bottom: 1px solid var(--border); }
.section-header {
  display: flex; align-items: baseline; gap: 1rem;
  margin-bottom: 3rem;
}
.section-num {
  font-size: 0.72rem; font-weight: 500; color: var(--accent);
  letter-spacing: 0.08em;
}
.section-title {
  font-family: 'Fraunces', serif;
  font-size: 1.35rem; font-weight: 400;
  letter-spacing: -0.02em; color: var(--text);
}

/* ── WHAT I DO ── */
.capabilities { display: flex; flex-direction: column; gap: 0; }
.cap-item {
  display: grid; grid-template-columns: 200px 1fr;
  gap: 2rem; align-items: start;
  padding: 1.75rem 0;
  border-bottom: 1px solid var(--border);
}
.cap-item:last-child { border-bottom: none; }
.cap-label {
  font-family: 'DM Sans', sans-serif;
  font-size: 0.82rem; font-weight: 500;
  color: var(--text-light); letter-spacing: 0.04em;
  text-transform: uppercase; padding-top: 0.15rem;
}
.cap-content h3 {
  font-family: 'Fraunces', serif;
  font-size: 1.15rem; font-weight: 400;
  letter-spacing: -0.02em; color: var(--text);
  margin-bottom: 0.5rem;
}
.cap-content p {
  font-size: 0.9rem; color: var(--text-mid);
  line-height: 1.7; font-weight: 300;
}

/* ── SELECTED WORK ── */
.work-list { display: flex; flex-direction: column; gap: 0; }
.work-item {
  padding: 2.25rem 0;
  border-bottom: 1px solid var(--border);
  display: grid; grid-template-columns: 1fr 2fr;
  gap: 2.5rem; align-items: start;
}
.work-item:last-child { border-bottom: none; }
.work-meta {}
.work-tag {
  display: inline-block;
  font-size: 0.68rem; font-weight: 500;
  letter-spacing: 0.08em; text-transform: uppercase;
  color: var(--accent);
  border: 1px solid rgba(212,80,10,0.25);
  padding: 0.2rem 0.55rem; border-radius: 3px;
  margin-bottom: 0.75rem;
}
.work-org {
  font-family: 'Fraunces', serif;
  font-size: 1.05rem; font-weight: 400;
  letter-spacing: -0.02em; color: var(--text);
  line-height: 1.3; margin-bottom: 0.3rem;
}
.work-period {
  font-size: 0.78rem; color: var(--text-xlight);
  font-weight: 400;
}
.work-body {}
.work-context {
  font-size: 0.82rem; color: var(--text-light);
  font-weight: 400; margin-bottom: 0.75rem;
  font-style: italic;
}
.work-what {
  font-size: 0.92rem; color: var(--text-mid);
  line-height: 1.72; font-weight: 300;
  margin-bottom: 1rem;
}
.work-impact {
  display: flex; flex-wrap: wrap; gap: 0.5rem;
  margin-bottom: 1rem;
}
.impact-chip {
  font-size: 0.78rem; font-weight: 500;
  padding: 0.3rem 0.75rem;
  background: var(--bg-warm);
  border: 1px solid var(--border);
  border-radius: 3px; color: var(--text-mid);
}
.work-link {
  font-size: 0.8rem; color: var(--accent);
  text-decoration: none; font-weight: 500;
  display: inline-flex; align-items: center; gap: 0.3rem;
  transition: gap 0.2s;
}
.work-link:hover { gap: 0.5rem; }

/* ── EVENTS SECTION ── */
.events-intro {
  font-size: 0.95rem; color: var(--text-mid);
  line-height: 1.75; font-weight: 300;
  max-width: 560px; margin-bottom: 2.5rem;
}
.events-stat-row {
  display: flex; gap: 2.5rem; flex-wrap: wrap;
  padding: 1.5rem 1.75rem;
  background: var(--bg-warm); border: 1px solid var(--border);
  border-radius: 6px; margin-bottom: 2.5rem;
}
.e-stat {}
.e-stat-num {
  font-family: 'Fraunces', serif;
  font-size: 1.8rem; font-weight: 300;
  color: var(--accent); line-height: 1;
  letter-spacing: -0.03em;
}
.e-stat-label {
  font-size: 0.75rem; color: var(--text-light); font-weight: 400;
  margin-top: 0.2rem;
}
.event-categories { display: flex; flex-direction: column; gap: 2rem; }
.event-category-title {
  font-size: 0.72rem; font-weight: 500;
  letter-spacing: 0.1em; text-transform: uppercase;
  color: var(--text-xlight); margin-bottom: 1rem;
  padding-bottom: 0.5rem;
  border-bottom: 1px solid var(--border);
}
.event-grid {
  display: flex; flex-direction: column; gap: 0;
}
.event-row {
  display: flex; align-items: center; justify-content: space-between;
  padding: 0.9rem 0;
  border-bottom: 1px solid var(--border);
  gap: 1rem;
}
.event-row:last-child { border-bottom: none; }
.event-name {
  font-size: 0.88rem; color: var(--text);
  font-weight: 400; flex: 1;
  line-height: 1.4;
}
.event-partner {
  font-size: 0.75rem; color: var(--text-light);
  white-space: nowrap;
}
.event-luma {
  font-size: 0.75rem; color: var(--accent);
  text-decoration: none; white-space: nowrap;
  transition: opacity 0.2s;
}
.event-luma:hover { opacity: 0.7; }

/* ── HOW I THINK ── */
.thoughts { display: flex; flex-direction: column; gap: 0; }
.thought-item {
  padding: 2rem 0;
  border-bottom: 1px solid var(--border);
  display: grid; grid-template-columns: 160px 1fr;
  gap: 2rem;
}
.thought-item:last-child { border-bottom: none; }
.thought-theme {
  font-size: 0.75rem; font-weight: 500;
  color: var(--text-xlight); letter-spacing: 0.07em;
  text-transform: uppercase; padding-top: 0.2rem;
}
.thought-content p {
  font-family: 'Fraunces', serif;
  font-size: 1rem; font-weight: 300;
  line-height: 1.75; color: var(--text-mid);
  font-style: italic; letter-spacing: -0.01em;
}
.thought-content p strong {
  color: var(--text); font-weight: 400; font-style: normal;
}

/* ── CONTACT ── */
.contact-block {
  display: flex; flex-direction: column; gap: 2rem;
}
.contact-line {
  font-family: 'Fraunces', serif;
  font-size: 1.5rem; font-weight: 300;
  letter-spacing: -0.03em; color: var(--text);
  line-height: 1.3;
}
.contact-line em { font-style: italic; color: var(--accent); }
.contact-email {
  display: inline-flex; align-items: center; gap: 0.5rem;
  font-size: 1rem; color: var(--text); text-decoration: none;
  border-bottom: 1px solid var(--border-mid);
  padding-bottom: 0.1rem;
  transition: border-color 0.2s, color 0.2s;
}
.contact-email:hover { color: var(--accent); border-color: var(--accent); }
.social-row {
  display: flex; gap: 1.5rem; flex-wrap: wrap;
  padding-top: 1rem; border-top: 1px solid var(--border);
}
.social-link {
  font-size: 0.82rem; color: var(--text-light);
  text-decoration: none;
  transition: color 0.2s;
  display: flex; align-items: center; gap: 0.3rem;
}
.social-link:hover { color: var(--text); }

/* ── FOOTER ── */
footer {
  padding: 2rem 0;
  display: flex; align-items: center; justify-content: space-between;
  flex-wrap: wrap; gap: 1rem;
}
.footer-text {
  font-size: 0.78rem; color: var(--text-xlight);
}
.footer-badge {
  font-size: 0.72rem; color: var(--text-xlight);
  display: flex; align-items: center; gap: 0.4rem;
}
.footer-badge::before {
  content: '';
  width: 5px; height: 5px; border-radius: 50%;
  background: #4ade80;
}

/* ── RESPONSIVE ── */
@media (max-width: 600px) {
  nav { padding: 1rem 1.25rem; }
  .nav-links { gap: 1.25rem; }
  .page { padding: 0 1.25rem; }
  .hero { padding: 7rem 0 3.5rem; }
  .cap-item, .work-item, .thought-item {
    grid-template-columns: 1fr;
    gap: 0.75rem;
  }
  .cap-label { font-size: 0.72rem; }
  .work-impact { gap: 0.4rem; }
}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a class="nav-logo" href="#">Uka<span>verse</span></a>
  <ul class="nav-links">
    <li><a href="#work">Work</a></li>
    <li><a href="#events">Events</a></li>
    <li><a href="#thinking">Thinking</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<main class="page">

  <!-- ── HERO ── -->
  <div class="hero">
    <div class="hero-tag">Ecosystem Builder · NYC</div>
    <h1>
      Complex systems.<br>
      Clear strategy.<br>
      <em>Real execution.</em>
    </h1>
    <p class="hero-sub">
      I work where ideas become infrastructure —
      building ecosystems in <strong>Web3 and AI</strong>,
      translating ambiguity into strategy,
      and connecting people who should already know each other.
    </p>
    <div class="hero-actions">
      <a href="#work" class="btn-primary">View Work →</a>
      <a href="mailto:yz11354@nyu.edu" class="btn-ghost">Get in Touch</a>
    </div>
  </div>

  <!-- ── WHAT I DO ── -->
  <section id="capabilities">
    <div class="section-header">
      <span class="section-num">01</span>
      <h2 class="section-title">What I Do</h2>
    </div>
    <div class="capabilities">
      <div class="cap-item">
        <div class="cap-label">Ecosystem Building</div>
        <div class="cap-content">
          <h3>I build communities that actually do things.</h3>
          <p>Not just audiences — operational networks. I connect students with industry, ideas with capital, and builders with each other. At NYU Blockchain Lab, I turned a student org into a recognized node in NYC's digital assets ecosystem.</p>
        </div>
      </div>
      <div class="cap-item">
        <div class="cap-label">Strategy & Execution</div>
        <div class="cap-content">
          <h3>I operate well in undefined environments.</h3>
          <p>Given ambiguity, I build structure. Given structure, I find the gaps. As Chief of Staff at a DeFi protocol, I translated product mechanics into market narrative — and made sure the execution matched the vision.</p>
        </div>
      </div>
      <div class="cap-item">
        <div class="cap-label">Market Translation</div>
        <div class="cap-content">
          <h3>I make complex things legible without losing precision.</h3>
          <p>Research on ETF-era Bitcoin. GTM for yield protocols. Content that treats the audience as intelligent. The skill isn't simplification — it's finding the right level of resolution for the right room.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- ── SELECTED WORK ── -->
  <section id="work">
    <div class="section-header">
      <span class="section-num">02</span>
      <h2 class="section-title">Selected Work</h2>
    </div>
    <div class="work-list">

      <!-- NYU Blockchain Lab -->
      <div class="work-item">
        <div class="work-meta">
          <div class="work-tag">Community · BD</div>
          <div class="work-org">NYU Blockchain Lab</div>
          <div class="work-period">Nov 2025 — Present</div>
        </div>
        <div class="work-body">
          <p class="work-context">A student org that needed to become a real player in NYC's digital assets scene.</p>
          <p class="work-what">Built the operating system from scratch — speaker sourcing, event execution, multichannel promotion. Secured partnerships with BNB Chain, OKX, and Solana. Moderated panels with founders, VCs, and protocol leads. Grew and managed a 250+ member Telegram community. Led 20+ events across panels, workshops, office visits, and hackathons.</p>
          <div class="work-impact">
            <span class="impact-chip">20+ events executed</span>
            <span class="impact-chip">250+ community members</span>
            <span class="impact-chip">BNB Chain · OKX · Solana</span>
          </div>
          <a href="https://www.nyublockchainlab.xyz/" target="_blank" class="work-link">nyublockchainlab.xyz →</a>
        </div>
      </div>

      <!-- SproutFi -->
      <div class="work-item">
        <div class="work-meta">
          <div class="work-tag">DeFi · GTM</div>
          <div class="work-org">SproutFi</div>
          <div class="work-period">Nov 2025 — Present</div>
        </div>
        <div class="work-body">
          <p class="work-context">A DeFi yield protocol with strong mechanics but a gap between what it does and what users understand.</p>
          <p class="work-what">Designed the go-to-market messaging framework — translating complex yield strategy into user-facing and market-facing narratives. Synthesized market feedback to inform product communication. Supported founder storytelling to build user trust and clarify the product's position in a crowded DeFi landscape.</p>
          <div class="work-impact">
            <span class="impact-chip">GTM framework built 0→1</span>
            <span class="impact-chip">Product messaging · Content</span>
          </div>
          <a href="https://sproutfi.xyz" target="_blank" class="work-link">sproutfi.xyz →</a>
        </div>
      </div>

      <!-- Research -->
      <div class="work-item">
        <div class="work-meta">
          <div class="work-tag">Research</div>
          <div class="work-org">Independent Research</div>
          <div class="work-period">Aug 2025 — Present</div>
        </div>
        <div class="work-body">
          <p class="work-context">An open question: does the Bitcoin halving still matter in a world with ETFs and institutional participation?</p>
          <p class="work-what">Used event-time analysis and Newey-West adjusted regressions on weekly return data to test whether post-halving return patterns persisted in 2024. Finding: they didn't — meaningfully muted compared to prior cycles, suggesting the market had already priced the supply shock earlier. Also authored a broader paper on stablecoins, RWAs, and the institutional adoption of digital assets.</p>
          <div class="work-impact">
            <span class="impact-chip">Econometric analysis</span>
            <span class="impact-chip">BTC · ETF · RWA · Stablecoins</span>
          </div>
        </div>
      </div>

      <!-- China Merchants -->
      <div class="work-item">
        <div class="work-meta">
          <div class="work-tag">TradFi · Automation</div>
          <div class="work-org">China Merchants Securities</div>
          <div class="work-period">Aug–Nov 2025</div>
        </div>
        <div class="work-body">
          <p class="work-context">A Debt Capital Markets team running daily macro and fixed-income analysis manually across China and U.S. markets.</p>
          <p class="work-what">Built an AI-assisted monitoring workflow and automated dashboards for yields, spreads, and market news — cutting data errors by 90% and improving research efficiency by 60%. Supported bond pricing and issuance analysis through comparable screening and market commentary.</p>
          <div class="work-impact">
            <span class="impact-chip">60% efficiency gain</span>
            <span class="impact-chip">90% fewer data errors</span>
          </div>
        </div>
      </div>

      <!-- Guosheng -->
      <div class="work-item">
        <div class="work-meta">
          <div class="work-tag">Equity Research</div>
          <div class="work-org">Guosheng Securities</div>
          <div class="work-period">Jun–Aug 2025</div>
        </div>
        <div class="work-body">
          <p class="work-context">An investment team running quantitative and fundamental equity analysis across Chinese markets.</p>
          <p class="work-what">Authored an investment thesis on Eoptolink — a leading optical module firm in CPO applications — combining top-down industry analysis with bottom-up DCF and peer benchmarking. Recommended a long position. It returned 135%.</p>
          <div class="work-impact">
            <span class="impact-chip">135% validated return</span>
            <span class="impact-chip">DCF · Peer comps · CPO sector</span>
          </div>
        </div>
      </div>

    </div>
  </section>

  <!-- ── EVENTS ── -->
  <section id="events">
    <div class="section-header">
      <span class="section-num">03</span>
      <h2 class="section-title">Events I've Led</h2>
    </div>
    <p class="events-intro">
      Every event below was organized, executed, and often moderated by me — not just attended. This is what ecosystem building looks like in practice: finding the right people, getting them in the same room, and making the conversation worth having.
    </p>
    <div class="events-stat-row">
      <div class="e-stat"><div class="e-stat-num">20+</div><div class="e-stat-label">events organized</div></div>
      <div class="e-stat"><div class="e-stat-num">5+</div><div class="e-stat-label">panels moderated</div></div>
      <div class="e-stat"><div class="e-stat-num">250+</div><div class="e-stat-label">community members</div></div>
      <div class="e-stat"><div class="e-stat-num">3</div><div class="e-stat-label">major chain partnerships</div></div>
    </div>

    <div class="event-categories">

      <!-- Panels & Talks -->
      <div>
        <div class="event-category-title">Panels & Industry Talks</div>
        <div class="event-grid">
          <div class="event-row">
            <span class="event-name">How to Break Into the Industry</span>
            <a href="https://luma.com/63wk6h7m" target="_blank" class="event-luma">Luma →</a>
          </div>
          <div class="event-row">
            <span class="event-name">Paths into Crypto Venture Capital</span>
            <a href="https://luma.com/bptmmbkx" target="_blank" class="event-luma">Luma →</a>
          </div>
          <div class="event-row">
            <span class="event-name">From NYU → Real World Leverage (Alumni Panel)</span>
            <a href="https://luma.com/uz7raevg" target="_blank" class="event-luma">Luma →</a>
          </div>
          <div class="event-row">
            <span class="event-name">Navigating Your Path in Web3</span>
            <a href="https://luma.com/tj57ipmg" target="_blank" class="event-luma">Luma →</a>
          </div>
          <div class="event-row">
            <span class="event-name">Money & Finance (r)Evolution?</span>
            <a href="https://luma.com/aza220rm" target="_blank" class="event-luma">Luma →</a>
          </div>
          <div class="event-row">
            <span class="event-name">Navigating Institutional Crypto</span>
            <a href="https://luma.com/y4i4zq95" target="_blank" class="event-luma">Luma →</a>
          </div>
          <div class="event-row">
            <span class="event-name">The Future Flow of Money</span>
            <a href="https://luma.com/g1524pmo" target="_blank" class="event-luma">Luma →</a>
          </div>
          <div class="event-row">
            <span class="event-name">Digital Gold vs. Payments</span>
            <a href="https://luma.com/maeibgmj" target="_blank" class="event-luma">Luma →</a>
          </div>
          <div class="event-row">
            <span class="event-name">On-Chain Privacy & Stablecoins: Security, Regulation, Institutional Adoption</span>
            <a href="https://luma.com/bghbkdar" target="_blank" class="event-luma">Luma →</a>
          </div>
        </div>
      </div>

      <!-- Partner Events -->
      <div>
        <div class="event-category-title">Partner & Institutional Events</div>
        <div class="event-grid">
          <div class="event-row">
            <span class="event-name">NYU Blockchain Lab × Grayscale Investments</span>
            <a href="https://luma.com/f9937p58" target="_blank" class="event-luma">Luma →</a>
          </div>
          <div class="event-row">
            <span class="event-name">NYU Blockchain Lab × Galaxy</span>
            <a href="https://luma.com/wph8q6oy" target="_blank" class="event-luma">Luma →</a>
          </div>
          <div class="event-row">
            <span class="event-name">DeFi Office Hours: 1inch × Ledger</span>
            <a href="https://luma.com/definyu" target="_blank" class="event-luma">Luma →</a>
          </div>
          <div class="event-row">
            <span class="event-name">BNB Chain & YZi Labs @ NYU</span>
            <span class="event-partner">BNB Chain</span>
          </div>
        </div>
      </div>

      <!-- Office Visits -->
      <div>
        <div class="event-category-title">Office Visits</div>
        <div class="event-grid">
          <div class="event-row">
            <span class="event-name">Solana Office Visit — NYC</span>
            <a href="https://x.com/BlockchainNYU/status/2024224504927408216?s=20" target="_blank" class="event-luma">Post →</a>
          </div>
          <div class="event-row">
            <span class="event-name">OKX Web3 Academy × NYU</span>
            <a href="https://luma.com/okxnyu26" target="_blank" class="event-luma">Luma →</a>
          </div>
        </div>
      </div>

      <!-- Networking -->
      <div>
        <div class="event-category-title">Networking & Happy Hours</div>
        <div class="event-grid">
          <div class="event-row">
            <span class="event-name">Digital Assets Happy Hour: RWA, Tokenization & Institutional Adoption</span>
            <a href="https://luma.com/kdd6z80q" target="_blank" class="event-luma">Luma →</a>
          </div>
          <div class="event-row">
            <span class="event-name">Ivy Students & Builders Rooftop Happy Hour</span>
            <a href="https://luma.com/qxkiuc1u" target="_blank" class="event-luma">Luma →</a>
          </div>
        </div>
      </div>

      <!-- Hackathons -->
      <div>
        <div class="event-category-title">Hackathons</div>
        <div class="event-grid">
          <div class="event-row">
            <span class="event-name">Build on Bitcoin</span>
            <a href="https://luma.com/b7enl348" target="_blank" class="event-luma">Luma →</a>
          </div>
          <div class="event-row">
            <span class="event-name">HashKey Chain — Horizon Hackathon</span>
            <a href="https://x.com/HSKChain/status/2019255934342553848?s=20" target="_blank" class="event-luma">Post →</a>
          </div>
          <div class="event-row">
            <span class="event-name">Build with TRAE.ai & MiniMax @ NYC</span>
            <a href="https://luma.com/my6krrea" target="_blank" class="event-luma">Luma →</a>
          </div>
        </div>
      </div>

    </div>
  </section>

  <!-- ── HOW I THINK ── -->
  <section id="thinking">
    <div class="section-header">
      <span class="section-num">04</span>
      <h2 class="section-title">How I Think</h2>
    </div>
    <div class="thoughts">

      <div class="thought-item">
        <div class="thought-theme">On Uncertainty</div>
        <div class="thought-content">
          <p>Most people wait for clarity before they act. I've learned that <strong>clarity is often the output of action, not its precondition.</strong> In ambiguous systems — early-stage protocols, new markets, undefined roles — the people who move first learn fastest. The goal isn't to eliminate risk. It's to make better bets with incomplete information.</p>
        </div>
      </div>

      <div class="thought-item">
        <div class="thought-theme">On Web3 & AI</div>
        <div class="thought-content">
          <p>These aren't just technologies. They're <strong>new coordination systems.</strong> Web3 is rebuilding how value flows between people. AI is rebuilding how information gets processed. The interesting work isn't in the tech itself — it's in the gap between what these systems can do and what the world is still organized to receive.</p>
        </div>
      </div>

      <div class="thought-item">
        <div class="thought-theme">On Building</div>
        <div class="thought-content">
          <p>The best builders I've met aren't the loudest. They're the ones who <strong>understand the system they're working inside</strong> — its incentives, its friction points, its unspoken rules — and then find the place where effort compounds. My background in economics isn't academic decoration. It's how I read rooms, markets, and organizations.</p>
        </div>
      </div>

      <div class="thought-item">
        <div class="thought-theme">On TradFi & DeFi</div>
        <div class="thought-content">
          <p>I don't see them as opposites. TradFi trained me to think in flows, risk, and structure. DeFi showed me what those same things look like when the middlemen are optional. <strong>The real opportunity is at the seam</strong> — for people who understand both languages and can speak to both rooms.</p>
        </div>
      </div>

    </div>
  </section>

  <!-- ── CONTACT ── -->
  <section id="contact">
    <div class="section-header">
      <span class="section-num">05</span>
      <h2 class="section-title">Get in Touch</h2>
    </div>
    <div class="contact-block">
      <div class="contact-line">
        If you're building something in <em>Web3, AI, or emerging markets</em><br>
        — or need someone who can — let's talk.
      </div>
      <a href="mailto:yz11354@nyu.edu" class="contact-email">
        yz11354@nyu.edu →
      </a>
      <div class="social-row">
        <a href="https://x.com/Ukaverse22" target="_blank" class="social-link">Twitter / X</a>
        <a href="https://www.linkedin.com/in/ukaaa/" target="_blank" class="social-link">LinkedIn</a>
        <a href="https://t.me/Ukaverse22" target="_blank" class="social-link">Telegram</a>
        <a href="https://www.instagram.com/ukaverse22" target="_blank" class="social-link">Instagram</a>
        <a href="https://linktr.ee/Ukaaa22" target="_blank" class="social-link">Linktree</a>
        <a href="https://luma.com/user/usr-TOz7rOGrBrYmQgO" target="_blank" class="social-link">Luma</a>
      </div>
    </div>
  </section>

</main>

<footer class="page">
  <span class="footer-text">Yiheng (Uka) Zhu · ukaverse.club · New York City</span>
  <span class="footer-badge">Open to opportunities</span>
</footer>

</body>
</html>
