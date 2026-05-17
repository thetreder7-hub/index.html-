# index.html-
SBP &amp; Associates - Legal Consultants 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SBP & Associates — Advocate & Legal Consultants</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;0,700;1,300;1,400;1,600&family=Jost:wght@200;300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --gold: #b8972a;
    --gold-light: #d4af37;
    --gold-pale: #f0e6c0;
    --deep: #0d0d0d;
    --charcoal: #1a1a1a;
    --mid: #2d2d2d;
    --warm-white: #faf8f4;
    --text-muted: #888;
    --border: rgba(184,151,42,0.25);
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--deep);
    color: var(--warm-white);
    font-family: 'Jost', sans-serif;
    font-weight: 300;
    overflow-x: hidden;
  }

  /* ─── NOISE TEXTURE OVERLAY ─── */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.04'/%3E%3C/svg%3E");
    pointer-events: none;
    z-index: 999;
    opacity: 0.4;
  }

  /* ─── NAVBAR ─── */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.4rem 4rem;
    background: rgba(13,13,13,0.85);
    backdrop-filter: blur(20px);
    border-bottom: 1px solid var(--border);
    transition: padding 0.3s;
  }

  .nav-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.4rem;
    font-weight: 600;
    color: var(--gold-light);
    letter-spacing: 0.08em;
    text-decoration: none;
  }

  .nav-links {
    display: flex;
    gap: 2.5rem;
    list-style: none;
  }

  .nav-links a {
    font-family: 'Jost', sans-serif;
    font-size: 0.72rem;
    font-weight: 400;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: rgba(250,248,244,0.7);
    text-decoration: none;
    transition: color 0.3s;
  }

  .nav-links a:hover { color: var(--gold-light); }

  .nav-cta {
    font-size: 0.72rem;
    font-weight: 500;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    padding: 0.6rem 1.6rem;
    border: 1px solid var(--gold);
    color: var(--gold-light);
    text-decoration: none;
    transition: all 0.3s;
  }

  .nav-cta:hover {
    background: var(--gold);
    color: var(--deep);
  }

  /* ─── HERO ─── */
  .hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    position: relative;
    overflow: hidden;
    padding: 8rem 4rem 6rem;
  }

  .hero-bg {
    position: absolute;
    inset: 0;
    background:
      radial-gradient(ellipse 70% 60% at 70% 50%, rgba(184,151,42,0.07) 0%, transparent 70%),
      radial-gradient(ellipse 40% 40% at 20% 80%, rgba(184,151,42,0.05) 0%, transparent 60%),
      linear-gradient(180deg, #0d0d0d 0%, #111008 100%);
  }

  .hero-lines {
    position: absolute;
    inset: 0;
    overflow: hidden;
  }

  .hero-lines::before {
    content: '';
    position: absolute;
    top: -10%;
    right: 8%;
    width: 1px;
    height: 120%;
    background: linear-gradient(180deg, transparent, rgba(184,151,42,0.3), transparent);
    animation: lineRise 3s ease-out forwards;
  }

  .hero-lines::after {
    content: '';
    position: absolute;
    top: -10%;
    right: 12%;
    width: 1px;
    height: 120%;
    background: linear-gradient(180deg, transparent, rgba(184,151,42,0.12), transparent);
    animation: lineRise 3s 0.4s ease-out forwards;
  }

  @keyframes lineRise {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .hero-content {
    position: relative;
    max-width: 750px;
    animation: heroIn 1.2s cubic-bezier(0.16,1,0.3,1) forwards;
    opacity: 0;
  }

  @keyframes heroIn {
    from { opacity: 0; transform: translateY(40px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .hero-label {
    font-size: 0.7rem;
    font-weight: 500;
    letter-spacing: 0.3em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 1.8rem;
    display: flex;
    align-items: center;
    gap: 1rem;
  }

  .hero-label::before {
    content: '';
    width: 40px;
    height: 1px;
    background: var(--gold);
  }

  .hero h1 {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(3.5rem, 7vw, 6.5rem);
    font-weight: 300;
    line-height: 1.05;
    letter-spacing: -0.01em;
    margin-bottom: 1rem;
  }

  .hero h1 em {
    font-style: italic;
    color: var(--gold-light);
  }

  .hero-sub {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(1.1rem, 2vw, 1.4rem);
    font-weight: 300;
    font-style: italic;
    color: rgba(250,248,244,0.55);
    margin-bottom: 2.5rem;
    letter-spacing: 0.02em;
  }

  .hero-desc {
    font-size: 0.9rem;
    line-height: 1.8;
    color: rgba(250,248,244,0.6);
    max-width: 500px;
    margin-bottom: 3rem;
  }

  .hero-actions {
    display: flex;
    gap: 1.2rem;
    flex-wrap: wrap;
  }

  .btn-primary {
    padding: 0.9rem 2.4rem;
    background: var(--gold);
    color: var(--deep);
    font-family: 'Jost', sans-serif;
    font-size: 0.75rem;
    font-weight: 500;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    text-decoration: none;
    border: none;
    cursor: pointer;
    transition: all 0.3s;
    display: inline-block;
  }

  .btn-primary:hover {
    background: var(--gold-light);
    transform: translateY(-2px);
    box-shadow: 0 12px 40px rgba(184,151,42,0.3);
  }

  .btn-ghost {
    padding: 0.9rem 2.4rem;
    border: 1px solid rgba(250,248,244,0.25);
    color: var(--warm-white);
    font-family: 'Jost', sans-serif;
    font-size: 0.75rem;
    font-weight: 400;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    text-decoration: none;
    transition: all 0.3s;
    display: inline-block;
  }

  .btn-ghost:hover {
    border-color: var(--gold);
    color: var(--gold-light);
  }

  /* Scales icon */
  .scales-deco {
    position: absolute;
    right: 4rem;
    top: 50%;
    transform: translateY(-50%);
    opacity: 0.06;
    font-size: 22rem;
    pointer-events: none;
    animation: float 6s ease-in-out infinite;
    user-select: none;
  }

  @keyframes float {
    0%, 100% { transform: translateY(-50%) rotate(-2deg); }
    50% { transform: translateY(-54%) rotate(2deg); }
  }

  /* ─── STATS STRIP ─── */
  .stats-strip {
    border-top: 1px solid var(--border);
    border-bottom: 1px solid var(--border);
    background: rgba(255,255,255,0.02);
    padding: 2.5rem 4rem;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 1rem;
  }

  .stat-item {
    text-align: center;
    padding: 1rem;
    border-right: 1px solid var(--border);
    animation: fadeUp 0.8s ease-out forwards;
    opacity: 0;
  }

  .stat-item:last-child { border-right: none; }

  .stat-number {
    font-family: 'Cormorant Garamond', serif;
    font-size: 3rem;
    font-weight: 300;
    color: var(--gold-light);
    line-height: 1;
    margin-bottom: 0.4rem;
  }

  .stat-label {
    font-size: 0.68rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: rgba(250,248,244,0.5);
  }

  /* ─── SECTION SHARED ─── */
  section { padding: 7rem 4rem; }

  .section-tag {
    font-size: 0.65rem;
    letter-spacing: 0.35em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 1rem;
    display: flex;
    align-items: center;
    gap: 0.8rem;
  }

  .section-tag::before {
    content: '';
    width: 30px;
    height: 1px;
    background: var(--gold);
  }

  .section-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(2.2rem, 4vw, 3.8rem);
    font-weight: 300;
    line-height: 1.1;
    margin-bottom: 1.2rem;
  }

  .section-title em {
    font-style: italic;
    color: var(--gold-light);
  }

  /* ─── ABOUT ─── */
  #about {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 5rem;
    align-items: center;
    background: var(--charcoal);
  }

  .about-left p {
    font-size: 0.9rem;
    line-height: 1.9;
    color: rgba(250,248,244,0.65);
    margin-bottom: 1.2rem;
  }

  .about-right {
    position: relative;
  }

  .about-card {
    background: var(--mid);
    border: 1px solid var(--border);
    padding: 2.5rem;
    position: relative;
  }

  .about-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 60px;
    height: 3px;
    background: var(--gold);
  }

  .about-card-quote {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.3rem;
    font-style: italic;
    font-weight: 300;
    color: rgba(250,248,244,0.8);
    line-height: 1.6;
    margin-bottom: 1.5rem;
  }

  .about-courts {
    display: flex;
    flex-wrap: wrap;
    gap: 0.6rem;
  }

  .court-badge {
    font-size: 0.65rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    padding: 0.4rem 0.9rem;
    border: 1px solid var(--border);
    color: var(--gold-pale);
  }

  /* ─── PRACTICE AREAS ─── */
  #practice {
    background: var(--deep);
  }

  .practice-header {
    max-width: 600px;
    margin-bottom: 4rem;
  }

  .practice-header p {
    font-size: 0.9rem;
    line-height: 1.8;
    color: rgba(250,248,244,0.55);
    margin-top: 1rem;
  }

  .practice-grid {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    gap: 1px;
    background: var(--border);
    border: 1px solid var(--border);
  }

  .practice-card {
    background: var(--deep);
    padding: 2.2rem 1.8rem;
    position: relative;
    overflow: hidden;
    cursor: default;
    transition: background 0.4s;
  }

  .practice-card::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0;
    width: 100%;
    height: 2px;
    background: var(--gold);
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.4s cubic-bezier(0.16,1,0.3,1);
  }

  .practice-card:hover { background: rgba(184,151,42,0.04); }
  .practice-card:hover::after { transform: scaleX(1); }

  .practice-icon {
    font-size: 1.6rem;
    margin-bottom: 1rem;
    display: block;
  }

  .practice-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.05rem;
    font-weight: 500;
    color: var(--warm-white);
    line-height: 1.3;
  }

  /* ─── TEAM ─── */
  #team {
    background: var(--charcoal);
  }

  .team-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
    margin-top: 3.5rem;
  }

  .team-card {
    border: 1px solid var(--border);
    padding: 2.8rem 2.2rem;
    position: relative;
    transition: all 0.4s cubic-bezier(0.16,1,0.3,1);
    background: var(--deep);
  }

  .team-card:hover {
    border-color: var(--gold);
    transform: translateY(-6px);
    box-shadow: 0 30px 60px rgba(0,0,0,0.4), 0 0 0 1px rgba(184,151,42,0.1);
  }

  .team-avatar {
    width: 60px;
    height: 60px;
    border: 1px solid var(--gold);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.5rem;
    font-weight: 300;
    color: var(--gold-light);
    margin-bottom: 1.5rem;
  }

  .team-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.5rem;
    font-weight: 500;
    margin-bottom: 0.3rem;
  }

  .team-role {
    font-size: 0.68rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 1.2rem;
  }

  .team-phone {
    font-size: 0.85rem;
    color: rgba(250,248,244,0.55);
    text-decoration: none;
    display: flex;
    align-items: center;
    gap: 0.5rem;
    transition: color 0.2s;
  }

  .team-phone:hover { color: var(--gold-light); }

  .team-phone::before { content: '↗'; font-size: 0.7rem; }

  /* ─── CONTACT ─── */
  #contact {
    background: var(--deep);
    display: grid;
    grid-template-columns: 1fr 1.2fr;
    gap: 5rem;
    align-items: start;
  }

  .contact-left .section-title { margin-bottom: 2rem; }

  .contact-info-item {
    margin-bottom: 2rem;
    padding-bottom: 2rem;
    border-bottom: 1px solid var(--border);
  }

  .contact-info-item:last-child { border-bottom: none; }

  .contact-info-label {
    font-size: 0.62rem;
    letter-spacing: 0.3em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 0.6rem;
  }

  .contact-info-value {
    font-size: 0.9rem;
    color: rgba(250,248,244,0.75);
    line-height: 1.7;
  }

  .contact-info-value a {
    color: rgba(250,248,244,0.75);
    text-decoration: none;
    display: block;
    transition: color 0.2s;
  }

  .contact-info-value a:hover { color: var(--gold-light); }

  /* Contact form */
  .contact-form {
    background: var(--charcoal);
    border: 1px solid var(--border);
    padding: 3rem;
  }

  .contact-form h3 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.6rem;
    font-weight: 400;
    margin-bottom: 0.4rem;
  }

  .contact-form p {
    font-size: 0.8rem;
    color: rgba(250,248,244,0.45);
    margin-bottom: 2rem;
  }

  .form-group {
    margin-bottom: 1.2rem;
  }

  .form-group label {
    display: block;
    font-size: 0.65rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: rgba(250,248,244,0.5);
    margin-bottom: 0.5rem;
  }

  .form-group input,
  .form-group select,
  .form-group textarea {
    width: 100%;
    background: var(--deep);
    border: 1px solid rgba(250,248,244,0.1);
    color: var(--warm-white);
    font-family: 'Jost', sans-serif;
    font-size: 0.88rem;
    padding: 0.85rem 1rem;
    outline: none;
    transition: border-color 0.3s;
    -webkit-appearance: none;
  }

  .form-group input:focus,
  .form-group select:focus,
  .form-group textarea:focus {
    border-color: var(--gold);
  }

  .form-group textarea { min-height: 100px; resize: vertical; }

  .form-group select option { background: var(--mid); }

  .form-submit {
    width: 100%;
    padding: 1rem;
    background: var(--gold);
    color: var(--deep);
    border: none;
    font-family: 'Jost', sans-serif;
    font-size: 0.75rem;
    font-weight: 600;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    cursor: pointer;
    transition: all 0.3s;
    margin-top: 0.5rem;
  }

  .form-submit:hover {
    background: var(--gold-light);
    box-shadow: 0 8px 30px rgba(184,151,42,0.35);
  }

  .form-note {
    font-size: 0.7rem;
    color: rgba(250,248,244,0.3);
    text-align: center;
    margin-top: 1rem;
  }

  /* ─── SUCCESS MESSAGE ─── */
  .form-success {
    display: none;
    text-align: center;
    padding: 2rem;
  }

  .form-success .check { font-size: 2.5rem; margin-bottom: 1rem; }
  .form-success h4 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.4rem;
    color: var(--gold-light);
    margin-bottom: 0.5rem;
  }
  .form-success p { font-size: 0.82rem; color: rgba(250,248,244,0.5); }

  /* ─── FOOTER ─── */
  footer {
    background: #080808;
    border-top: 1px solid var(--border);
    padding: 3rem 4rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 1rem;
  }

  .footer-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.2rem;
    font-weight: 500;
    color: var(--gold-light);
  }

  .footer-copy {
    font-size: 0.72rem;
    color: rgba(250,248,244,0.3);
    letter-spacing: 0.08em;
  }

  .footer-links {
    display: flex;
    gap: 2rem;
    list-style: none;
  }

  .footer-links a {
    font-size: 0.7rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: rgba(250,248,244,0.35);
    text-decoration: none;
    transition: color 0.2s;
  }

  .footer-links a:hover { color: var(--gold); }

  /* ─── DIVIDER ─── */
  .gold-divider {
    width: 80px;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--gold), transparent);
    margin: 0 auto 3rem;
  }

  /* ─── WHATSAPP FLOAT ─── */
  .wa-float {
    position: fixed;
    bottom: 2rem;
    right: 2rem;
    z-index: 200;
    width: 56px;
    height: 56px;
    background: #25D366;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.5rem;
    text-decoration: none;
    box-shadow: 0 4px 20px rgba(37,211,102,0.4);
    transition: all 0.3s;
    animation: waPulse 2s ease-in-out infinite;
  }

  .wa-float:hover {
    transform: scale(1.1);
    box-shadow: 0 8px 30px rgba(37,211,102,0.5);
  }

  @keyframes waPulse {
    0%, 100% { box-shadow: 0 4px 20px rgba(37,211,102,0.4); }
    50% { box-shadow: 0 4px 30px rgba(37,211,102,0.7); }
  }

  /* ─── FADE UP ANIMATION ─── */
  .fade-up {
    opacity: 0;
    transform: translateY(30px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }

  .fade-up.visible {
    opacity: 1;
    transform: translateY(0);
  }

  @keyframes fadeUp {
    to { opacity: 1; transform: none; }
  }

  /* ─── RESPONSIVE ─── */
  @media (max-width: 900px) {
    nav { padding: 1.2rem 1.5rem; }
    .nav-links { display: none; }
    .hero { padding: 7rem 1.5rem 4rem; }
    .scales-deco { display: none; }
    .stats-strip { grid-template-columns: repeat(2, 1fr); padding: 2rem 1.5rem; }
    section { padding: 5rem 1.5rem; }
    #about { grid-template-columns: 1fr; gap: 3rem; }
    .practice-grid { grid-template-columns: repeat(2, 1fr); }
    .team-grid { grid-template-columns: 1fr; }
    #contact { grid-template-columns: 1fr; gap: 3rem; }
    footer { flex-direction: column; text-align: center; padding: 2rem 1.5rem; }
    .footer-links { justify-content: center; }
  }
</style>
</head>
<body>

<!-- NAVBAR -->
<nav>
  <a href="#" class="nav-logo">SBP & Associates</a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#practice">Practice Areas</a></li>
    <li><a href="#team">Our Team</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <a href="tel:+918178838999" class="nav-cta">Consult Now</a>
</nav>

<!-- HERO -->
<section class="hero" id="home">
  <div class="hero-bg"></div>
  <div class="hero-lines"></div>
  <div class="scales-deco">⚖</div>

  <div class="hero-content">
    <div class="hero-label">Est. — Delhi NCR</div>
    <h1>SBP &<br><em>Associates</em></h1>
    <p class="hero-sub">Advocate & Legal Consultants</p>
    <p class="hero-desc">
      Practising before the Delhi High Court, Tis Hazari Courts, and Debts Recovery Tribunal-I,
      we deliver incisive legal counsel with the precision and integrity our clients deserve.
    </p>
    <div class="hero-actions">
      <a href="#contact" class="btn-primary">Book Consultation</a>
      <a href="#practice" class="btn-ghost">Practice Areas</a>
    </div>
  </div>
</section>

<!-- STATS STRIP -->
<div class="stats-strip">
  <div class="stat-item" style="animation-delay:0.1s">
    <div class="stat-number">3</div>
    <div class="stat-label">Senior Advocates</div>
  </div>
  <div class="stat-item" style="animation-delay:0.2s">
    <div class="stat-number">10+</div>
    <div class="stat-label">Practice Areas</div>
  </div>
  <div class="stat-item" style="animation-delay:0.3s">
    <div class="stat-number">2</div>
    <div class="stat-label">Office Locations</div>
  </div>
  <div class="stat-item" style="animation-delay:0.4s">
    <div class="stat-number">HC</div>
    <div class="stat-label">Delhi High Court</div>
  </div>
</div>

<!-- ABOUT -->
<section id="about" class="fade-up">
  <div class="about-left">
    <div class="section-tag">About the Firm</div>
    <h2 class="section-title">Justice is not a<br><em>luxury</em> — it is a right.</h2>
    <p>
      SBP & Associates is a full-service law firm committed to providing strategic, effective, and
      ethical legal representation. Our practice spans civil and criminal litigation, property disputes,
      commercial matters, and specialized tribunal proceedings.
    </p>
    <p>
      With a presence at Tis Hazari Courts, the Delhi High Court, and the Debts Recovery Tribunal,
      our team brings deep procedural knowledge and courtroom experience to every mandate.
    </p>
    <p>
      We approach each case with thoroughness and a client-first philosophy — ensuring that every
      individual we represent receives the full weight of our expertise and attention.
    </p>
  </div>

  <div class="about-right">
    <div class="about-card">
      <div class="about-card-quote">
        "We don't just argue cases — we build arguments that courts cannot ignore."
      </div>
      <div class="about-courts">
        <span class="court-badge">Delhi High Court</span>
        <span class="court-badge">Tis Hazari Courts</span>
        <span class="court-badge">DRT-I Delhi</span>
        <span class="court-badge">District Courts</span>
      </div>
    </div>
  </div>
</section>

<!-- PRACTICE AREAS -->
<section id="practice">
  <div class="practice-header fade-up">
    <div class="section-tag">Expertise</div>
    <h2 class="section-title">Our <em>Practice</em> Areas</h2>
    <p>Comprehensive legal representation across all major domains of civil and criminal law.</p>
  </div>

  <div class="practice-grid fade-up">
    <div class="practice-card">
      <span class="practice-icon">⚖️</span>
      <div class="practice-name">Civil Litigation</div>
    </div>
    <div class="practice-card">
      <span class="practice-icon">🔍</span>
      <div class="practice-name">Criminal Litigation</div>
    </div>
    <div class="practice-card">
      <span class="practice-icon">🏛️</span>
      <div class="practice-name">Property Disputes</div>
    </div>
    <div class="practice-card">
      <span class="practice-icon">🤝</span>
      <div class="practice-name">Arbitration & Mediation</div>
    </div>
    <div class="practice-card">
      <span class="practice-icon">💼</span>
      <div class="practice-name">Commercial Disputes</div>
    </div>
    <div class="practice-card">
      <span class="practice-icon">🔐</span>
      <div class="practice-name">Bail Matters</div>
    </div>
    <div class="practice-card">
      <span class="practice-icon">📋</span>
      <div class="practice-name">FIR Matters</div>
    </div>
    <div class="practice-card">
      <span class="practice-icon">📜</span>
      <div class="practice-name">Civil Appeals</div>
    </div>
    <div class="practice-card">
      <span class="practice-icon">🏦</span>
      <div class="practice-name">Sec. 138 NI Act Matters</div>
    </div>
    <div class="practice-card">
      <span class="practice-icon">™️</span>
      <div class="practice-name">IPR & Trademark</div>
    </div>
  </div>
</section>

<!-- TEAM -->
<section id="team">
  <div class="fade-up">
    <div class="section-tag">Our Team</div>
    <h2 class="section-title">The <em>Advocates</em></h2>
  </div>

  <div class="team-grid fade-up">
    <div class="team-card">
      <div class="team-avatar">SB</div>
      <div class="team-name">Sweta Baisla</div>
      <div class="team-role">Senior Advocate</div>
      <a href="tel:+918178838999" class="team-phone">+91 81788 38999</a>
    </div>

    <div class="team-card">
      <div class="team-avatar">BK</div>
      <div class="team-name">Baburam Kumar</div>
      <div class="team-role">Advocate</div>
      <a href="tel:+917541010256" class="team-phone">+91 75410 10256</a>
    </div>

    <div class="team-card">
      <div class="team-avatar">PK</div>
      <div class="team-name">Pradeep Kumar</div>
      <div class="team-role">Advocate</div>
      <a href="tel:+917055118951" class="team-phone">+91 70551 18951</a>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="contact-left fade-up">
    <div class="section-tag">Get In Touch</div>
    <h2 class="section-title">Let's Discuss<br>Your <em>Case</em></h2>

    <div class="contact-info-item">
      <div class="contact-info-label">Courts</div>
      <div class="contact-info-value">
        Tis Hazari Courts, Delhi<br>
        Delhi High Court
      </div>
    </div>

    <div class="contact-info-item">
      <div class="contact-info-label">Office — New Delhi</div>
      <div class="contact-info-value">
        A-16 Nehru Vihar,<br>New Delhi — 110054
      </div>
    </div>

    <div class="contact-info-item">
      <div class="contact-info-label">Office — Ghaziabad</div>
      <div class="contact-info-value">
        33 Fut Road, Shani Bazar Road,<br>Subhash Park-2, Khoda Colony,<br>Ghaziabad, Uttar Pradesh
      </div>
    </div>

    <div class="contact-info-item">
      <div class="contact-info-label">Phone</div>
      <div class="contact-info-value">
        <a href="tel:+918178838999">+91 81788 38999 (Sweta Baisla)</a>
        <a href="tel:+917541010256">+91 75410 10256 (Baburam Kumar)</a>
        <a href="tel:+917055118951">+91 70551 18951 (Pradeep Kumar)</a>
      </div>
    </div>
  </div>

  <div class="contact-right fade-up">
    <div class="contact-form">
      <h3>Send an Enquiry</h3>
      <p>We respond within 24 hours. All communications are strictly confidential.</p>

      <div id="contactForm">
        <div class="form-group">
          <label>Full Name</label>
          <input type="text" id="clientName" placeholder="Your full name">
        </div>
        <div class="form-group">
          <label>Phone Number</label>
          <input type="tel" id="clientPhone" placeholder="+91 XXXXX XXXXX">
        </div>
        <div class="form-group">
          <label>Nature of Matter</label>
          <select id="clientMatter">
            <option value="">— Select Matter Type —</option>
            <option>Civil Litigation</option>
            <option>Criminal Litigation</option>
            <option>Property Dispute</option>
            <option>Bail Matter</option>
            <option>FIR Matter</option>
            <option>Civil Appeal</option>
            <option>Arbitration / Mediation</option>
            <option>Section 138 NI Act</option>
            <option>Commercial Dispute</option>
            <option>IPR / Trademark</option>
            <option>Other</option>
          </select>
        </div>
        <div class="form-group">
          <label>Brief Description</label>
          <textarea id="clientDesc" placeholder="Briefly describe your legal matter..."></textarea>
        </div>
        <button class="form-submit" onclick="submitForm()">Submit Enquiry</button>
        <p class="form-note">* All information shared is strictly confidential and protected by attorney-client privilege.</p>
      </div>

      <div class="form-success" id="formSuccess">
        <div class="check">✦</div>
        <h4>Enquiry Received</h4>
        <p>Thank you. Our team will contact you within 24 hours to discuss your matter.</p>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">SBP & Associates</div>
  <p class="footer-copy">© 2025 SBP & Associates. Advocate & Legal Consultants, Delhi.</p>
  <ul class="footer-links">
    <li><a href="#about">About</a></li>
    <li><a href="#practice">Practice</a></li>
    <li><a href="#team">Team</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</footer>

<!-- WHATSAPP FLOAT -->
<a href="https://wa.me/918178838999?text=Hello%2C%20I%20need%20legal%20consultation." 
   class="wa-float" target="_blank" title="WhatsApp Us">💬</a>

<script>
  // Fade-up intersection observer
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.classList.add('visible');
      }
    });
  }, { threshold: 0.12 });

  document.querySelectorAll('.fade-up').forEach(el => observer.observe(el));

  // Stats counter animation
  const statNumbers = document.querySelectorAll('.stat-number');
  const statsObserver = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.style.animation = 'fadeUp 0.8s ease-out forwards';
      }
    });
  }, { threshold: 0.5 });

  document.querySelectorAll('.stat-item').forEach(el => statsObserver.observe(el));

  // Smooth scroll
  document.querySelectorAll('a[href^="#"]').forEach(a => {
    a.addEventListener('click', e => {
      e.preventDefault();
      const target = document.querySelector(a.getAttribute('href'));
      if (target) target.scrollIntoView({ behavior: 'smooth' });
    });
  });

  // Form submission
  function submitForm() {
    const name = document.getElementById('clientName').value.trim();
    const phone = document.getElementById('clientPhone').value.trim();
    if (!name || !phone) {
      alert('Please fill in your name and phone number.');
      return;
    }
    document.getElementById('contactForm').style.display = 'none';
    document.getElementById('formSuccess').style.display = 'block';
  }

  // Navbar scroll effect
  window.addEventListener('scroll', () => {
    const nav = document.querySelector('nav');
    if (window.scrollY > 60) {
      nav.style.padding = '1rem 4rem';
    } else {
      nav.style.padding = '1.4rem 4rem';
    }
  });
</script>
</body>
</html>
