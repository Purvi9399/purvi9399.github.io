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

<div class="about-wrap" role="main">

  <!-- Big Description Hero -->
  <section class="hero" role="banner" aria-label="Introduction to Purvi Jain">
    <div class="pic">
      <img src="{{ site.avatar }}" alt="Purvi Jain, technologist and philosopher">
    </div>
    <div>
      <h1>Hi, I’m <span class="underline">Purvi Jain</span></h1>
      <p>Technologist by training, philosopher by calling, and environmental activist at heart. I explore how we design <em>just</em> digital systems, asking: How can technology amplify fairness, sustainability, and human dignity? My journey spans coding in India, debating ethics in Glasgow, and leading grassroots movements—blending tech with purpose to create a better future.</p>
      <div class="personal-note">From unraveling AI’s moral complexities to turning e-waste into a civic mission, I’m driven by curiosity and a commitment to ethical innovation. Let’s connect to shape a world where tech serves us all.</div>
    </div>
  </section>

  <!-- What I Do -->
  <h2 class="section-title"><span class="dot"></span> What I Do</h2>
  <div class="chips">
    <div class="chip">
      <b>AI Ethics Research</b>
      <small>Developing frameworks to integrate Rawls’ Theory of Justice into AI, tackling bias and fairness.</small>
      <div class="t-reflection">I aim to make AI a tool for equity, not division.</div>
    </div>
    <div class="chip">
      <b>Environmental Activism</b>
      <small>Leading e-waste initiatives and advocating for sustainable tech practices.</small>
      <div class="t-reflection">Tech should heal, not harm, our planet.</div>
    </div>
    <div class="chip">
      <b>Interdisciplinary Learning</b>
      <small>Hosting podcasts and reading groups on AI, philosophy, and society.</small>
      <div class="t-reflection">Connecting ideas across fields fuels my passion.</div>
    </div>
    <div class="chip">
      <b>Education & Writing</b>
      <small>Mentoring students and writing on AI ethics and social justice.</small>
      <div class="t-reflection">Sharing knowledge to inspire change is my joy.</div>
    </div>
  </div>

  <!-- Education Timeline -->
  <h2 class="section-title"><span class="dot"></span> Education Timeline</h2>
  <div class="timeline" role="region" aria-label="Purvi's academic timeline">
    <div class="t-item">
      <div class="t-role">Workshop on LLMs & Philosophy</div>
      <div class="t-org">Berlin — May 2025</div>
      <p class="t-note">Explored semantic, cognitive, and moral implications of foundation models and prompting’s role in decision-making.</p>
      <div class="t-reflection">A philosophical dive into AI’s future.</div>
    </div>
    <div class="t-item">
      <div class="t-role">Summer School in Ethics of AI</div>
      <div class="t-org">London School of Economics</div>
      <p class="t-note">Studied transparency, epistemic authority, and LLMs from ethical and political lenses.</p>
      <div class="t-reflection">Learned how power shapes AI ethics.</div>
    </div>
    <div class="t-item">
      <div class="t-role">Master’s in Philosophy</div>
      <div class="t-org">University of Glasgow</div>
      <p class="t-note">Dissertation: <em>Towards an Unbiased AI: Integrating Rawls’ Theory of Justice into Ethical AI Frameworks</em>.</p>
      <div class="t-reflection">A cornerstone of my mission to align tech with justice.</div>
    </div>
    <div class="t-item">
      <div class="t-role">Bachelor’s in Information Technology</div>
      <div class="t-org">National Institute of Technology Raipur, India</div>
      <p class="t-note">Laid the foundation with coding, sparking my interest in tech’s ethical challenges.</p>
      <div class="t-reflection">Where my journey began.</div>
    </div>
  </div>

  <!-- Publications -->
  <h2 class="section-title"><span class="dot"></span> Publications</h2>
  <div class="accordion" id="pubs">
    <div class="acc-item">
      <button class="acc-btn" aria-expanded="false" aria-controls="pub1">
        <span><i class="fas fa-book-open"></i> Noctua — “Technological Change and the Evolution of Perspectives on Artificial Consciousness.”</span>
        <i class="fas fa-chevron-down"></i>
      </button>
      <div class="acc-panel" id="pub1">
        <p>Philosophical reflections on how technological shifts redefine theories of mind and moral status.</p>
        <div class="acc-reflection">A deep exploration of AI’s consciousness debate.</div>
      </div>
    </div>
    <div class="acc-item">
      <button class="acc-btn" aria-expanded="false" aria-controls="pub2">
        <span><i class="fas fa-book"></i> Chapter — “AI, Human Values, and Social Transformation in Learning Societies” <span style="margin-left:.4rem; opacity:.75">in <em>Future Learning with AI</em></span></span>
        <i class="fas fa-chevron-down"></i>
      </button>
      <div class="acc-panel" id="pub2">
        <p>Argues for value-aligned AI in educational and civic systems, blending normative theory with practical guardrails.</p>
        <div class="acc-reflection">A vision for ethical AI in education.</div>
        <p><b>ISBN:</b> [add ISBN]</p>
      </div>
    </div>
    <div class="acc-item">
      <button class="acc-btn" aria-expanded="false" aria-controls="pub3">
        <span><i class="fab fa-medium"></i> Medium Essays — AI ethics, environmental impacts, techno-social justice</span>
        <i class="fas fa-chevron-down"></i>
      </button>
      <div class="acc-panel" id="pub3">
        <p>Accessible writings on fairness, transparency, and design justice.</p>
        <div class="acc-reflection">Bridging complex ideas with real-world impact.</div>
        <p><a href="https://medium.com/@passionatepurvi07" target="_blank" rel="noopener">Visit my Medium profile →</a></p>
      </div>
    </div>
  </div>

  <!-- GreenBeans Initiative -->
  <h2 class="section-title"><span class="dot"></span> GreenBeans Initiative</h2>
  <div class="chips">
    <div class="chip">
      <b>Mission</b>
      <small>First student-led e-waste movement in Chhattisgarh, co-founded and led by me.</small>
      <div class="t-reflection">I co-founded and continue to serve as the President of GreenBeans, the first-ever student-led e-waste movement in Chhattisgarh. What began as a small group of just three or four friends driven by concern for the environment has now grown into a community of over 30 active members. GreenBeans was born out of a simple but urgent idea: to spread awareness about the dangers of electronic waste in a state where this conversation had never truly begun.

