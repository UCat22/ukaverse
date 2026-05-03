[index.html](https://github.com/user-attachments/files/27312604/index.html)
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
  --bg: #f7f6ff;
  --bg-warm: #f0eeff;
  --bg-card: #ffffff;
  --text: #1a1826;
  --text-mid: #4a4760;
  --text-light: #9290a8;
  --text-xlight: #c2c0d4;
  --accent: #7c6fd4;
  --accent-soft: #a89ee8;
  --accent-dim: rgba(124,111,212,0.1);
  --accent-pink: #e87fa8;
  --accent-pink-dim: rgba(232,127,168,0.1);
  --border: rgba(180,170,230,0.2);
  --border-mid: rgba(180,170,230,0.35);

  /* Gradient palette from the reference image */
  --grad-purple: #c5bcf0;
  --grad-blue: #b8c8f5;
  --grad-pink: #f0c8dc;
  --grad-cream: #fdf6f0;
}

* { margin: 0; padding: 0; box-sizing: border-box; }

html { scroll-behavior: smooth; }

body {
  font-family: 'DM Sans', sans-serif;
  background: var(--bg);
  /* Subtle overall gradient wash */
  background-image:
    radial-gradient(ellipse at 0% 0%, rgba(197,188,240,0.25) 0%, transparent 50%),
    radial-gradient(ellipse at 100% 100%, rgba(240,200,220,0.2) 0%, transparent 50%);
  background-attachment: fixed;
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
  background: rgba(247,246,255,0.82);
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  border-bottom: 1px solid var(--border);
}
.nav-left {
  display: flex; align-items: center; gap: 1.25rem;
}
.nav-logo {
  font-family: 'DM Sans', sans-serif;
  font-weight: 500; font-size: 0.95rem;
  color: var(--text); text-decoration: none;
  letter-spacing: -0.01em;
}
.nav-logo span { color: var(--accent); }
.nav-socials {
  display: flex; align-items: center; gap: 0.75rem;
  padding-left: 1.25rem;
  border-left: 1px solid var(--border-mid);
}
.nav-social {
  color: var(--text-xlight);
  text-decoration: none;
  display: flex; align-items: center;
  transition: color 0.2s;
  line-height: 1;
}
.nav-social:hover { color: var(--accent); }
.nav-social svg {
  width: 15px; height: 15px;
  fill: currentColor;
}
.nav-links { display: flex; gap: 2rem; list-style: none; }
.nav-links a {
  color: var(--text-light); text-decoration: none;
  font-size: 0.85rem; font-weight: 400;
  transition: color 0.2s;
}
.nav-links a:hover { color: var(--accent); }

/* ── WRAPPER ── */
.page { max-width: 760px; margin: 0 auto; padding: 0 2.5rem; }

/* ── HERO ── */
.hero {
  padding: 8rem 0 5rem;
  border-bottom: 1px solid var(--border);
  display: grid;
  grid-template-columns: 1fr 260px;
  gap: 3.5rem;
  align-items: center;
}
.hero-text {}
.hero-photo { position: relative; }
.hero-photo img {
  width: 100%;
  aspect-ratio: 3/4;
  object-fit: cover;
  object-position: center top;
  border-radius: 12px;
  display: block;
  box-shadow: 0 16px 48px rgba(120,100,200,0.15);
}
.hero-tag {
  display: inline-flex; align-items: center; gap: 0.5rem;
  font-size: 0.72rem; font-weight: 500; letter-spacing: 0.1em;
  text-transform: uppercase; color: var(--text-light);
  margin-bottom: 1.75rem;
}
.hero-tag::before {
  content: '';
  display: inline-block; width: 20px; height: 1px;
  background: var(--accent);
}
.hero h1 {
  font-family: 'Fraunces', serif;
  font-size: clamp(2.4rem, 5vw, 3.6rem);
  font-weight: 300;
  font-variation-settings: 'opsz' 144, 'SOFT' 0, 'WONK' 0;
  line-height: 1.15;
  letter-spacing: -0.03em;
  color: var(--text);
  margin-bottom: 1.5rem;
}
.hero h1 em {
  font-style: italic;
  color: var(--accent);
}
.hero-sub {
  font-size: 0.95rem; color: var(--text-mid);
  max-width: 420px; line-height: 1.75;
  margin-bottom: 2.25rem;
  font-weight: 300;
}
.hero-sub strong { color: var(--text); font-weight: 500; }
.hero-actions {
  display: flex; gap: 0.75rem;
  align-items: center; flex-wrap: wrap;
}

@media (max-width: 640px) {
  .hero { grid-template-columns: 1fr; gap: 2rem; }
  .hero-photo { max-width: 200px; }
}
.btn-primary {
  display: inline-flex; align-items: center; gap: 0.4rem;
  padding: 0.65rem 1.4rem;
  background: var(--accent); color: #fff;
  font-family: 'DM Sans', sans-serif;
  font-size: 0.85rem; font-weight: 500;
  border-radius: 100px; text-decoration: none;
  transition: background 0.2s, transform 0.15s, box-shadow 0.2s;
  letter-spacing: 0.01em;
  box-shadow: 0 4px 16px rgba(124,111,212,0.25);
}
.btn-primary:hover {
  background: #6a5ec0;
  transform: translateY(-1px);
  box-shadow: 0 6px 20px rgba(124,111,212,0.35);
}
.btn-ghost {
  display: inline-flex; align-items: center; gap: 0.4rem;
  padding: 0.65rem 1.4rem;
  border: 1px solid var(--border-mid); color: var(--text-mid);
  font-family: 'DM Sans', sans-serif;
  font-size: 0.85rem; font-weight: 400;
  border-radius: 100px; text-decoration: none;
  transition: border-color 0.2s, color 0.2s, background 0.2s;
  background: rgba(255,255,255,0.6);
}
.btn-ghost:hover { border-color: var(--accent); color: var(--accent); background: var(--accent-dim); }

