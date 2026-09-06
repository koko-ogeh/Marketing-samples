# Marketing-samples<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Fortune Ogeh — Email Systems & Automation</title>
<meta name="description" content="Email marketing, list cleanup, and automation work by Fortune Ogeh.">

<!--
  ============================================================
  HOW TO EDIT THIS PAGE (read this before touching anything)
  ============================================================

  1. SAMPLES (the "View sample" buttons)
     Every sample button looks like this:

       <button class="sample-link" onclick="showSample('assets/newsletter-1.png','Weekly newsletter')">View sample</button>

     Just replace the part in the first set of quotes with either:
       a) a path to an image sitting in your /assets folder, e.g. 'assets/newsletter-1.png'
       b) a full link starting with http, e.g. 'https://drive.google.com/yourfile'

     If it's an image path or an image link, clicking the button pops the
     image up on screen. If it's any other kind of link, clicking it just
     opens that link in a new tab. You don't need to change any code for
     this to work, just swap the link/path.

  2. TEXT
     Change any of the sentences directly. Titles are inside <h3> tags,
     descriptions are inside <p> tags right under them.

  3. PRICE RANGE
     Search for "What this usually costs" further down this file. The
     numbers are plain text, edit them directly.

  4. CONTACT INFO
     Search for "Let's talk it through" near the bottom. Swap the email
     and LinkedIn link for whichever you want to use.

  5. HOSTING ON GITHUB
     Keep index.html and the assets folder in the same repo, same level.
     If you turn on GitHub Pages for the repo, this becomes a live link
     you can drop straight into an email.
  ============================================================
-->

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600&family=Work+Sans:wght@400;500;600&display=swap" rel="stylesheet">

