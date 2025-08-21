
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
    --accent: #FFB6C1;           /* Light pinkish accent */
    --accent-2: #FFDAB9;         /* Soft peach for secondary accents */
    --chip: #FFF0F5;             /* Very light pink for chips */
    --card: #fff;
    --ring: rgba(0,0,0,.08);
    --background-gradient: linear-gradient(to bottom, #FFE4E1 0%, #FFFFFF 100%); /* Fade from light pink to white */
  }

  .about-wrap {
    max-width: 980px;
    margin: 0 auto;
    padding: 2.25rem 1.25rem 4rem;
    font-family: "Space Grotesk", system-ui, -apple-system, Segoe UI, Roboto, sans-serif;
    color: var(--ink);
    background: var(--background-gradient); /* Apply fade gradient to the whole wrap */
    border-radius: 16px; /* Soft corners for a gentle feel */
  }

  /* HERO */
  .hero {
    display: grid;
    grid-template-columns: 120px 1fr;
    gap: 1.25rem;
    align-items: center;
    margin-bottom: 1.75rem;
    background: rgba(255, 182, 193, 0.1); /* Subtle pink tint */
    padding: 1rem;
    border-radius: 12px;
    transition: background 0.3s ease;
  }
  .hero:hover {
    background: rgba(255, 182, 193, 0.2); /* Fun hover for interactivity */
  }
  .hero .pic {
    width: 120px; height: 120px; border-radius: 16px; overflow: hidden;
    box-shadow: 0 8px 20px var(--ring);
    transition: transform 0.3s ease;
  }
  .hero .pic:hover {
    transform: scale(1.05); /* Playful zoom on hover */
  }
  .hero .pic img { width: 100%; height: 100%; object-fit: cover; }
  .hero h1 {
    font-size: clamp(1.6rem, 1.1rem + 2vw, 2.25rem);
    margin: 0;
    line-height: 1.15;
    letter-spacing: .2px;
  }
  .hero h1 .underline {
    background: linear-gradient(120deg, rgba(255,182,193,.25) 0%, rgba(255,218,185,.25) 100%);
    border-radius: 8px; padding: 0 .35rem;
  }
  .hero p {
    margin: .55rem 0 0;
    color: var(--muted);
    font-size: 1.05rem;
  }
  .hero .personal-note {
    margin-top: 1rem;
    font-style: italic;
    color: var(--accent);
    font-size: 0.95rem;
  }

  /* SECTION HEADER */
  .section-title {
    display: inline-flex;
    align-items: center;
    gap: .6rem;
    margin: 2.2rem 0 1rem;
    font-weight: 700;
    letter-spacing: .3px;
    color: var(--accent);
    transition: color 0.3s ease;
  }
  .section-title:hover {
    color: var(--accent-2); /* Fun color shift on hover */
  }
  .section-title .dot {
    width: 10px; height: 10px; border-radius: 50%;
    background: radial-gradient(circle at 30% 30%, var(--accent), var(--accent-2));
    box-shadow: 0 0 0 6px rgba(255,182,193,.10);
    animation: pulse 2s infinite; /* Gentle pulse for fun */
  }
  @keyframes pulse {
    0% { transform: scale(1); }
    50% { transform: scale(1.1); }
    100% { transform: scale(1); }
  }

  /* TIMELINE (Enhanced for interactivity) */
  .timeline {
    position: relative;
    margin: .75rem 0 1.25rem 0.3rem;
    padding-left: 1.2rem;
  }
  .timeline::before {
    content: "";
    position: absolute;
    left: .3rem; top: .2rem; bottom: .2rem;
    width: 2px; background: linear-gradient(var(--accent), var(--accent-2));
  }
  .t-item {
    position: relative;
    margin: 1.15rem 0 1.2rem;
    padding: 1rem;
    background: rgba(255, 255, 255, 0.8);
    border-radius: 12px;
    box-shadow: 0 4px 12px var(--ring);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  .t-item:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 20px rgba(255,182,193,.2); /* Pinkish shadow on hover */
  }
  .t-item::before {
    content: "";
    position: absolute;
    left: -1.45rem; top: 1.5rem;
    width: 14px; height: 14px; border-radius: 50%;
    background: var(--accent);
    box-shadow: 0 0 0 4px rgba(255,182,193,.12);
  }
  .t-role { font-weight: 700; color: var(--accent); }
  .t-org { color: var(--muted); font-weight: 600; }
  .t-note { margin: .35rem 0 0; color: var(--ink); }
  .t-reflection { margin-top: .5rem; font-style: italic; color: var(--muted); font-size: 0.95rem; }

  /* HIGHLIGHTS / CHIPS */
  .chips {
    display: grid; gap: .6rem;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    margin-top: .6rem;
  }
  .chip {
    background: var(--chip);
    border: 1px solid rgba(255,182,193,.1);
    padding: .9rem 1rem;
    border-radius: 12px;
    box-shadow: 0 4px 14px var(--ring);
    transition: background 0.3s ease;
  }
  .chip:hover {
    background: rgba(255,182,193,.15); /* Light pink hover */
  }
  .chip b { display: block; margin-bottom: .25rem; color: var(--accent); }
  .chip small { color: var(--muted); }
  .chip details summary { cursor: pointer; font-weight: 600; color: var(--ink); transition: color 0.3s; }
  .chip details summary:hover { color: var(--accent); }
  .chip details[open] summary { color: var(--accent); }

  /* ACCORDION (Publications / Writing) */
  .accordion { border-radius: 14px; overflow: hidden; border: 1px solid rgba(255,182,193,.1); background: rgba(255,255,255,0.9); }
  .acc-item + .acc-item { border-top: 1px solid rgba(255,182,193,.1); }
  .acc-btn {
    width: 100%; text-align: left;
    padding: .95rem 1.1rem;
    background: var(--card);
    border: 0; cursor: pointer; font-weight: 700;
    display: flex; align-items: center; justify-content: space-between;
    transition: background 0.3s ease;
  }
  .acc-btn:hover { background: rgba(255,182,193,.1); }
  .acc-btn span { color: var(--muted); font-weight: 600; font-size: .95rem; }
  .acc-panel {
    display: none; padding: .9rem 1.1rem 1.1rem;
    background: #fff;
  }
  .acc-panel p { margin: .45rem 0 .4rem; color: var(--ink); }
  .acc-panel a { color: var(--accent); text-decoration: underline; }
  .acc-reflection { font-style: italic; color: var(--muted); margin-top: 0.5rem; }

  /* MEDIA STRIP */
  .media-row {
    display: grid; gap: .75rem;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  }
  .media-card {
    background: var(--card);
    border: 1px solid rgba(255,182,193,.1);
    border-radius: 12px; padding: .85rem 1rem;
    box-shadow: 0 4px 12px var(--ring);
    transition: transform 0.3s ease;
  }
  .media-card:hover {
    transform: translateY(-3px); /* Lift on hover for fun */
  }
  .media-card a { color: var(--accent); text-decoration: none; font-weight: 700; }
  .media-card a:hover { text-decoration: underline; }

  /* CTA */
  .cta {
    margin-top: 2rem;
    background: linear-gradient(120deg, rgba(255,182,193,.08), rgba(255,218,185,.08));
    border: 1px dashed rgba(255,182,193,.35);
    border-radius: 14px;
    padding: 1.1rem 1.2rem;
    text-align: center;
  }
  .cta p { margin: .4rem 0 .8rem; color: var(--muted); }
  .cta a.btn {
    display: inline-block; padding: .55rem .9rem; border-radius: 10px;
    background: var(--accent); color: #fff; text-decoration: none; font-weight: 700;
    box-shadow: 0 10px 20px rgba(255,182,193,.15);
    transition: transform 0.3s ease;
  }
  .cta a.btn:hover { transform: scale(1.05); } /* Fun scale on hover */

  /* LINKS */
  .about-wrap a { color: var(--accent); text-decoration: underline; }
  .about-wrap a:hover { text-decoration: none; }

  @media (max-width: 700px) {
    .hero { grid-template-columns: 72px 1fr; }
    .hero .pic { width: 72px; height: 72px; border-radius: 12px; }
  }