/* ── SECTION BASE ── */
section { padding: 4.5rem 0; border-bottom: 1px solid var(--border); }
.section-header {
  display: flex; align-items: baseline; gap: 1rem;
  margin-bottom: 3rem;
}
.section-num {
  font-size: 0.72rem; font-weight: 500; color: var(--accent-soft);
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
  border: 1px solid rgba(124,111,212,0.3);
  background: var(--accent-dim);
  padding: 0.2rem 0.55rem; border-radius: 100px;
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
.work-roles {
  display: flex; flex-direction: column;
  gap: 0.35rem; margin-top: 0.1rem;
}
.work-role-item {
  display: flex; flex-direction: column; gap: 0.1rem;
}
.work-role-title {
  font-size: 0.82rem; font-weight: 500;
  color: var(--text-mid);
}
.work-role-period {
  font-size: 0.72rem; color: var(--text-xlight);
}
.work-role-sub .work-role-title {
  font-size: 0.75rem; font-weight: 400;
  color: var(--text-xlight);
}
.work-role-item + .work-role-item {
  padding-top: 0.35rem;
  border-top: 1px solid var(--border);
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
  background: var(--accent-dim);
  border: 1px solid rgba(124,111,212,0.15);
  border-radius: 100px; color: var(--accent);
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
  background: linear-gradient(135deg, rgba(197,188,240,0.15), rgba(240,200,220,0.12));
  border: 1px solid var(--border);
  border-radius: 12px; margin-bottom: 2.5rem;
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

/* ── EVENT CARDS ── */
.event-section-label {
  font-size: 0.72rem; font-weight: 600;
  letter-spacing: 0.1em; text-transform: uppercase;
  color: var(--text-xlight); margin-bottom: 1rem;
  padding-bottom: 0.5rem;
  border-bottom: 1px solid var(--border);
}
.event-card-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
  margin-bottom: 0.5rem;
}
.event-card {
  text-decoration: none;
  border: 1px solid var(--border);
  border-radius: 8px;
  overflow: hidden;
  background: var(--bg);
  transition: border-color 0.2s, transform 0.2s, box-shadow 0.2s;
  display: flex; flex-direction: column;
}
.event-card:hover {
  border-color: var(--accent-soft);
  transform: translateY(-2px);
  box-shadow: 0 8px 32px rgba(124,111,212,0.12);
}
.event-card-img {
  position: relative;
  aspect-ratio: 16/10;
  overflow: hidden;
  background: var(--bg-warm);
}
.event-card-img img {
  width: 100%; height: 100%;
  object-fit: cover;
  display: block;
  transition: transform 0.4s;
  filter: grayscale(10%);
}
.event-card:hover .event-card-img img {
  transform: scale(1.04);
  filter: grayscale(0%);
}
.event-card-img.no-img {
  display: flex; align-items: center; justify-content: center;
}
.event-card-img.no-img::after {
  content: 'Photo coming soon';
  font-size: 0.72rem; color: var(--text-xlight);
}
.event-card-tag {
  position: absolute; top: 0.6rem; left: 0.6rem;
  font-size: 0.65rem; font-weight: 600;
  letter-spacing: 0.07em; text-transform: uppercase;
  color: white;
  background: rgba(0,0,0,0.5);
  backdrop-filter: blur(4px);
  padding: 0.2rem 0.55rem; border-radius: 3px;
}
.event-card-body {
  padding: 0.85rem 1rem;
  flex: 1;
}
.event-card-title {
  font-size: 0.85rem; font-weight: 500;
  color: var(--text); line-height: 1.4;
  margin-bottom: 0.25rem;
}
.event-card-sub {
  font-size: 0.75rem; color: var(--text-light);
}
@media (max-width: 640px) {
  .event-card-grid { grid-template-columns: repeat(2, 1fr); }
}

/* ── THINK QUOTE ── */
.think-quote {
  margin-bottom: 2.5rem;
  padding: 1.75rem 2rem;
  background: linear-gradient(135deg, rgba(197,188,240,0.15), rgba(240,200,220,0.12));
  border: 1px solid var(--border);
  border-left: 3px solid var(--accent);
  border-radius: 0 12px 12px 0;
  display: flex; align-items: baseline; gap: 1rem;
  flex-wrap: wrap;
}
.think-quote-mark {
  font-family: 'Fraunces', serif;
  font-size: 3rem; line-height: 0.8;
  color: var(--accent-soft); opacity: 0.5;
  flex-shrink: 0;
}
.think-quote-text {
  font-family: 'Fraunces', serif;
  font-size: 1.1rem; font-weight: 300;
  font-style: italic; color: var(--text-mid);
  line-height: 1.5; flex: 1;
  letter-spacing: -0.01em;
}
.think-quote-sig {
  font-size: 0.82rem; color: var(--text-xlight);
  font-weight: 400; white-space: nowrap;
}

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
.social-link:hover { color: var(--accent); }

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
  font-size: 0.72rem; color: var(--accent-soft);
  display: flex; align-items: center; gap: 0.4rem;
}
.footer-badge::before {
  content: '';
  width: 5px; height: 5px; border-radius: 50%;
  background: var(--accent-soft);
  animation: pulse-badge 2s ease-in-out infinite;
}
@keyframes pulse-badge {
  0%, 100% { opacity: 1; transform: scale(1); }
  50% { opacity: 0.5; transform: scale(0.8); }
}