<style>
  :root {
    --ink: #131c19;
    --panel: #1c2622;
    --panel-line: rgba(243,238,227,0.14);
    --paper: #f3eee3;
    --paper-dim: #c9c3b4;
    --muted: #a3ada5;
    --brass: #c79a56;
    --brass-soft: rgba(199,154,86,0.16);
    --teal: #83a493;
    --teal-soft: rgba(131,164,147,0.16);
    --max: 760px;
    --max-wide: 1080px;
  }

  * { box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    margin: 0;
    background: var(--ink);
    color: var(--paper);
    font-family: "Work Sans", -apple-system, sans-serif;
    font-size: 17px;
    line-height: 1.6;
    -webkit-font-smoothing: antialiased;
  }

  h1, h2, h3 {
    font-family: "Fraunces", Georgia, serif;
    font-weight: 500;
    margin: 0;
    color: var(--paper);
  }

  p { margin: 0; }

  a { color: inherit; }

  :focus-visible {
    outline: 2px solid var(--brass);
    outline-offset: 3px;
  }

  .wrap {
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 28px;
  }

  .wrap-wide {
    max-width: var(--max-wide);
    margin: 0 auto;
    padding: 0 28px;
  }

  /* ---------- Top bar ---------- */

  .topbar {
    padding: 28px 0 0;
  }

  .topbar .wrap-wide {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .topbar-name {
    font-family: "Fraunces", serif;
    font-size: 1rem;
    letter-spacing: 0.01em;
  }

  .topbar-contact {
    font-size: 0.9rem;
    color: var(--paper-dim);
    text-decoration: none;
    border-bottom: 1px solid transparent;
    transition: border-color 0.15s ease;
  }

  .topbar-contact:hover { border-color: var(--brass); }

  /* ---------- Hero ---------- */

  .hero {
    padding: 64px 0 88px;
  }

  .hero .wrap-wide {
    display: grid;
    grid-template-columns: 1.15fr 0.85fr;
    gap: 56px;
    align-items: center;
  }

  .byline {
    display: flex;
    flex-direction: column;
    gap: 2px;
    margin-bottom: 22px;
  }

  .byline-name {
    font-size: 0.95rem;
    color: var(--brass);
  }

  .byline-role {
    font-size: 0.95rem;
    color: var(--muted);
  }

  .hero h1 {
    font-size: clamp(2.1rem, 4.4vw, 3.4rem);
    line-height: 1.12;
    max-width: 13ch;
  }

  .hero-sub {
    margin-top: 22px;
    max-width: 46ch;
    color: var(--paper-dim);
    font-size: 1.05rem;
  }

  .hero-graphic {
    width: 100%;
    height: auto;
  }

  .hero-graphic .flow-line {
    fill: none;
    stroke-width: 1.6;
    stroke-linecap: round;
    stroke-dasharray: 260;
    stroke-dashoffset: 260;
    animation: draw 1.6s ease forwards;
  }

  .hero-graphic .flow-line.t2 { animation-delay: 0.15s; }
  .hero-graphic .flow-line.t3 { animation-delay: 0.3s; }

  .hero-graphic circle {
    opacity: 0;
    animation: fadein 0.6s ease forwards;
  }

  .hero-graphic .dot-2 { animation-delay: 0.5s; }
  .hero-graphic .dot-3 { animation-delay: 0.65s; }
  .hero-graphic .dot-4 { animation-delay: 0.8s; }
  .hero-graphic .dot-5 { animation-delay: 0.95s; }
  .hero-graphic .dot-6 { animation-delay: 1.1s; }

  .hero-graphic .seg-label {
    opacity: 0;
    animation: fadein 0.5s ease forwards;
    animation-delay: 1.3s;
  }

  @keyframes draw { to { stroke-dashoffset: 0; } }
  @keyframes fadein { to { opacity: 1; } }

  @media (prefers-reduced-motion: reduce) {
    .hero-graphic .flow-line,
    .hero-graphic circle,
    .hero-graphic .seg-label {
      animation: none;
      opacity: 1;
      stroke-dashoffset: 0;
    }
  }

  /* ---------- Section shell ---------- */

  section {
    padding: 56px 0;
    border-top: 1px solid var(--panel-line);
  }

  .section-head {
    margin-bottom: 30px;
  }

  .section-head h2 {
    font-size: 1.7rem;
  }

  .section-head p {
    margin-top: 10px;
    color: var(--paper-dim);
    max-width: 52ch;
  }

  /* ---------- What I do ---------- */

  .offer-list {
    list-style: none;
    margin: 0;
    padding: 0;
  }

  .offer-list li {
    padding: 20px 0;
    border-top: 1px solid var(--panel-line);
    display: grid;
    grid-template-columns: 180px 1fr;
    gap: 20px;
  }

  .offer-list li:first-child { border-top: none; }

  .offer-list h3 {
    font-size: 1.05rem;
  }

  .offer-list p {
    color: var(--paper-dim);
  }

  /* ---------- Sample rows ---------- */

  .sample-list {
    list-style: none;
    margin: 0;
    padding: 0;
  }

  .sample-row {
    padding: 22px 0;
    border-top: 1px solid var(--panel-line);
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 24px;
  }

  .sample-list .sample-row:first-child { border-top: none; }

  .sample-tag {
    display: inline-block;
    font-size: 0.78rem;
    color: var(--teal);
    background: var(--teal-soft);
    padding: 3px 9px;
    border-radius: 3px;
    margin-bottom: 8px;
  }

  .sample-row h3 {
    font-size: 1.1rem;
    margin-bottom: 6px;
  }

  .sample-row p {
    color: var(--paper-dim);
    font-size: 0.95rem;
    max-width: 46ch;
  }

  .sample-link {
    flex-shrink: 0;
    background: none;
    border: 1px solid var(--brass);
    color: var(--brass);
    font-family: "Work Sans", sans-serif;
    font-size: 0.9rem;
    padding: 9px 16px;
    border-radius: 3px;
    cursor: pointer;
    transition: background 0.15s ease, color 0.15s ease;
  }

  .sample-link:hover {
    background: var(--brass);
    color: var(--ink);
  }

  /* ---------- Case study ---------- */

  .case-study p {
    color: var(--paper-dim);
    max-width: 62ch;
  }

  .case-study p + p { margin-top: 16px; }

  .case-study .sample-row {
    margin-top: 26px;
  }

  /* ---------- Pricing ---------- */

  .price-block {
    background: var(--panel);
    border: 1px solid var(--panel-line);
    border-radius: 4px;
    padding: 32px;
  }

  .price-block p {
    color: var(--paper-dim);
    max-width: 58ch;
  }

  .price-block p + p { margin-top: 14px; }

  .price-block strong {
    color: var(--paper);
    font-weight: 600;
  }

  /* ---------- Closing ---------- */

  .closing h2 {
    font-size: 1.9rem;
    max-width: 16ch;
  }

  .closing p {
    margin-top: 16px;
    color: var(--paper-dim);
    max-width: 50ch;
  }

  .closing-links {
    margin-top: 26px;
    display: flex;
    gap: 24px;
    flex-wrap: wrap;
  }

  .closing-links a {
    text-decoration: none;
    border-bottom: 1px solid var(--brass);
    padding-bottom: 2px;
    font-size: 1rem;
  }

  footer {
    padding: 30px 0 50px;
    color: var(--muted);
    font-size: 0.85rem;
  }

  /* ---------- Lightbox ---------- */

  .lightbox {
    display: none;
    position: fixed;
    inset: 0;
    background: rgba(8,10,9,0.92);
    z-index: 100;
    align-items: center;
    justify-content: center;
    padding: 40px 20px;
  }

  .lightbox.is-open { display: flex; }

  .lightbox figure {
    margin: 0;
    max-width: 90vw;
    text-align: center;
  }

  .lightbox img {
    max-width: 90vw;
    max-height: 78vh;
    border-radius: 4px;
    display: block;
    margin: 0 auto;
  }

  .lightbox figcaption {
    margin-top: 14px;
    color: var(--paper-dim);
    font-size: 0.9rem;
  }

  .lightbox-close {
    position: absolute;
    top: 22px;
    right: 28px;
    background: none;
    border: none;
    color: var(--paper);
    font-size: 2rem;
    line-height: 1;
    cursor: pointer;
    padding: 6px;
  }

  /* ---------- Responsive ---------- */

  @media (max-width: 780px) {
    .hero .wrap-wide { grid-template-columns: 1fr; }
    .hero-graphic { max-width: 320px; margin-top: 10px; }
    .offer-list li { grid-template-columns: 1fr; gap: 6px; }
    .sample-row { flex-direction: column; align-items: flex-start; }
    .sample-link { align-self: flex-start; }
  }
</style>
</head>
<body>

<div class="topbar">
  <div class="wrap-wide">
    <span class="topbar-name">Fortune Ogeh</span>
    <!-- Swap this email for whichever address you want people replying to -->
    <a class="topbar-contact" href="mailto:fortuneogeh8@gmail.com">fortuneogeh8@gmail.com</a>
  </div>
</div>

<header class="hero">
  <div class="wrap-wide">
    <div>
      <div class="byline">
        <span class="byline-name">Fortune Ogeh</span>
        <span class="byline-role">Email systems & automation</span>
      </div>
      <h1>Email systems that keep working after you stop thinking about them.</h1>
      <p class="hero-sub">I clean up messy contact lists, build the segments and signup forms behind them, and set up the automations that send the right email to the right person without anyone opening a laptop. A few samples of that work are below.</p>
    </div>

    <!-- Decorative hero graphic, purely visual, safe to leave as is -->
    <svg class="hero-graphic" viewBox="0 0 400 300" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Diagram showing contacts flowing into three grouped segments">
      <circle class="dot-1" cx="34" cy="60" r="5" fill="#c79a56"/>
      <circle class="dot-2" cx="34" cy="110" r="5" fill="#c79a56"/>
      <circle class="dot-3" cx="34" cy="160" r="5" fill="#c79a56"/>
      <circle class="dot-4" cx="34" cy="210" r="5" fill="#c79a56"/>
      <circle class="dot-5" cx="34" cy="260" r="5" fill="#c79a56"/>
      <circle class="dot-6" cx="34" cy="35" r="5" fill="#c79a56"/>

      <path class="flow-line t1" d="M40 60 C 140 60, 160 90, 260 90" stroke="#83a493"/>
      <path class="flow-line t1" d="M40 35 C 140 35, 160 90, 260 90" stroke="#83a493"/>
      <path class="flow-line t2" d="M40 110 C 140 110, 160 150, 260 150" stroke="#83a493"/>
      <path class="flow-line t2" d="M40 160 C 140 160, 160 150, 260 150" stroke="#83a493"/>
      <path class="flow-line t3" d="M40 210 C 140 210, 160 220, 260 220" stroke="#83a493"/>
      <path class="flow-line t3" d="M40 260 C 140 260, 160 220, 260 220" stroke="#83a493"/>

      <rect x="258" y="76" width="118" height="28" rx="3" fill="none" stroke="#c79a56" stroke-width="1.2"/>
      <text class="seg-label" x="317" y="94" text-anchor="middle" fill="#f3eee3" font-family="Work Sans" font-size="12">Segment A</text>

      <rect x="258" y="136" width="118" height="28" rx="3" fill="none" stroke="#c79a56" stroke-width="1.2"/>
      <text class="seg-label" x="317" y="154" text-anchor="middle" fill="#f3eee3" font-family="Work Sans" font-size="12">Segment B</text>

      <rect x="258" y="206" width="118" height="28" rx="3" fill="none" stroke="#c79a56" stroke-width="1.2"/>
      <text class="seg-label" x="317" y="224" text-anchor="middle" fill="#f3eee3" font-family="Work Sans" font-size="12">Segment C</text>
    </svg>
  </div>
</header>

<section>
  <div class="wrap">
    <div class="section-head">
      <h2>What I actually do</h2>
    </div>
    <ul class="offer-list">
      <li>
        <h3>List cleanup & segmentation</h3>
        <p>Going through a contact list, clearing out anyone who's gone quiet, and grouping the rest by what they actually care about.</p>
      </li>
      <li>
        <h3>Signup forms & welcome flows</h3>
        <p>Building the form someone fills out and the automatic email they get right after, so nobody joins a list and hears nothing.</p>
      </li>
      <li>
        <h3>Automations & drip sequences</h3>
        <p>Setting up the behind-the-scenes logic so emails go out on their own, based on what each segment needs.</p>
      </li>
    </ul>
  </div>
</section>

<section>
  <div class="wrap">
    <div class="section-head">
      <h2>Email & newsletter work</h2>
      <p>A few samples from newsletters and sequences I've written and set up.</p>
    </div>
    <ul class="sample-list">
      <li class="sample-row">
        <div>
          <span class="sample-tag">Newsletter</span>
          <h3>Weekly newsletter</h3>
          <p>A regular send built around one clear idea per issue, not a link dump.</p>
        </div>
        <!-- Replace the path/link in quotes below with your own -->
        <button class="sample-link" onclick="showSample('assets/newsletter-1.png','Weekly newsletter')">View sample</button>
      </li>
      <li class="sample-row">
        <div>
          <span class="sample-tag">Sequence</span>
          <h3>Follow-up sequence</h3>
          <p>A short series that goes out after someone takes an action, written to sound like one person talking to one person.</p>
        </div>
        <button class="sample-link" onclick="showSample('assets/sequence-1.png','Follow-up sequence')">View sample</button>
      </li>
      <li class="sample-row">
        <div>
          <span class="sample-tag">Welcome email</span>
          <h3>Waitlist welcome email</h3>
          <p>The first email someone gets right after they join a list, set up to send itself.</p>
        </div>
        <button class="sample-link" onclick="showSample('assets/welcome-1.png','Waitlist welcome email')">View sample</button>
      </li>
    </ul>
  </div>
</section>

<section>
  <div class="wrap">
    <div class="section-head">
      <h2>Signup forms</h2>
      <p>Forms built to feed straight into a list and its tags, not sit disconnected from everything else.</p>
    </div>
    <ul class="sample-list">
      <li class="sample-row">
        <div>
          <span class="sample-tag">Form</span>
          <h3>Lead magnet signup form</h3>
          <p>Built to collect just enough information, without scaring people off before they've even joined.</p>
        </div>
        <button class="sample-link" onclick="showSample('assets/form-1.png','Lead magnet signup form')">View sample</button>
      </li>
      <li class="sample-row">
        <div>
          <span class="sample-tag">Form</span>
          <h3>Waitlist form</h3>
          <p>Connected directly into the list and tagging behind it, so every signup lands where it should.</p>
        </div>
        <button class="sample-link" onclick="showSample('assets/form-2.png','Waitlist form')">View sample</button>
      </li>
    </ul>
  </div>
</section>

<section class="case-study">
  <div class="wrap">
    <div class="section-head">
      <h2>Building a list from zero</h2>
    </div>
    <p>A while back I built an email list from scratch to sell a guide I'd written. No paid ads, no existing audience to pull from. Just a free resource, a signup form, and a plan to earn people's attention before I asked them for anything.</p>
    <p>The list grew past 90 subscribers in the first stretch, and I wrote a five week sequence to keep people engaged before the offer went out. It's a small list by most standards. But it taught me something that applies at any size: if a list isn't cleaned, grouped, and spoken to on purpose, most of it goes quiet. That's usually the same issue sitting inside a list of a few thousand contacts that's been running for years. More contacts, same problem.</p>
    <div class="sample-row">
      <div>
        <span class="sample-tag">List growth</span>
        <h3>From zero to launch</h3>
        <p>A look at how the list and sequence were structured.</p>
      </div>
      <button class="sample-link" onclick="showSample('assets/list-growth.png','From zero to launch')">View sample</button>
    </div>
  </div>
</section>

<section>
  <div class="wrap">
    <div class="section-head">
      <h2>Automation logic</h2>
      <p>Most of my more complex automation work lives in GoHighLevel: branching sequences where the path changes depending on what someone does. If they click, they go one way. If they don't, they go another. The tool changes from client to client. That logic underneath doesn't.</p>
    </div>
    <ul class="sample-list">
      <li class="sample-row">
        <div>
          <span class="sample-tag">Automation</span>
          <h3>Branching sequence</h3>
          <p>A workflow with conditional steps built in, based on how a contact responds.</p>
        </div>
        <button class="sample-link" onclick="showSample('assets/automation-1.png','Branching sequence')">View sample</button>
      </li>
    </ul>
  </div>
</section>

<section>
  <div class="wrap">
    <div class="section-head">
      <h2>What this usually costs</h2>
    </div>
    <div class="price-block">
      <p>Every project gets scoped around your list size and what actually needs building, so one flat number never tells the full story. As a rough guide, a project covering a full list cleanup, segmentation, signup forms, and a set of automations usually lands between <strong>$2,000 and $2,800</strong>.</p>
      <p>After the build, ongoing monthly support, checking that everything's still running and fixing anything that breaks, usually runs <strong>$100 to $150 a month</strong>, and only if you want it.</p>
    </div>
  </div>
</section>

<section class="closing">
  <div class="wrap">
    <h2>Let's talk it through</h2>
    <p>Send me a note about your list and what's not getting done right now. I'll tell you exactly what I'd build first.</p>
    <div class="closing-links">
      <!-- Swap either of these for whichever contact details you want live -->
      <a href="mailto:fortuneogeh8@gmail.com">fortuneogeh8@gmail.com</a>
      <a href="https://www.linkedin.com/in/ogeh-fortune" target="_blank" rel="noopener">linkedin.com/in/ogeh-fortune</a>
    </div>
  </div>
</section>

<footer>
  <div class="wrap">
    <p>Fortune Ogeh · Backed by Fortune</p>
  </div>
</footer>

<!-- Lightbox for image samples -->
<div class="lightbox" id="lightbox" role="dialog" aria-modal="true" aria-label="Sample preview" onclick="if(event.target===this) closeLightbox()">
  <button class="lightbox-close" onclick="closeLightbox()" aria-label="Close preview">&times;</button>
  <figure>
    <img id="lightbox-img" src="" alt="">
    <figcaption id="lightbox-caption"></figcaption>
  </figure>
</div>

<script>
  function showSample(src, title) {
    if (!src || src === '#') return;
    var isImage = /\.(png|jpe?g|gif|webp|svg)(\?.*)?$/i.test(src);
    if (isImage) {
      document.getElementById('lightbox-img').src = src;
      document.getElementById('lightbox-img').alt = title || '';
      document.getElementById('lightbox-caption').textContent = title || '';
      document.getElementById('lightbox').classList.add('is-open');
    } else {
      window.open(src, '_blank', 'noopener');
    }
  }

  function closeLightbox() {
    document.getElementById('lightbox').classList.remove('is-open');
    document.getElementById('lightbox-img').src = '';
  }

  document.addEventListener('keydown', function (e) {
    if (e.key === 'Escape') closeLightbox();
  });
</script>

</body>
</html>