</style>

<div class="about-wrap">

  <!-- HERO (Added more authentic content) -->
  <section class="hero">
    <div class="pic">
      <!-- swap if you want a different photo than the sidebar -->
      <img src="{{ site.avatar }}" alt="Purvi Jain">
    </div>
    <div>
      <h1>Hi, I’m <span class="underline">Purvi Jain</span> 👋</h1>
      <p>Technologist by training, philosopher by calling, and environmental activist at heart. I explore how we design <em>just</em> digital systems, always questioning: What if technology could amplify human values instead of eroding them?</p>
      <div class="personal-note">Growing up in India, I fell in love with coding, but it was the ethical dilemmas in tech that truly captured my curiosity—leading me to blend philosophy with AI to build a fairer future.</div>
    </div>
  </section>

  <!-- EDUCATION / TIMELINE (Enhanced with reflections for authenticity) -->
  <h2 class="section-title"><span class="dot"></span> Academic Journey</h2>
  <div class="timeline">

    <div class="t-item">
      <div class="t-role">Workshop on LLMs &amp; Philosophy</div>
      <div class="t-org">Berlin — May 2025</div>
      <p class="t-note">Semantic, cognitive, and moral implications of foundation models; how prompting reshapes technical decision-making.</p>
      <div class="t-reflection">This workshop deepened my fascination with how language models challenge our notions of knowledge and ethics—it's where I first explored prompting as a form of philosophical inquiry.</div>
    </div>

    <div class="t-item">
      <div class="t-role">Summer School in Ethics of AI</div>
      <div class="t-org">London School of Economics</div>
      <p class="t-note">Transparency, epistemic authority, and LLMs from ethical &amp; political perspectives.</p>
      <div class="t-reflection">Here, I grappled with the power dynamics in AI, realizing that true transparency isn't just technical—it's about empowering people to question the systems around them.</div>
    </div>

    <div class="t-item">
      <div class="t-role">Master’s in Philosophy</div>
      <div class="t-org">University of Glasgow</div>
      <p class="t-note">Dissertation: <em>Towards an Unbiased AI: Integrating Rawls’ Theory of Justice into Ethical AI Frameworks</em>.</p>
      <div class="t-reflection">My dissertation was a personal quest to marry Rawls' veil of ignorance with AI design, ensuring fairness isn't an afterthought but the foundation of innovation.</div>
    </div>

    <div class="t-item">
      <div class="t-role">Bachelor’s in Information Technology / Computer Science</div>
      <div class="t-org">India</div>
      <p class="t-note">Began with code &amp; systems; stayed for the hard questions about power, bias, and responsibility.</p>
      <div class="t-reflection">This is where it all started—coding late nights turned into pondering: Who does this tech serve? It sparked my lifelong commitment to ethical tech.</div>
    </div>

  </div>

  <!-- GREENBEANS HIGHLIGHT (Placed after timeline, enhanced with more content and infographic-like list) -->
  <h2 class="section-title" id="greenbeans"><span class="dot"></span> GreenBeans Society · E-Waste Activism</h2>
  <p style="margin-bottom: 1rem; color: var(--muted);">As a co-founder and president, this initiative is close to my heart—it's where my tech background met my passion for the environment, turning e-waste from a problem into a community-driven solution.</p>

  <div class="chips">
    <div class="chip">
      <b>What it is</b>
      <small>First student-led e-waste movement in Chhattisgarh. We focused on education, advocacy, and action to reduce electronic waste's environmental impact.</small>
      <div class="t-reflection" style="margin-top: 0.5rem;">Starting this society felt like planting seeds—literally 'green beans'—for a sustainable tech ecosystem in my home state.</div>
    </div>

    <div class="chip">
      <b>Impact</b>
      <ul class="mini" style="list-style-type: disc; padding-left: 1rem; color: var(--ink);">
        <li>Reached <b>100+ colleges</b> in ~3 months via campaigns & workshops</li>
        <li>Convinced universities to <b>recycle legacy IT</b> instead of discarding</li>
        <li>Shifted framing: e-waste as a <b>shared civic responsibility</b></li>
        <li>Inspired local policies and raised awareness among thousands of students</li>
      </ul>
      <div class="t-reflection" style="margin-top: 0.5rem;">The real win was seeing students take ownership—proving that small actions can spark big change in how we handle tech's footprint.</div>
    </div>

    <div class="chip">
      <b>Media</b>
      <small>
        📺 <a href="https://youtu.be/OgPp5OKAzEU?si=7yFxgIxdfUA-qFaJ" target="_blank" rel="noopener">Intro video →</a>
      </small>
      <div class="t-reflection" style="margin-top: 0.5rem;">This video captures the energy of our campaigns—moments that remind me why activism matters.</div>
    </div>
  </div>

  <!-- HIGHLIGHTS (Chips with added authentic reflections) -->
  <h2 class="section-title"><span class="dot"></span> Highlights & Communities</h2>
  <div class="chips">
    <div class="chip">
      <b>Reading Group · LLMs & Philosophy</b>
      <details>
        <summary>Interdisciplinary forum at Glasgow</summary>
        <small>Ongoing series bridging systems, semantics, and ethics with faculty & students.</small>
        <div class="t-reflection">These discussions fueled my curiosity, turning abstract ideas into collaborative explorations that shaped my views on AI's moral landscape.</div>
      </details>
    </div>

  <div class="chip">
      <b>United by Fascination for Learning (UFL)</b>
      <details>
        <summary>Podcast-style YouTube series</summary>
        <small>
          Moral theories, conceptual engineering, AI & society.
          <a href="https://www.youtube.com/@unitedbyfascinationforlearning" target="_blank" rel="noopener">Watch →</a>
        </small>
        <div class="t-reflection">UFL is my creative outlet—sharing stories of curiosity that connect tech, philosophy, and life, just like the conversations that inspire me daily.</div>
      </details>
    </div>

  <div class="chip">
      <b>Mentor · IntoUniversity</b>
      <details>
        <summary>Academic confidence & curiosity</summary>
        <small>Volunteer mentoring across disciplines; study skills and purpose-driven learning.</small>
        <div class="t-reflection">Mentoring reminds me of my own journey—helping others find their 'why' in learning is incredibly rewarding and keeps me grounded.</div>
      </details>
    </div>

  <div class="chip">
      <b>Communities</b>
      <details>
        <summary>SWIP UK · MAP · The Aristotelian Society</summary>
        <small>Active participation; organizing, attending, and presenting discussions.</small>
        <div class="t-reflection">These groups are my intellectual home—places where diverse voices challenge and refine my ideas on ethics and justice.</div>
      </details>
    </div>
  </div>

  <!-- PUBLICATIONS / WRITING (Added reflections for authenticity) -->
  <h2 class="section-title"><span class="dot"></span> Publications &amp; Writing</h2>
  <div class="accordion" id="pubs">

  <div class="acc-item">
      <button class="acc-btn">
        <span><i class="fas fa-book-open"></i> Noctua — “Technological Change and the Evolution of Perspectives on Artificial Consciousness.”</span>
        <i class="fas fa-chevron-down"></i>
      </button>
      <div class="acc-panel">
        <p>Philosophical reflections on how technological shifts reframe our theories of mind and moral status.</p>
        <div class="acc-reflection">Writing this piece was a deep dive into consciousness—questioning if AI could ever 'feel' and what that means for our humanity.</div>
        <!-- add link when you have it -->
        <!-- <p><a href="URL" target="_blank">Read the piece →</a></p> -->
      </div>
    </div>

  <div class="acc-item">
      <button class="acc-btn">
        <span>
          <i class="fas fa-book"></i>
          Chapter — “AI, Human Values, and Social Transformation in Learning Societies”
          <span style="margin-left:.4rem; opacity:.75">in <em>Future Learning with AI</em></span>
        </span>
        <i class="fas fa-chevron-down"></i>
      </button>
      <div class="acc-panel">
        <p>
          A chapter arguing for value-aligned AI in civic and educational infrastructures,
          linking normative theories with deployable guardrails for learning systems.
        </p>
        <div class="acc-reflection">This chapter embodies my belief that AI should serve society—drawing from philosophy to create practical tools for equitable education.</div>
        <p><b>ISBN:</b> [add ISBN]</p>
       
   </div>
  </div>

  <div class="acc-item">
      <button class="acc-btn">
        <span><i class="fab fa-medium"></i> Medium Essays — AI ethics, environmental impacts of computing, techno-social justice</span>
        <i class="fas fa-chevron-down"></i>
      </button>
      <div class="acc-panel">
        <p>Accessible writing on fairness, transparency, and design justice.</p>
        <div class="acc-reflection">My Medium pieces are my way of making complex ideas approachable—sparking conversations on how tech can be a force for good.</div>
        <p><a href="https://medium.com/@passionatepurvi07" target="_blank">Visit my Medium profile →</a></p>
      </div>
    </div>

  </div>

  <!-- MEDIA / LINKS (Added short descriptions for authenticity) -->
  <h2 class="section-title"><span class="dot"></span> Media &amp; Links</h2>
  <div class="media-row">
    <div class="media-card">
      <div><i class="fab fa-youtube"></i> <a href="https://www.youtube.com/@unitedbyfascinationforlearning" target="_blank">United by Fascination for Learning</a></div>
      <small>Podcast-style series: moral theories, conceptual engineering, AI &amp; society. Join me in exploring the 'why' behind our world.</small>
    </div>
    <div class="media-card">
      <div><i class="fab fa-github"></i> <a href="https://github.com/purvi9399" target="_blank">GitHub</a></div>
      <small>Mini-projects &amp; audit notebooks (Explainable AI, fairness, tooling). Where I tinker with code to solve real ethical challenges.</small>
    </div>
    <div class="media-card">
      <div><i class="fab fa-linkedin"></i> <a href="https://www.linkedin.com/in/purvi-jain7" target="_blank">LinkedIn</a></div>
      <small>Talks, communities, and ongoing work. Connect with me to discuss building thoughtful tech together.</small>
    </div>
  </div>

  <!-- CTA (Added personal invite for authenticity) -->
  <div class="cta">
    <h3 style="margin:0;">Let’s build thoughtful tech.</h3>
    <p>I’m open to collaborations, guest lectures, research assistance, writing partnerships, or workshops on AI ethics and design justice. If you share my passion for blending philosophy with tech, let's chat!</p>
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
```