/* ── EDUCATION ── */
.edu-list { display: flex; flex-direction: column; gap: 0; }
.edu-item {
  display: grid; grid-template-columns: 1fr 1fr;
  gap: 2rem; align-items: start;
  padding: 1.75rem 0;
  border-bottom: 1px solid var(--border);
}
.edu-item:last-child { border-bottom: none; }
.edu-school {
  font-family: 'Fraunces', serif;
  font-size: 1.05rem; font-weight: 400;
  letter-spacing: -0.02em; color: var(--text);
  margin-bottom: 0.2rem;
}
.edu-degree {
  font-size: 0.85rem; color: var(--text-light);
  font-weight: 300;
}
.edu-chips {
  display: flex; flex-wrap: wrap; gap: 0.4rem;
  margin-bottom: 0.6rem;
}
.edu-chip {
  font-size: 0.72rem; font-weight: 500;
  padding: 0.22rem 0.65rem;
  border: 1px solid var(--border-mid);
  border-radius: 100px;
  color: var(--text-light);
}
.edu-chip-accent {
  background: var(--accent-dim);
  border-color: rgba(124,111,212,0.2);
  color: var(--accent);
}
.edu-courses {
  font-size: 0.78rem; color: var(--text-xlight);
  line-height: 1.6;
}
@media (max-width: 600px) {
  .edu-item { grid-template-columns: 1fr; gap: 0.75rem; }
}

/* ── GALLERY ── */
.gallery-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: 200px 200px;
  gap: 8px;
}
.gallery-item {
  position: relative;
  overflow: hidden;
  border-radius: 4px;
  background: var(--bg-warm);
}
.gallery-item.tall {
  grid-row: span 2;
}
.gallery-item img {
  width: 100%; height: 100%;
  object-fit: cover;
  display: block;
  transition: transform 0.4s ease;
  filter: grayscale(20%);
}
.gallery-item:hover img {
  transform: scale(1.04);
  filter: grayscale(0%);
}
.gallery-overlay {
  position: absolute; bottom: 0; left: 0; right: 0;
  padding: 1rem 0.85rem 0.75rem;
  background: linear-gradient(transparent, rgba(0,0,0,0.55));
  opacity: 0;
  transition: opacity 0.3s;
}
.gallery-item:hover .gallery-overlay { opacity: 1; }
.gallery-overlay span {
  font-size: 0.75rem; color: #fff;
  font-weight: 400; letter-spacing: 0.02em;
}
.gallery-empty {
  width: 100%; height: 100%;
  display: flex; align-items: center; justify-content: center;
  font-size: 0.75rem; color: var(--text-xlight);
  border: 1px dashed var(--border-mid);
  border-radius: 4px;
}
@media (max-width: 600px) {
  .gallery-grid {
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: auto;
  }
  .gallery-item.tall { grid-row: span 1; }
}