As pioneers in this space, we worked closely with Raipur Smart City and the Chhattisgarh Environment Conservation Board (CECB), creating impactful projects that linked young people with city-level sustainability efforts. Alongside awareness campaigns, we also organized plantation drives, educational events, and community workshops, showing that environmental action can be both hands-on and deeply collaborative.

What started as a small initiative among friends has become a movement that inspires others to rethink waste, sustainability, and their role in protecting our shared future.</div>
    </div>
    <div class="chip">
      <b>Impact</b>
      <ul class="mini" style="list-style-type: disc; padding-left: 1rem; color: var(--ink);">
        <li>Reached 100+ colleges in ~3 months via campaigns & workshops</li>
        <li>Convinced universities to recycle legacy IT</li>
        <li>Framed e-waste as a shared civic responsibility</li>
      </ul>
      <div class="t-reflection">A testament to collective environmental action.</div>
    </div>
    <div class="chip">
      <b>Video Story</b>
      <small>📺 <a href="https://youtu.be/OgPp5OKAzEU?si=7yFxgIxdfUA-qFaJ" target="_blank" rel="noopener">Watch our journey →</a></small>
      <div class="video-container">
        <iframe src="https://www.youtube.com/embed/OgPp5OKAzEU" title="GreenBeans Society Intro Video" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </div>
    </div>
  </div>

  <!-- Other Initiatives -->
  <h2 class="section-title"><span class="dot"></span> Other Initiatives</h2>
  <div class="chips">
    <div class="chip">
      <b>Reading Group · LLMs & Philosophy</b>
      <details>
        <summary>Interdisciplinary forum at Glasgow</summary>
        <small>Ongoing series bridging systems, semantics, and ethics with faculty & students.</small>
        <div class="t-reflection">A space for intellectual growth.</div>
      </details>
    </div>
    <div class="chip">
      <b>United by Fascination for Learning (UFL)</b>
      <details>
        <summary>Podcast-style YouTube series</summary>
        <small>Explores moral theories, AI & society. <a href="https://www.youtube.com/@unitedbyfascinationforlearning" target="_blank" rel="noopener">Watch →</a></small>
        <div class="t-reflection">Sharing stories that connect tech and humanity.</div>
      </details>
    </div>
    <div class="chip">
      <b>Mentor · IntoUniversity</b>
      <details>
        <summary>Academic confidence & curiosity</summary>
        <small>Volunteer mentoring across disciplines; study skills and purpose-driven learning.</small>
        <div class="t-reflection">Guiding students to find their passion.</div>
      </details>
    </div>
    <div class="chip">
      <b>Communities</b>
      <details>
        <summary>Society for Women in Philosophy UK · Minorities in Philosophy · The Aristotelian Society</summary>
        <small>Active participation; organizing and presenting discussions.</small>
        <div class="t-reflection">Growing through diverse philosophical voices.</div>
      </details>
    </div>
  </div>

  <!-- Option to Collaborate -->
  <h2 class="section-title"><span class="dot"></span> Collaborate With Me</h2>
  <div class="cta">
    <h3 style="margin:0;">Let’s Build Thoughtful Tech Together</h3>
    <p>I’m open to collaborations, guest lectures, research partnerships, or workshops on AI ethics, sustainability, and design justice. Let’s create something impactful!</p>
    <a class="btn" href="mailto:ipurvijain@gmail.com">Email me</a>
  </div>

</div>

<!-- JS for Fancy Animations -->
<script>
  gsap.registerPlugin(ScrollTrigger);

  gsap.from(".hero", { opacity: 0, y: -50, duration: 1, ease: "power2.out" });
  gsap.utils.toArray('.section-title').forEach(title => {
    gsap.from(title, {
      opacity: 0,
      x: -50,
      duration: 0.8,
      scrollTrigger: {
        trigger: title,
        start: "top 80%",
      }
    });
  });
  gsap.utils.toArray('.t-item, .chip, .log-item, .media-card, .acc-item').forEach((item, i) => {
    gsap.from(item, {
      opacity: 0,
      y: 50,
      duration: 0.8,
      delay: i * 0.15,
      scrollTrigger: {
        trigger: item,
        start: "top 80%",
        toggleActions: "play none none none"
      }
    });
  });

  document.querySelectorAll('.acc-btn').forEach(btn => {
    btn.addEventListener('click', () => {
      const panel = btn.nextElementSibling;
      const isOpen = panel.style.display === 'block';
      document.querySelectorAll('.acc-panel').forEach(p => p.style.display = 'none');
      document.querySelectorAll('.acc-btn i.fas.fa-chevron-down').forEach(i => i.style.transform = 'rotate(0deg)');
      document.querySelectorAll('.acc-btn').forEach(b => b.setAttribute('aria-expanded', 'false'));
      if (!isOpen) {
        panel.style.display = 'block';
        btn.querySelector('i.fas.fa-chevron-down').style.transform = 'rotate(180deg)';
        btn.setAttribute('aria-expanded', 'true');
      }
    });
  });
</script>
