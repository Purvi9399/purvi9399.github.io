---
title: About Me
icon: fas fa-user
order: 1
layout: default
---

<!-- Custom Styles for a Fancy Design -->
<style>
  :root {
    --ink: #111;
    --muted: #595959;
    --accent: #FFB6C1;           /* Light pinkish accent */
    --accent-2: #FFDAB9;         /* Soft peach */
    --chip: #FFF0F5;             /* Very light pink */
    --card: #fff;
    --ring: rgba(0,0,0,.08);
    --background-gradient: linear-gradient(to bottom, #FFE4E1 0%, #FFFFFF 100%);
    --fancy-shadow: 0 10px 30px rgba(255,182,193,.2);
  }

  .about-wrap {
    max-width: 980px;
    margin: 0 auto;
    padding: 2.25rem 1.25rem 4rem;
    font-family: "Space Grotesk", system-ui, -apple-system, Segoe UI, Roboto, sans-serif;
    color: var(--ink);
    background: var(--background-gradient);
    border-radius: 16px;
    box-shadow: var(--fancy-shadow);
    overflow: hidden;
  }

  .hero {
    display: grid;
    grid-template-columns: 160px 1fr;
    gap: 1.5rem;
    align-items: center;
    margin-bottom: 2.5rem;
    padding: 1.5rem;
    border-radius: 16px;
    background: rgba(255,182,193,0.15);
    box-shadow: var(--fancy-shadow);
    transition: transform 0.5s ease, box-shadow 0.5s ease;
  }
  .hero:hover {
    transform: translateY(-5px);
    box-shadow: 0 15px 40px rgba(255,182,193,.3);
  }
  .hero .pic {
    width: 160px; height: 160px; border-radius: 50%; overflow: hidden;
    box-shadow: 0 12px 24px rgba(255,182,193,.3);
    transition: transform 0.4s ease;
  }
  .hero .pic:hover { transform: rotate(5deg) scale(1.05); }
  .hero .pic img { width: 100%; height: 100%; object-fit: cover; }
  .hero h1 {
    font-size: clamp(2rem, 1.5rem + 2vw, 2.75rem);
    margin: 0;
    line-height: 1.1;
    letter-spacing: .3px;
    color: var(--accent);
    text-shadow: 0 2px 4px rgba(255,182,193,.2);
  }
  .hero h1 .underline {
    background: linear-gradient(120deg, rgba(255,182,193,.4) 0%, rgba(255,218,185,.4) 100%);
    border-radius: 8px; padding: 0 .4rem;
    animation: glow 2s infinite alternate;
  }
  @keyframes glow {
    from { text-shadow: 0 0 5px rgba(255,182,193,.3); }
    to { text-shadow: 0 0 10px rgba(255,182,193,.6); }
  }
  .hero p { margin: .75rem 0 0; color: var(--muted); font-size: 1.1rem; line-height: 1.6; }
  .hero .personal-note {
    margin-top: 1.25rem;
    font-style: italic;
    color: var(--accent-2);
    font-size: 1rem;
    border-left: 4px solid var(--accent);
    padding-left: 1rem;
    background: rgba(255,182,193,0.1);
    border-radius: 8px;
  }

  .section-title {
    display: inline-flex;
    align-items: center;
    gap: .8rem;
    margin: 3rem 0 1.5rem;
    font-weight: 700;
    letter-spacing: .4px;
    color: var(--accent);
    font-size: 1.8rem;
    position: relative;
    text-transform: uppercase;
  }
  .section-title::after {
    content: '';
    position: absolute;
    bottom: -0.5rem;
    left: 0;
    width: 100%;
    height: 2px;
    background: linear-gradient(to right, var(--accent), transparent);
    animation: slide 2s infinite alternate;
  }
  @keyframes slide {
    from { width: 0; }
    to { width: 100%; }
  }
  .section-title .dot {
    width: 14px; height: 14px; border-radius: 50%;
    background: radial-gradient(circle at 30% 30%, var(--accent), var(--accent-2));
    box-shadow: 0 0 0 8px rgba(255,182,193,.15);
    animation: pulse 2s infinite;
  }
  @keyframes pulse {
    0% { transform: scale(1); opacity: 1; }
    50% { transform: scale(1.2); opacity: 0.7; }
    100% { transform: scale(1); opacity: 1; }
  }

  .timeline {
    position: relative;
    margin: 1rem 0 2rem 0.5rem;
    padding-left: 1.5rem;
  }
  .timeline::before {
    content: "";
    position: absolute;
    left: .5rem; top: 0; bottom: 0;
    width: 4px; background: linear-gradient(var(--accent), var(--accent-2));
    border-radius: 4px;
    box-shadow: 0 0 10px rgba(255,182,193,.1);
  }
  .t-item {
    position: relative;
    margin: 1.5rem 0 2rem;
    padding: 1.25rem;
    background: rgba(255,255,255,0.9);
    border-radius: 16px;
    box-shadow: var(--fancy-shadow);
    transition: transform 0.4s ease, box-shadow 0.4s ease;
  }
  .t-item:hover {
    transform: translateX(10px) scale(1.02);
    box-shadow: 0 12px 36px rgba(255,182,193,.3);
  }
  .t-item::before {
    content: "";
    position: absolute;
    left: -2rem; top: 1.75rem;
    width: 18px; height: 18px; border-radius: 50%;
    background: var(--accent);
    box-shadow: 0 0 0 6px rgba(255,182,193,.2);
    transition: transform 0.3s ease;
  }
  .t-item:hover::before { transform: scale(1.2); }
  .t-role { font-weight: 700; color: var(--accent); font-size: 1.2rem; }
  .t-org { color: var(--muted); font-weight: 600; font-size: 1rem; }
  .t-note { margin: .5rem 0 0; color: var(--ink); line-height: 1.6; }
  .t-reflection { margin-top: .75rem; font-style: italic; color: var(--muted); font-size: 0.95rem; background: rgba(255,182,193,0.05); padding: 0.5rem; border-radius: 8px; }

  .chips {
    display: grid; gap: 1rem;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    margin-top: 1rem;
  }
  .chip {
    background: var(--chip);
    border: 1px solid rgba(255,182,193,.15);
    padding: 1.25rem;
    border-radius: 16px;
    box-shadow: var(--fancy-shadow);
    transition: transform 0.4s ease, background 0.4s ease;
  }
  .chip:hover {
    background: rgba(255,182,193,.2);
    transform: rotate(2deg) translateY(-5px);
  }
  .chip b { display: block; margin-bottom: .5rem; color: var(--accent); font-size: 1.1rem; }
  .chip small { color: var(--muted); line-height: 1.5; }
  .chip details summary { cursor: pointer; font-weight: 600; color: var(--ink); transition: color 0.3s; }
  .chip details summary:hover { color: var(--accent); }
  .chip details[open] summary { color: var(--accent); }
  .chip .t-reflection { margin-top: 0.75rem; }

  .accordion { border-radius: 16px; overflow: hidden; border: 1px solid rgba(255,182,193,.15); background: rgba(255,255,255,0.95); box-shadow: var(--fancy-shadow); }
  .acc-item + .acc-item { border-top: 1px solid rgba(255,182,193,.15); }
  .acc-btn {
    width: 100%; text-align: left;
    padding: 1.25rem 1.5rem;
    background: var(--card);
    border: 0; cursor: pointer; font-weight: 700;
    display: flex; align-items: center; justify-content: space-between;
    transition: background 0.4s ease, padding-left 0.4s ease;
  }
  .acc-btn:hover { background: rgba(255,182,193,.15); padding-left: 1.75rem; }
  .acc-btn span { color: var(--muted); font-weight: 600; font-size: 1rem; }
  .acc-panel {
    display: none; padding: 1.25rem 1.5rem;
    background: #fff;
  }
  .acc-panel p { margin: .5rem 0 .5rem; color: var(--ink); line-height: 1.6; }
  .acc-panel a { color: var(--accent); text-decoration: underline; transition: color 0.3s; }
  .acc-panel a:hover { color: var(--accent-2); }
  .acc-reflection { font-style: italic; color: var(--muted); margin-top: 0.75rem; padding: 0.5rem; background: rgba(255,182,193,0.05); border-radius: 8px; }

  .video-container {
    position: relative;
    padding-bottom: 56.25%;
    height: 0;
    overflow: hidden;
    border-radius: 16px;
    margin-top: 1.5rem;
    box-shadow: var(--fancy-shadow);
    transition: transform 0.4s ease;
  }
  .video-container:hover { transform: scale(1.02); }
  .video-container iframe {
    position: absolute;
    top: 0; left: 0;
    width: 100%; height: 100%;
  }

  .curiosity-log {
    display: grid; gap: 1rem;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    margin-top: 1rem;
  }
  .log-item {
    background: var(--chip);
    border: 1px solid rgba(255,182,193,.15);
    padding: 1.25rem;
    border-radius: 16px;
    box-shadow: var(--fancy-shadow);
    transition: transform 0.4s ease;
  }
  .log-item:hover { transform: rotate(-2deg) translateY(-5px); }
  .log-item b { display: block; margin-bottom: .5rem; color: var(--accent); font-size: 1.1rem; }
  .log-item small { color: var(--muted); }

  .media-row {
    display: grid; gap: 1rem;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  }
  .media-card {
    background: var(--card);
    border: 1px solid rgba(255,182,193,.15);
    border-radius: 16px; padding: 1.25rem;
    box-shadow: var(--fancy-shadow);
    transition: transform 0.4s ease;
  }
  .media-card:hover { transform: translateY(-5px); }
  .media-card a { color: var(--accent); text-decoration: none; font-weight: 700; }
  .media-card a:hover { text-decoration: underline; }

  .cta {
    margin-top: 3rem;
    background: linear-gradient(120deg, rgba(255,182,193,.2), rgba(255,218,185,.2));
    border: 1px dashed rgba(255,182,193,.5);
    border-radius: 16px;
    padding: 1.5rem;
    text-align: center;
    box-shadow: var(--fancy-shadow);
    transition: transform 0.4s ease;
  }
  .cta:hover { transform: translateY(-5px); }
  .cta p { margin: .5rem 0 1rem; color: var(--muted); font-size: 1.1rem; }
  .cta a.btn {
    display: inline-block; padding: .75rem 1.5rem; border-radius: 12px;
    background: var(--accent); color: #fff; text-decoration: none; font-weight: 700;
    box-shadow: 0 12px 24px rgba(255,182,193,.3);
    transition: transform 0.3s ease;
  }
  .cta a.btn:hover { transform: scale(1.1); }

  .about-wrap a { color: var(--accent); text-decoration: underline; transition: color 0.3s; }
  .about-wrap a:hover { color: var(--accent-2); text-decoration: none; }

  @media (max-width: 700px) {
    .hero { grid-template-columns: 1fr; text-align: center; }
    .hero .pic { margin: 0 auto; }
    .chips, .curiosity-log, .media-row { grid-template-columns: 1fr; }
  }
</style>

<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>

<div class="