/* ── CONTACT SOCIALS ── */
.contact-socials {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 0.75rem;
  margin-top: 0.5rem;
}
.contact-social-item {
  display: flex; align-items: center; gap: 0.75rem;
  padding: 0.85rem 1rem;
  border: 1px solid var(--border);
  border-radius: 6px;
  text-decoration: none;
  transition: border-color 0.2s, background 0.2s;
  background: var(--bg);
}
.contact-social-item:hover {
  border-color: var(--accent-soft);
  background: var(--accent-dim);
}
.contact-social-icon {
  font-size: 1rem; color: var(--text-mid);
  width: 24px; text-align: center; flex-shrink: 0;
}
.contact-social-name {
  font-size: 0.82rem; font-weight: 500;
  color: var(--text);
}
.contact-social-handle {
  font-size: 0.72rem; color: var(--text-light);
  margin-top: 0.1rem;
}
.contact-cv {
  display: flex; align-items: center; gap: 1.25rem;
  margin-top: 0.5rem;
  padding-top: 1.5rem;
  border-top: 1px solid var(--border);
}
.contact-cv-note {
  font-size: 0.8rem; color: var(--text-light);
}
@media (max-width: 600px) {
  .contact-socials { grid-template-columns: repeat(2, 1fr); }
  .contact-cv { flex-direction: column; align-items: flex-start; gap: 0.75rem; }
}
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
  <div class="nav-left">
    <a class="nav-logo" href="#">Uka<span>verse</span></a>
    <div class="nav-socials">
      <!-- LinkedIn -->
      <a href="https://www.linkedin.com/in/ukaaa/" target="_blank" class="nav-social" aria-label="LinkedIn">
        <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
        </svg>
      </a>
      <!-- X / Twitter -->
      <a href="https://x.com/Ukaverse22" target="_blank" class="nav-social" aria-label="Twitter / X">
        <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-4.714-6.231-5.401 6.231H2.744l7.737-8.835L1.254 2.25H8.08l4.253 5.622 5.911-5.622zm-1.161 17.52h1.833L7.084 4.126H5.117z"/>
        </svg>
      </a>
      <!-- Email -->
      <a href="mailto:yz11354@nyu.edu" class="nav-social" aria-label="Email">
        <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path d="M20 4H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4-8 5-8-5V6l8 5 8-5v2z"/>
        </svg>
      </a>
    </div>
  </div>
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
    <div class="hero-text">
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
        <a href="cv.pdf" target="_blank" class="btn-primary">Download CV ↓</a>
        <a href="#work" class="btn-ghost">View Work →</a>
      </div>
    </div>
    <div class="hero-photo">
      <img src="images/hero.jpg" alt="Uka moderating a Web3 panel at NYU">
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
          <div class="work-roles">
            <div class="work-role-item">
              <span class="work-role-title">Co-President</span>
              <span class="work-role-period">Apr 2025 – Present</span>
            </div>
            <div class="work-role-item">
              <span class="work-role-title">Vice President</span>
              <span class="work-role-period">Nov 2024 – Apr 2025</span>
            </div>
          </div>
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
          <div class="work-roles">
            <div class="work-role-item">
              <span class="work-role-title">Chief of Staff</span>
              <span class="work-role-period">Nov 2025 – Present</span>
            </div>
            <div class="work-role-item work-role-sub">
              <span class="work-role-title">Product Marketing & Ops</span>
            </div>
          </div>
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

  <!-- ── EDUCATION ── -->
  <section id="education">
    <div class="section-header">
      <span class="section-num">03</span>
      <h2 class="section-title">Education</h2>
    </div>
    <div class="edu-list">
      <div class="edu-item">
        <div class="edu-left">
          <div class="edu-school">New York University</div>
          <div class="edu-degree">MA, Economics</div>
        </div>
        <div class="edu-right">
          <div class="edu-chips">
            <span class="edu-chip edu-chip-accent">GPA 3.8</span>
            <span class="edu-chip">STEM OPT Eligible</span>
            <span class="edu-chip">2024–2026</span>
          </div>
          <div class="edu-courses">Digital Currency & Blockchain · Decentralized Finance · Financial Econometrics</div>
        </div>
      </div>
      <div class="edu-item">
        <div class="edu-left">
          <div class="edu-school">UCLA</div>
          <div class="edu-degree">BA, Economics · Minor in Mathematics</div>
        </div>
        <div class="edu-right">
          <div class="edu-chips">
            <span class="edu-chip edu-chip-accent">GPA 3.6</span>
            <span class="edu-chip">2020–2023</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ── EVENTS ── -->
  <section id="events">
    <div class="section-header">
      <span class="section-num">04</span>
      <h2 class="section-title">Events I've Led</h2>
    </div>
    <p class="events-intro">
      Every event below was organized, executed, and often moderated by me — not just attended. This is what ecosystem building looks like in practice: finding the right people, getting them in the same room, and making the conversation worth having.
    </p>
    <div class="events-stat-row">
      <div class="e-stat"><div class="e-stat-num">20+</div><div class="e-stat-label">events organized</div></div>
      <div class="e-stat"><div class="e-stat-num">5+</div><div class="e-stat-label">panels moderated</div></div>
      <div class="e-stat"><div class="e-stat-num">250+</div><div class="e-stat-label">community members</div></div>
      <div class="e-stat"><div class="e-stat-num">10+</div><div class="e-stat-label">industry partners</div></div>
    </div>

    <!-- PANELS -->
    <div class="event-section-label">Panels & Industry Talks</div>
    <div class="event-card-grid">

      <a href="https://luma.com/tj57ipmg" target="_blank" class="event-card">
        <div class="event-card-img">
          <img src="images/events/web3-path.jpg" alt="Navigating Your Path in Web3" onerror="this.parentElement.classList.add('no-img')">
          <div class="event-card-tag">Panel</div>
        </div>
        <div class="event-card-body">
          <div class="event-card-title">Navigating Your Path in Web3</div>
          <div class="event-card-sub">From Curiosity to Building</div>
        </div>
      </a>

      <a href="https://luma.com/63wk6h7m" target="_blank" class="event-card">
        <div class="event-card-img">
          <img src="images/events/break-into-industry.jpg" alt="How to Break Into the Industry" onerror="this.parentElement.classList.add('no-img')">
          <div class="event-card-tag">Panel</div>
        </div>
        <div class="event-card-body">
          <div class="event-card-title">How to Break Into the Industry</div>
          <div class="event-card-sub">NYU Blockchain Lab</div>
        </div>
      </a>

      <a href="https://luma.com/bptmmbkx" target="_blank" class="event-card">
        <div class="event-card-img">
          <img src="images/events/crypto-vc.jpg" alt="Paths into Crypto VC" onerror="this.parentElement.classList.add('no-img')">
          <div class="event-card-tag">Panel</div>
        </div>
        <div class="event-card-body">
          <div class="event-card-title">Paths into Crypto Venture Capital</div>
          <div class="event-card-sub">NYU Blockchain Lab</div>
        </div>
      </a>

      <a href="https://luma.com/uz7raevg" target="_blank" class="event-card">
        <div class="event-card-img">
          <img src="images/events/alumni-panel.jpg" alt="Alumni Panel" onerror="this.parentElement.classList.add('no-img')">
          <div class="event-card-tag">Panel</div>
        </div>
        <div class="event-card-body">
          <div class="event-card-title">From NYU → Real World Leverage</div>
          <div class="event-card-sub">Alumni Panel + Networking</div>
        </div>
      </a>

      <a href="https://luma.com/aza220rm" target="_blank" class="event-card">
        <div class="event-card-img">
          <img src="images/events/finance-revolution.jpg" alt="Money & Finance Revolution" onerror="this.parentElement.classList.add('no-img')">
          <div class="event-card-tag">Panel</div>
        </div>
        <div class="event-card-body">
          <div class="event-card-title">Money & Finance (r)Evolution?</div>
          <div class="event-card-sub">NYU Blockchain Lab</div>
        </div>
      </a>

      <a href="https://luma.com/y4i4zq95" target="_blank" class="event-card">
        <div class="event-card-img">
          <img src="images/events/institutional-crypto.jpg" alt="Navigating Institutional Crypto" onerror="this.parentElement.classList.add('no-img')">
          <div class="event-card-tag">Panel</div>
        </div>
        <div class="event-card-body">
          <div class="event-card-title">Navigating Institutional Crypto</div>
          <div class="event-card-sub">NYU Blockchain Lab</div>
        </div>
      </a>

      <a href="https://luma.com/g1524pmo" target="_blank" class="event-card">
        <div class="event-card-img">
          <img src="images/events/future-flow.jpg" alt="The Future Flow of Money" onerror="this.parentElement.classList.add('no-img')">
          <div class="event-card-tag">Panel</div>
        </div>
        <div class="event-card-body">
          <div class="event-card-title">The Future Flow of Money</div>
          <div class="event-card-sub">NYU Blockchain Lab</div>
        </div>
      </a>

      <a href="https://luma.com/maeibgmj" target="_blank" class="event-card">
        <div class="event-card-img">
          <img src="images/events/digital-gold.jpg" alt="Digital Gold vs Payments" onerror="this.parentElement.classList.add('no-img')">
          <div class="event-card-tag">Panel</div>
        </div>
        <div class="event-card-body">
          <div class="event-card-title">Digital Gold vs. Payments</div>
          <div class="event-card-sub">NYU Blockchain Lab</div>
        </div>
      </a>

      <a href="https://luma.com/bghbkdar" target="_blank" class="event-card">
        <div class="event-card-img">
          <img src="images/events/privacy-stablecoins.jpg" alt="On-Chain Privacy & Stablecoins" onerror="this.parentElement.classList.add('no-img')">
          <div class="event-card-tag">Panel</div>
        </div>
        <div class="event-card-body">
          <div class="event-card-title">On-Chain Privacy & Stablecoins</div>
          <div class="event-card-sub">Security · Regulation · Adoption</div>
        </div>
      </a>

    </div>

    <!-- PARTNER EVENTS -->
    <div class="event-section-label" style="margin-top:2.5rem;">Partner & Institutional</div>
    <div class="event-card-grid">

      <a href="https://luma.com/f9937p58" target="_blank" class="event-card">
        <div class="event-card-img">
          <img src="images/events/grayscale.jpg" alt="Grayscale" onerror="this.parentElement.classList.add('no-img')">
          <div class="event-card-tag">Partner</div>
        </div>
        <div class="event-card-body">
          <div class="event-card-title">NYU Blockchain Lab × Grayscale</div>
          <div class="event-card-sub">Grayscale Investments</div>
        </div>
      </a>

      <a href="https://luma.com/wph8q6oy" target="_blank" class="event-card">
        <div class="event-card-img">
          <img src="images/events/galaxy.jpg" alt="Galaxy" onerror="this.parentElement.classList.add('no-img')">
          <div class="event-card-tag">Partner</div>
        </div>
        <div class="event-card-body">
          <div class="event-card-title">NYU Blockchain Lab × Galaxy</div>
          <div class="event-card-sub">Galaxy Digital</div>
        </div>
      </a>

      <a href="https://luma.com/definyu" target="_blank" class="event-card">
        <div class="event-card-img">
          <img src="images/events/defi-office-hours.jpg" alt="DeFi Office Hours" onerror="this.parentElement.classList.add('no-img')">
          <div class="event-card-tag">Workshop</div>
        </div>
        <div class="event-card-body">
          <div class="event-card-title">DeFi Office Hours at NYU</div>
          <div class="event-card-sub">1inch × Ledger</div>
        </div>
      </a>

      <a href="#" class="event-card">
        <div class="event-card-img">
          <img src="images/events/bnb-chain.jpg" alt="BNB Chain" onerror="this.parentElement.classList.add('no-img')">
          <div class="event-card-tag">Partner</div>
        </div>
        <div class="event-card-body">
          <div class="event-card-title">BNB Chain & YZi Labs @ NYU</div>
          <div class="event-card-sub">BNB Chain</div>
        </div>
      </a>

    </div>

    <!-- OFFICE VISITS -->
    <div class="event-section-label" style="margin-top:2.5rem;">Office Visits</div>
    <div class="event-card-grid">

      <a href="https://x.com/BlockchainNYU/status/2024224504927408216?s=20" target="_blank" class="event-card">
        <div class="event-card-img">
          <img src="images/events/solana-visit.jpg" alt="Solana Office Visit" onerror="this.parentElement.classList.add('no-img')">
          <div class="event-card-tag">Office Visit</div>
        </div>
        <div class="event-card-body">
          <div class="event-card-title">Solana Office Visit — NYC</div>
          <div class="event-card-sub">Solana Foundation</div>
        </div>
      </a>

      <a href="https://luma.com/okxnyu26" target="_blank" class="event-card">
        <div class="event-card-img">
          <img src="images/events/okx.jpg" alt="OKX" onerror="this.parentElement.classList.add('no-img')">
          <div class="event-card-tag">Office Visit</div>
        </div>
        <div class="event-card-body">
          <div class="event-card-title">OKX Web3 Academy × NYU</div>
          <div class="event-card-sub">OKX</div>
        </div>
      </a>

    </div>

    <!-- NETWORKING -->
    <div class="event-section-label" style="margin-top:2.5rem;">Networking & Happy Hours</div>
    <div class="event-card-grid">

      <a href="https://luma.com/kdd6z80q" target="_blank" class="event-card">
        <div class="event-card-img">
          <img src="images/events/happy-hour-rwa.jpg" alt="Digital Assets Happy Hour" onerror="this.parentElement.classList.add('no-img')">
          <div class="event-card-tag">Networking</div>
        </div>
        <div class="event-card-body">
          <div class="event-card-title">Digital Assets Happy Hour</div>
          <div class="event-card-sub">RWA · Tokenization · Institutional</div>
        </div>
      </a>

      <a href="https://luma.com/qxkiuc1u" target="_blank" class="event-card">
        <div class="event-card-img">
          <img src="images/events/rooftop.jpg" alt="Rooftop Happy Hour" onerror="this.parentElement.classList.add('no-img')">
          <div class="event-card-tag">Networking</div>
        </div>
        <div class="event-card-body">
          <div class="event-card-title">Ivy Students & Builders Rooftop</div>
          <div class="event-card-sub">Happy Hour</div>
        </div>
      </a>

    </div>

    <!-- HACKATHONS -->
    <div class="event-section-label" style="margin-top:2.5rem;">Hackathons</div>
    <div class="event-card-grid">

      <a href="https://luma.com/b7enl348" target="_blank" class="event-card">
        <div class="event-card-img">
          <img src="images/events/build-bitcoin.jpg" alt="Build on Bitcoin" onerror="this.parentElement.classList.add('no-img')">
          <div class="event-card-tag">Hackathon</div>
        </div>
        <div class="event-card-body">
          <div class="event-card-title">Build on Bitcoin</div>
          <div class="event-card-sub">NYU Blockchain Lab</div>
        </div>
      </a>

      <a href="https://x.com/HSKChain/status/2019255934342553848?s=20" target="_blank" class="event-card">
        <div class="event-card-img">
          <img src="images/events/hashkey.jpg" alt="HashKey Hackathon" onerror="this.parentElement.classList.add('no-img')">
          <div class="event-card-tag">Hackathon</div>
        </div>
        <div class="event-card-body">
          <div class="event-card-title">HashKey Chain — Horizon Hackathon</div>
          <div class="event-card-sub">HashKey Chain</div>
        </div>
      </a>

      <a href="https://luma.com/my6krrea" target="_blank" class="event-card">
        <div class="event-card-img">
          <img src="images/events/trae-hackathon.jpg" alt="TRAE Hackathon" onerror="this.parentElement.classList.add('no-img')">
          <div class="event-card-tag">Hackathon</div>
        </div>
        <div class="event-card-body">
          <div class="event-card-title">Build with TRAE.ai & MiniMax @ NYC</div>
          <div class="event-card-sub">TRAE.ai · MiniMax</div>
        </div>
      </a>

    </div>

  </section>

  <!-- ── HOW I THINK ── -->
  <section id="thinking">
    <div class="section-header">
      <span class="section-num">05</span>
      <h2 class="section-title">How I Think</h2>
    </div>

    <!-- Quote card -->
    <div class="think-quote">
      <div class="think-quote-mark">"</div>
      <div class="think-quote-text">The future is not predicted. It's designed.</div>
      <div class="think-quote-sig">— Uka</div>
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

  <!-- ── PHOTO GALLERY ── -->
  <section id="gallery">
    <div class="section-header">
      <span class="section-num">06</span>
      <h2 class="section-title">In the Room</h2>
    </div>
    <p class="events-intro">Real moments from building, moderating, and showing up.</p>
    <div class="gallery-grid">
      <div class="gallery-item tall">
        <img src="images/hero.jpg" alt="Moderating Web3 panel at NYU">
        <div class="gallery-overlay">
          <span>Navigating Your Path in Web3</span>
        </div>
      </div>
      <div class="gallery-item">
        <img src="images/gallery-1.jpg" alt="NYU Blockchain Lab event">
        <div class="gallery-overlay">
          <span>NYU Blockchain Lab</span>
        </div>
      </div>
      <div class="gallery-item">
        <img src="images/gallery-2.jpg" alt="Industry panel">
        <div class="gallery-overlay">
          <span>Industry Panel</span>
        </div>
      </div>
      <div class="gallery-item">
        <img src="images/gallery-3.jpg" alt="Conference">
        <div class="gallery-overlay">
          <span>Digital Asset Summit</span>
        </div>
      </div>
      <div class="gallery-item">
        <img src="images/gallery-4.jpg" alt="Happy Hour">
        <div class="gallery-overlay">
          <span>Community Building</span>
        </div>
      </div>
      <div class="gallery-item">
        <img src="images/gallery-5.jpg" alt="Hackathon">
        <div class="gallery-overlay">
          <span>Hackathon</span>
        </div>
      </div>
    </div>
  </section>

  <!-- ── CONTACT ── -->
  <section id="contact">
    <div class="section-header">
      <span class="section-num">07</span>
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
      <div class="contact-socials">
        <a href="https://x.com/Ukaverse22" target="_blank" class="contact-social-item">
          <span class="contact-social-icon">𝕏</span>
          <div>
            <div class="contact-social-name">Twitter / X</div>
            <div class="contact-social-handle">@Ukaverse22</div>
          </div>
        </a>
        <a href="https://www.linkedin.com/in/ukaaa/" target="_blank" class="contact-social-item">
          <span class="contact-social-icon">in</span>
          <div>
            <div class="contact-social-name">LinkedIn</div>
            <div class="contact-social-handle">Yiheng (Uka) Zhu</div>
          </div>
        </a>
        <a href="https://t.me/Ukaverse22" target="_blank" class="contact-social-item">
          <span class="contact-social-icon">✈</span>
          <div>
            <div class="contact-social-name">Telegram</div>
            <div class="contact-social-handle">@Ukaverse22</div>
          </div>
        </a>
        <a href="https://www.instagram.com/ukaverse22" target="_blank" class="contact-social-item">
          <span class="contact-social-icon">◎</span>
          <div>
            <div class="contact-social-name">Instagram</div>
            <div class="contact-social-handle">@ukaverse22</div>
          </div>
        </a>
        <a href="https://luma.com/user/usr-TOz7rOGrBrYmQgO" target="_blank" class="contact-social-item">
          <span class="contact-social-icon">◈</span>
          <div>
            <div class="contact-social-name">Luma</div>
            <div class="contact-social-handle">Events I organize</div>
          </div>
        </a>
        <a href="https://linktr.ee/Ukaaa22" target="_blank" class="contact-social-item">
          <span class="contact-social-icon">⌘</span>
          <div>
            <div class="contact-social-name">Linktree</div>
            <div class="contact-social-handle">All links</div>
          </div>
        </a>
      </div>
      <div class="contact-cv">
        <a href="cv.pdf" target="_blank" class="btn-primary">Download CV ↓</a>
        <span class="contact-cv-note">MA Economics · NYU · GPA 3.8 · STEM OPT Eligible</span>
      </div>
    </div>
  </section>

