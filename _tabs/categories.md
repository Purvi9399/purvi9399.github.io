---
title: About Me
icon: fas fa-user
order: 1
layout: default
---

<!-- ===== About Page Styles (scoped) ===== -->
<style>
  :root {
    --ink: #111;
    --muted: #595959;
    --accent: #8a2be2;           /* matches your site vibe */
    --accent-2: #ff7cc8;         /* playful pop */
    --chip: #f3e6ed;             /* soft pink background for elements */
    --card: #fff;
    --ring: rgba(0,0,0,.08);
  }

  .about-wrap {
    max-width: 980px;
    margin: 0 auto;
    padding: 2.25rem 1.25rem 4rem;
    font-family: "Space Grotesk", system-ui, -apple-system, Segoe UI, Roboto, sans-serif;
    color: var(--ink);
  }

  /* HERO */
  .hero {
    display: grid;
    grid-template-columns: 120px 1fr;
    gap: 1.25rem;
    align-items: center;
    margin-bottom: 1.75rem;
  }
  .hero .pic {
    width: 120px; height: 120px; border-radius: 16px; overflow: hidden;
    box-shadow: 0 8px 20px var(--ring);
  }
  .hero .pic img { width: 100%; height: 100%; object-fit: cover; }
  .hero h1 {
    font-size: clamp(1.6rem, 1.1rem + 2vw, 2.25rem);
    margin: 0;
    line-height: 1.15;
    letter-spacing: .2px;
  }
  .hero h1 .underline {
    background: linear-gradient(120deg, rgba(138,43,226,.25) 0%, rgba(255,124,200,.25) 100%);
    border-radius: 8px; padding: 0 .35rem;
  }
  .hero p {
    margin: .55rem 0 0;
    color: var(--muted);
    font-size: 1.05rem;
  }

  /* SECTION HEADER */
  .section-title {
    display: inline-flex;
    align-items: center;
    gap: .6rem;
    margin: 2.2rem 0 1rem;
    font-weight: 700;
    letter-spacing: .3px;
  }
  .section-title .dot {
    width: 10px; height: 10px; border-radius: 50%;
    background: radial-gradient(circle at 30% 30%, var(--accent), var(--accent-2));
    box-shadow: 0 0 0 6px rgba(138,43,226,.10);
  }

  /* TIMELINE */
  .timeline {
    position: relative;
    margin: .75rem 0 1.25rem 0.3rem;
    padding-left: 1.2rem;
  }
  .timeline::before {
    content: "";
    position: absolute;
    left: .3rem; top: .2rem; bottom: .2rem;
    width: 2px; background: linear-gradient(#ddd, #eee);
  }
  .t-item {
    position: relative;
    margin: 1.15rem 0 1.2rem;
    padding-left: .9rem;
  }
  .t-item::before {
    content: "";
    position: absolute;
    left: -1.1rem; top: .35rem;
    width: 10px; height: 10px; border-radius: 50%;
    background: var(--accent);
    box-shadow: 0 0 0 4px rgba(138,43,226,.12);
  }
  .t-role { font-weight: 700; }
  .t-org { color: var(--muted); font-weight: 600; }
  .t-note { margin: .35rem 0 0; color: var(--ink); }

  /* HIGHLIGHTS / CHIPS */
  .chips {
    display: grid; gap: .6rem;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    margin-top: .6rem;
  }
  .chip {
    background: var(--chip);
    border: 1px solid rgba(0,0,0,.05);
    padding: .9rem 1rem;
    border-radius: 12px;
    box-shadow: 0 4px 14px var(--ring);
  }
  .chip b { display: block; margin-bottom: .25rem; }
  .chip small { color: var(--muted); }

  /* ACCORDION (Publications / Writing) */
  .accordion { border-radius: 14px; overflow: hidden; border: 1px solid rgba(0,0,0,.06); }
  .acc-item + .acc-item { border-top: 1px solid rgba(0,0,0,.06); }
  .acc-btn {
    width: 100%; text-align: left;
    padding: .95rem 1.1rem;
    background: var(--card);
    border: 0; cursor: pointer; font-weight: 700;
    display: flex; align-items: center; justify-content: space-between;
  }
  .acc-btn span { color: var(--muted); font-weight: 600; font-size: .95rem; }
  .acc-btn:hover { background: #fafafa; }
  .acc-panel {
    display: none; padding: .9rem 1.1rem 1.1rem;
    background: #fff;
  }
  .acc-panel p { margin: .45rem 0 .4rem; color: var(--ink); }
  .acc-panel a { color: var(--accent); text-decoration: underline; }

  /* MEDIA STRIP */
  .media-row {
    display: grid; gap: .75rem;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  }
  .media-card {
    background: var(--card);
    border: 1px solid rgba(0,0,0,.06);
    border-radius: 12px; padding: .85rem 1rem;
    box-shadow: 0 4px 12px var(--ring);
  }
  .media-card a { color: var(--accent); text-decoration: none; font-weight: 700; }
  .media-card a:hover { text-decoration: underline; }

  /* CTA */
  .cta {
    margin-top: 2rem;
    background: linear-gradient(120deg, rgba(138,43,226,.08), rgba(255,124,200,.08));
    border: 1px dashed rgba(138,43,226,.35);
    border-radius: 14px;
    padding: 1.1rem 1.2rem;
  }
  .cta p { margin: .4rem 0 .8rem; color: var(--muted); }
  .cta a.btn {
    display: inline-block; padding: .55rem .9rem; border-radius: 10px;
    background: var(--accent); color: #fff; text-decoration: none; font-weight: 700;
    box-shadow: 0 10px 20px rgba(138,43,226,.15);
  }
  .cta a.btn:hover { transform: translateY(-1px); }

  /* LINKS */
  .about-wrap a { color: var(--accent); text-decoration: underline; }
  .about-wrap a:hover { text-decoration: none; }

  @media (max-width: 700px) {
    .hero { grid-template-columns: 72px 1fr; }
    .hero .pic { width: 72px; height: 72px; border-radius: 12px; }
  }
</style>

<div class="about-wrap">

  <!-- HERO -->
  <section class="hero">
    <div class="pic">
      <!-- swap if you want a different photo than the sidebar -->
      <img src="{{ site.avatar }}" alt="Purvi Jain">
    </div>
    <div>
      <h1>Hi, I’m <span class="underline">Purvi Jain</span> 👋</h1>
      <p>Technologist by training, philosopher by calling, and environmental activist at heart. I explore how we design <em>just</em> digital systems.</p>
    </div>
  </section>

  <!-- EDUCATION / TIMELINE -->
  <h2 class="section-title"><span class="dot"></span> Academic Journey</h2>
  <div class="timeline">

  <div class="t-item">
      <div class="t-role">Workshop on LLMs &amp; Philosophy</div>
      <div class="t-org">Berlin — May 2025</div>
      <p class="t-note">Semantic, cognitive, and moral implications of foundation models; how prompting reshapes technical decision-making.</p>
    </div>

  <div class="t-item">
      <div class="t-role">Summer School in Ethics of AI</div>
      <div class="t-org">London School of Economics</div>
      <p class="t-note">Transparency, epistemic authority, and LLMs from ethical &amp; political perspectives.</p>
    </div>

  <div class="t-item">
     <div class="t-role">Master’s in Philosophy</div>
      <div class="t-org">University of Glasgow</div>
      <p class="t-note">Dissertation: <em>Towards an Unbiased AI: Integrating Rawls’ Theory of Justice into Ethical AI Frameworks</em>.</p>
    </div>

   <div class="t-item">
      <div class="t-role">Bachelor’s in Information Technology / Computer Science</div>
      <div class="t-org">India</div>
      <p class="t-note">Began with code &amp; systems; stayed for the hard questions about power, bias, and responsibility.</p>
    </div>

  </div>

  <!-- HIGHLIGHTS -->
  <h2 class="section-title"><span class="dot"></span> Highlights</h2>
  <div class="chips">
    <div class="chip">
      <b>GreenBeans Society · President</b>
      <small>E-waste activism. 100+ colleges reached; helped universities shift to responsible recycling.</small>
    </div>
    <div class="chip">
      <b>Reading Group · LLMs &amp; Philosophy</b>
      <small>Founded an interdisciplinary forum at Glasgow to bridge systems and semantics.</small>
    </div>
    <div class="chip">
      <b>United by Fascination for Learning (UFL)</b>
      <small>Podcast-style YouTube series translating philosophy for broader audiences.</small>
    </div>
    <div class="chip">
      <b>Mentor · IntoUniversity</b>
      <small>Supporting curiosity and academic confidence for younger students.</small>
    </div>
    <div class="chip">
      <b>Communities</b>
      <small>SWIP UK · MAP · The Aristotelian Society.</small>
    </div>
  </div>

  <!-- PUBLICATIONS / WRITING -->
  <h2 class="section-title"><span class="dot"></span> Publications &amp; Writing</h2>
  <div class="accordion" id="pubs">

   <div class="acc-item">
      <button class="acc-btn">
        <span><i class="fas fa-book-open"></i> Noctua — “Technological Change and the Evolution of Perspectives on Artificial Consciousness.”</span>
        <i class="fas fa-chevron-down"></i>
      </button>
      <div class="acc-panel">
        <p>Philosophical reflections on how technological shifts reframe our theories of mind and moral status.</p>
        <!-- add link when you have it -->
        <!-- <p><a href="URL" target="_blank">Read the piece →</a></p> -->
      </div>
    </div>

   <div class="acc-item">
      <button class="acc-btn">
        <span><i class="fab fa-medium"></i> Medium Essays — AI ethics, environmental impacts of computing, techno-social justice</span>
        <i class="fas fa-chevron-down"></i>
      </button>
      <div class="acc-panel">
        <p>Accessible writing on fairness, transparency, and design justice.</p>
        <p><a href="https://medium.com/@passionatepurvi07" target="_blank">Visit my Medium profile →</a></p>
      </div>
    </div>

  </div>

  <!-- MEDIA / LINKS -->
  <h2 class="section-title"><span class="dot"></span> Media &amp; Links</h2>
  <div class="media-row">
    <div class="media-card">
      <div><i class="fab fa-youtube"></i> <a href="https://www.youtube.com/@unitedbyfascinationforlearning" target="_blank">United by Fascination for Learning</a></div>
      <small>Podcast-style series: moral theories, conceptual engineering, AI &amp; society.</small>
    </div>
    <div class="media-card">
      <div><i class="fab fa-github"></i> <a href="https://github.com/purvi9399" target="_blank">GitHub</a></div>
      <small>Mini-projects &amp; audit notebooks (Explainable AI, fairness, tooling).</small>
    </div>
    <div class="media-card">
      <div><i class="fab fa-linkedin"></i> <a href="https://www.linkedin.com/in/purvi-jain7" target="_blank">LinkedIn</a></div>
      <small>Talks, communities, and ongoing work.</small>
    </div>
  </div>

  <!-- CTA -->
  <div class="cta">
    <h3 style="margin:0;">Let’s build thoughtful tech.</h3>
    <p>I’m open to collaborations, guest lectures, research assistance, writing partnerships, or workshops on AI ethics and design justice.</p>
    <a class="btn" href="mailto:ipurvijain@gmail.com">Email me</a>
  </div>
</div>

<!-- ===== tiny accordion JS (scoped) ===== -->
<script>
  document.querySelectorAll('.acc-btn').forEach(btn => {
    btn.addEventListener('click', () => {
      const panel = btn.nextElementSibling;
      const open = panel.style.display === 'block';
      document.querySelectorAll('.acc-panel').forEach(p => p.style.display = 'none');
      document.querySelectorAll('.acc-btn i.fas.fa-chevron-down').forEach(i => i.style.transform = 'rotate(0deg)');
      if (!open) {
        panel.style.display = 'block';
        btn.querySelector('i.fas.fa-chevron-down').style.transform = 'rotate(180deg)';
      }
    });
  });
</script>