</main>

<footer class="page">
  <span class="footer-text">Yiheng (Uka) Zhu · ukaverse.club · New York City</span>
  <span class="footer-badge">Open to opportunities</span>
</footer>

<!-- ── UKA CHATBOT ── -->
<style>
.chat-bubble-btn {
  position: fixed; bottom: 1.75rem; right: 1.75rem;
  width: 54px; height: 54px;
  background: linear-gradient(135deg, #7c6fd4, #a89ee8);
  border-radius: 50%; border: none; cursor: pointer;
  display: flex; align-items: center; justify-content: center;
  box-shadow: 0 8px 24px rgba(124,111,212,0.4);
  transition: transform 0.2s, box-shadow 0.2s;
  z-index: 1000;
}
.chat-bubble-btn:hover { transform: scale(1.08); box-shadow: 0 12px 32px rgba(124,111,212,0.5); }
.chat-bubble-btn svg { width: 22px; height: 22px; fill: white; }
.chat-unread {
  position: absolute; top: -2px; right: -2px;
  width: 13px; height: 13px; background: #e87fa8;
  border-radius: 50%; border: 2px solid white;
  animation: chatpulse 2s infinite;
}
@keyframes chatpulse { 0%,100%{transform:scale(1);opacity:1} 50%{transform:scale(1.2);opacity:0.7} }

.chat-win {
  position: fixed; bottom: 5.25rem; right: 1.75rem;
  width: 360px; max-height: 560px;
  background: rgba(255,255,255,0.96);
  backdrop-filter: blur(20px); -webkit-backdrop-filter: blur(20px);
  border: 1px solid rgba(180,170,230,0.25);
  border-radius: 20px;
  box-shadow: 0 24px 64px rgba(100,80,180,0.18);
  display: flex; flex-direction: column; overflow: hidden;
  z-index: 999;
  transition: opacity 0.25s, transform 0.25s;
}
.chat-win.hide { opacity:0; pointer-events:none; transform:translateY(14px) scale(0.97); }

.chat-hdr {
  padding: 0.9rem 1.1rem;
  background: linear-gradient(135deg, rgba(197,188,240,0.18), rgba(240,200,220,0.12));
  border-bottom: 1px solid rgba(180,170,230,0.18);
  display: flex; align-items: center; gap: 0.65rem;
}
.chat-av {
  width: 38px; height: 38px; border-radius: 50%;
  background: linear-gradient(135deg, #7c6fd4, #e87fa8);
  display: flex; align-items: center; justify-content: center;
  font-family: 'Fraunces', serif; font-size: 0.95rem; font-style: italic;
  color: white; flex-shrink: 0;
}
.chat-hdr-name { font-weight: 500; font-size: 0.88rem; color: #1a1826; }
.chat-hdr-status { font-size: 0.7rem; color: #9290a8; display:flex; align-items:center; gap:0.3rem; }
.status-green { width:6px; height:6px; border-radius:50%; background:#4ade80; animation:chatpulse 2s infinite; }
.chat-x { margin-left:auto; background:none; border:none; cursor:pointer; color:#c2c0d4; display:flex; transition:color 0.2s; padding:2px; }
.chat-x:hover { color:#7c6fd4; }

.chat-msgs {
  flex:1; overflow-y:auto; padding:0.85rem;
  display:flex; flex-direction:column; gap:0.65rem;
  scroll-behavior:smooth;
}
.chat-msgs::-webkit-scrollbar { width:3px; }
.chat-msgs::-webkit-scrollbar-thumb { background:rgba(180,170,230,0.3); border-radius:2px; }

.cmsg { display:flex; gap:0.45rem; align-items:flex-end; }
.cmsg.u { flex-direction:row-reverse; }
.cmsg-av {
  width:26px; height:26px; border-radius:50%;
  background:linear-gradient(135deg,#7c6fd4,#e87fa8);
  flex-shrink:0; display:flex; align-items:center; justify-content:center;
  font-family:'Fraunces',serif; font-size:0.65rem; font-style:italic; color:white;
}
.cmsg-b {
  max-width:80%; padding:0.6rem 0.85rem; border-radius:14px;
  font-size:0.85rem; line-height:1.5;
}
.cmsg.a .cmsg-b {
  background:rgba(247,246,255,0.9); border:1px solid rgba(180,170,230,0.2);
  border-bottom-left-radius:3px; color:#1a1826;
}
.cmsg.u .cmsg-b {
  background:linear-gradient(135deg,#7c6fd4,#9088d8);
  color:white; border-bottom-right-radius:3px;
}
.typing-b { display:flex; gap:3px; align-items:center; padding:0.6rem 0.85rem; }
.td { width:5px; height:5px; border-radius:50%; background:#c2c0d4; animation:tdot 1.2s infinite; }
.td:nth-child(2){animation-delay:0.2s} .td:nth-child(3){animation-delay:0.4s}
@keyframes tdot{0%,80%,100%{transform:translateY(0);opacity:0.5}40%{transform:translateY(-5px);opacity:1}}

.chat-qr { display:flex; flex-wrap:wrap; gap:0.35rem; padding:0 0.85rem 0.65rem; }
.chat-qr button {
  font-size:0.72rem; padding:0.3rem 0.7rem;
  border:1px solid rgba(124,111,212,0.3); border-radius:100px;
  cursor:pointer; color:#7c6fd4; background:rgba(124,111,212,0.06);
  transition:all 0.2s; font-family:'DM Sans',sans-serif;
}
.chat-qr button:hover { background:rgba(124,111,212,0.14); border-color:#7c6fd4; }

.chat-inp-wrap {
  padding:0.65rem 0.85rem; border-top:1px solid rgba(180,170,230,0.18);
  display:flex; gap:0.45rem; align-items:flex-end;
  background:rgba(255,255,255,0.8);
}
.chat-inp {
  flex:1; font-family:'DM Sans',sans-serif; font-size:0.85rem; font-weight:300;
  border:1px solid rgba(180,170,230,0.25); border-radius:10px;
  padding:0.55rem 0.8rem; background:rgba(247,246,255,0.8);
  color:#1a1826; resize:none; outline:none; line-height:1.4;
  max-height:90px; min-height:36px; transition:border-color 0.2s;
}
.chat-inp:focus { border-color:rgba(124,111,212,0.45); }
.chat-inp::placeholder { color:#c2c0d4; }
.chat-send-btn {
  width:34px; height:34px; border-radius:50%;
  background:linear-gradient(135deg,#7c6fd4,#a89ee8);
  border:none; cursor:pointer; display:flex; align-items:center; justify-content:center;
  flex-shrink:0; transition:transform 0.15s; box-shadow:0 4px 12px rgba(124,111,212,0.3);
}
.chat-send-btn:hover { transform:scale(1.08); }
.chat-send-btn:disabled { opacity:0.4; cursor:not-allowed; transform:none; }
.chat-send-btn svg { width:14px; height:14px; fill:white; }
.chat-note { text-align:center; font-size:0.6rem; color:#c2c0d4; padding:0.25rem; letter-spacing:0.04em; }
</style>

<button class="chat-bubble-btn" id="chatBtn" onclick="toggleChat()">
  <div class="chat-unread" id="chatDot"></div>
  <svg viewBox="0 0 24 24"><path d="M20 2H4c-1.1 0-2 .9-2 2v18l4-4h14c1.1 0 2-.9 2-2V4c0-1.1-.9-2-2-2z"/></svg>
</button>

<div class="chat-win hide" id="chatWin">
  <div class="chat-hdr">
    <div class="chat-av">U</div>
    <div>
      <div class="chat-hdr-name">Uka Zhu</div>
      <div class="chat-hdr-status"><div class="status-green"></div>Ask me anything</div>
    </div>
    <button class="chat-x" onclick="toggleChat()">
      <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor"><path d="M19 6.41L17.59 5 12 10.59 6.41 5 5 6.41 10.59 12 5 17.59 6.41 19 12 13.41 17.59 19 19 17.59 13.41 12z"/></svg>
    </button>
  </div>
  <div class="chat-msgs" id="chatMsgs"></div>
  <div class="chat-qr" id="chatQR">
    <button onclick="sendQ('What is your background?')">Background</button>
    <button onclick="sendQ('What roles are you open to?')">Open roles</button>
    <button onclick="sendQ('Tell me about NYU Blockchain Lab')">Blockchain Lab</button>
    <button onclick="sendQ('Are you available for full-time?')">Availability</button>
  </div>
  <div class="chat-inp-wrap">
    <textarea class="chat-inp" id="chatInp" placeholder="Ask Uka anything…" rows="1"
      onkeydown="if(event.key==='Enter'&&!event.shiftKey){event.preventDefault();sendMsg()}"
      oninput="this.style.height='auto';this.style.height=Math.min(this.scrollHeight,90)+'px'"></textarea>
    <button class="chat-send-btn" id="chatSend" onclick="sendMsg()">
      <svg viewBox="0 0 24 24"><path d="M2.01 21L23 12 2.01 3 2 10l15 2-15 2z"/></svg>
    </button>
  </div>
  <div class="chat-note">Powered by Claude · Ukaverse</div>
</div>

<script>
const API_URL = 'https://ukaverse-api.vercel.app/api/chat';
let chatHistory = [], chatBusy = false, chatOpened = false;

function toggleChat() {
  const win = document.getElementById('chatWin');
  const dot = document.getElementById('chatDot');
  win.classList.toggle('hide');
  dot.style.display = 'none';
  if (!chatOpened && !win.classList.contains('hide')) {
    chatOpened = true;
    setTimeout(() => addMsg('a', "Hey! I'm Uka. Feel free to ask me about my background, what I'm building, or what I'm looking for — happy to chat."), 350);
  }
}

function addMsg(role, text) {
  const c = document.getElementById('chatMsgs');
  const d = document.createElement('div');
  d.className = 'cmsg ' + (role === 'a' ? 'a' : 'u');
  d.innerHTML = role === 'a'
    ? `<div class="cmsg-av">U</div><div class="cmsg-b">${text}</div>`
    : `<div class="cmsg-b">${text}</div>`;
  c.appendChild(d); c.scrollTop = c.scrollHeight;
}

function showTyping() {
  const c = document.getElementById('chatMsgs');
  const d = document.createElement('div');
  d.className = 'cmsg a'; d.id = 'typingEl';
  d.innerHTML = '<div class="cmsg-av">U</div><div class="cmsg-b typing-b"><div class="td"></div><div class="td"></div><div class="td"></div></div>';
  c.appendChild(d); c.scrollTop = c.scrollHeight;
}

async function sendMsg() {
  const inp = document.getElementById('chatInp');
  const txt = inp.value.trim();
  if (!txt || chatBusy) return;
  inp.value = ''; inp.style.height = 'auto';
  document.getElementById('chatQR').style.display = 'none';
  addMsg('u', txt);
  chatHistory.push({ role: 'user', content: txt });
  chatBusy = true;
  document.getElementById('chatSend').disabled = true;
  showTyping();
  try {
    const r = await fetch(API_URL, {
      method: 'POST', headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({ messages: chatHistory })
    });
    const data = await r.json();
    const reply = data.reply || "Something went wrong — reach me at yz11354@nyu.edu";
    document.getElementById('typingEl')?.remove();
    addMsg('a', reply);
    chatHistory.push({ role: 'assistant', content: reply });
  } catch {
    document.getElementById('typingEl')?.remove();
    addMsg('a', "Something went wrong — email me at yz11354@nyu.edu");
  }
  chatBusy = false;
  document.getElementById('chatSend').disabled = false;
}

function sendQ(q) { document.getElementById('chatInp').value = q; sendMsg(); }
</script>

</body>
</html>
