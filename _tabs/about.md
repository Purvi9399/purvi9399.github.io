---
title: About Me
icon: fas fa-user
order: 1
layout: default
---

<!-- Custom Styles for a Fancy and Philosophical Design -->
<style>
  @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&family=Space+Grotesk:wght@400;600&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Carolyna+Pro+Black&family=Great+Vibes&family=Space+Grotesk:wght@400;600&display=swap');

  :root {
    --ink: #111;
    --muted: #595959;
    --accent: #FF69B4;          /* Bold magenta for name */
    --accent-2: #899499;        /* Deeper magenta for headlines */
    --chip: #FFF0F5;            /* Very light pink */
    --card: #fff;
    --ring: rgba(0,0,0,.08);
    --background-gradient: linear-gradient(to bottom, #FFE4E1 0%, #FFFFFF 100%);
    --fancy-shadow: 0 10px 30px rgba(216,27,96,.2);
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
    background: rgba(216,27,96,0.15);
    box-shadow: var(--fancy-shadow);
    transition: transform 0.5s ease, box-shadow 0.5s ease;
  }
  .hero:hover {
    transform: translateY(-5px);
    box-shadow: 0 15px 40px rgba(216,27,96,.3);
  }
  .hero .pic {
    width: 160px; height: 160px; border-radius: 50%; overflow: hidden;
    box-shadow: 0 12px 24px rgba(216,27,96,.3);
    transition: transform 0.4s ease;
  }
  .hero .pic:hover { transform: rotate(5deg) scale(1.05); }
  .hero .pic img { width: 100%; height: 100%; object-fit: cover; }
.hero h1 {
  margin: 0;
  line-height: 1.1;
  letter-spacing: .3px;
  color: var(--accent);
  font-family: 'Carolyna Pro Black', cursive;
  font-size: clamp(2.5rem, 2rem + 2vw, 3.5rem);
}
  .hero p { margin: .75rem 0 0; color: var(--muted); font-size: 1.1rem; line-height: 1.6; }
  .hero .personal-note {
    margin-top: 1.25rem;
    font-style: italic;
    color: var(--accent-2);
    font-size: 1rem;
    border-left: 4px solid var(--accent);
    padding-left: 1rem;
    background: rgba(216,27,96,0.1);
    border-radius: 8px;
  }

  .section-title {
    display: inline-flex;
    align-items: center;
    gap: .8rem;
    margin: 3rem 0 1.5rem;
    font-weight: 700;
    letter-spacing: .4px;
    color: var(--accent-2);
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
    background: linear-gradient(to right, var(--accent-2), transparent);
    animation: slide 2s infinite alternate;
  }
  @keyframes slide {
    from { width: 0; }
    to { width: 100%; }
  }
  .section-title .dot {
    width: 14px; height: 14px; border-radius: 50%;
    background: radial-gradient(circle at 30% 30%, var(--accent), var(--accent-2));
    box-shadow: 0 0 0 8px rgba(216,27,96,.15);
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
    box-shadow: 0 0 10px rgba(216,27,96,.1);
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
    box-shadow: 0 12px 36px rgba(216,27,96,.3);
  }
  .t-item::before {
    content: "";
    position: absolute;
    left: -2rem; top: 1.75rem;
    width: 18px; height: 18px; border-radius: 50%;
    background: var(--accent);
    box-shadow: 0 0 0 6px rgba(216,27,96,.2);
    transition: transform 0.3s ease;
  }
  .t-item:hover::before { transform: scale(1.2); }
  .t-role { font-weight: 700; color: var(--accent-2); font-size: 1.2rem; }
  .t-org { color: var(--muted); font-weight: 600; font-size: 1rem; }
  .t-note { margin: .5rem 0 0; color: var(--ink); line-height: 1.6; }
  .t-reflection { margin-top: .75rem; font-style: italic; color: var(--muted); font-size: 0.95rem; background: rgba(216,27,96,0.05); padding: 0.5rem; border-radius: 8px; }

  .philosophical-section {
    margin: 2rem 0;
    padding: 2rem;
    background: linear-gradient(to right, rgba(216,27,96,0.1), rgba(255,255,255,0.9));
    border-left: 6px solid var(--accent-2);
    border-radius: 12px;
    box-shadow: var(--fancy-shadow);
    position: relative;
    overflow: hidden;
  }
  .philosophical-section::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0; bottom: 0;
    background: radial-gradient(circle, rgba(216,27,96,0.05) 0%, transparent 70%);
    z-index: 0;
  }
  .philosophical-section > * {
    position: relative;
    z-index: 1;
  }
  .philosophical-section h3 {
    color: var(--accent-2);
    font-size: 1.6rem;
    margin-bottom: 1rem;
    text-transform: uppercase;
    letter-spacing: 2px;
  }
  .philosophical-section p {
    color: var(--ink);
    font-size: 1.1rem;
    line-height: 1.8;
    margin-bottom: 1rem;
  }
  .philosophical-section .reflection {
    font-style: italic;
    color: var(--accent);
    font-size: 1rem;
    padding: 0.75rem;
    background: rgba(216,27,96,0.1);
    border-radius: 8px;
    display: inline-block;
  }

  .greenbeans-narrative {
    margin: 2rem 0;
    padding: 2rem;
    background: linear-gradient(to bottom, rgba(216,27,96,0.1), rgba(255,255,255,0.9));
    border-top: 4px solid var(--accent-2);
    border-bottom: 4px solid var(--accent-2);
    border-radius: 12px;
    box-shadow: var(--fancy-shadow);
    position: relative;
    overflow: hidden;
  }
  .greenbeans-narrative::before {
    content: '';
    position: absolute;
    top: -50%; left: -50%; width: 200%; height: 200%;
    background: radial-gradient(circle, rgba(216,27,96,0.05) 0%, transparent 70%);
    animation: rotate 10s infinite linear;
  }
  @keyframes rotate {
    from { transform: rotate(0deg); }
    to { transform: rotate(360deg); }
  }
  .greenbeans-narrative > * {
    position: relative;
    z-index: 1;
  }
  .greenbeans-narrative h3 {
    color: var(--accent-2);
    font-size: 1.6rem;
    margin-bottom: 1rem;
    text-transform: uppercase;
    letter-spacing: 2px;
  }
  .greenbeans-narrative p {
    color: var(--ink);
    font-size: 1.1rem;
    line-height: 1.8;
    margin-bottom: 1rem;
  }
  .greenbeans-narrative .timeline-point {
    position: relative;
    padding-left: 1.5rem;
    margin: 1rem 0;
  }
  .greenbeans-narrative .timeline-point::before {
    content: '';
    position: absolute;
    left: 0; top: 0.5rem;
    width: 10px; height: 10px;
    background: var(--accent);
    border-radius: 50%;
    box-shadow: 0 0 0 4px rgba(216,27,96,.2);
  }
  .greenbeans-narrative .video-container {
    margin-top: 1.5rem;
    box-shadow: var(--fancy-shadow);
    transition: transform 0.4s ease;
  }
  .greenbeans-narrative .video-container:hover { transform: scale(1.02); }

  .accordion { border-radius: 16px; overflow: hidden; border: 1px solid rgba(216,27,96,.15); background: rgba(255,255,255,0.95); box-shadow: var(--fancy-shadow); }
  .acc-item + .acc-item { border-top: 1px solid rgba(216,27,96,.15); }
  .acc-btn {
    width: 100%; text-align: left;
    padding: 1.25rem 1.5rem;
    background: var(--card);
    border: 0; cursor: pointer; font-weight: 700;
    display: flex; align-items: center; justify-content: space-between;
    transition: background 0.4s ease, padding-left 0.4s ease;
  }
  .acc-btn:hover { background: rgba(216,27,96,.15); padding-left: 1.75rem; }
  .acc-btn span { color: var(--muted); font-weight: 600; font-size: 1rem; }
  .acc-panel {
    display: none; padding: 1.25rem 1.5rem;
    background: #fff;
  }
  .acc-panel p { margin: .5rem 0 .5rem; color: var(--ink); line-height: 1.6; }
  .acc-panel a { color: var(--accent); text-decoration: underline; transition: color 0.3s; }
  .acc-panel a:hover { color: var(--accent-2); }
  .acc-reflection { font-style: italic; color: var(--muted); margin-top: 0.75rem; padding: 0.5rem; background: rgba(216,27,96,0.05); border-radius: 8px; }

  .cta {
    margin-top: 3rem;
    background: linear-gradient(120deg, rgba(216,27,96,.2), rgba(255,255,255,0.9));
    border: 1px dashed rgba(216,27,96,.5);
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
    box-shadow: 0 12px 24px rgba(216,27,96,.3);
    transition: transform 0.3s ease;
  }
  .cta a.btn:hover { transform: scale(1.1); }

  .about-wrap a { color: var(--accent); text-decoration: underline; transition: color 0.3s; }
  .about-wrap a:hover { color: var(--accent-2); text-decoration: none; }

  @media (max-width: 700px) {
    .hero { grid-template-columns: 1fr; text-align: center; }
    .hero .pic { margin: 0 auto; }
    .philosophical-section, .greenbeans-narrative { padding: 1.5rem; }
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
    <h1>Hi, I’m <span class="underline">Purvi Jain</span> </h1>
    <p>Technologist by training, philosopher by calling, and environmental activist at heart. I explore how we design <em>just</em> digital systems, asking: How can technology amplify fairness, sustainability, and human dignity? My journey spans coding in India, debating ethics in Glasgow, and leading grassroots movements, blending tech with purpose to create a better future.</p>
    <div class="personal-note">From unraveling AI’s moral complexities to turning e-waste into a civic mission, I’m driven by curiosity and a commitment to ethical innovation. Let’s connect to shape a world where tech serves us all.</div>
  </div>
</section>

  <!-- Why I Do, What I Do -->
  <div class="philosophical-section">
    <h3>Why I Do, What I Do ?</h3>
    <p>I’m Purvi Jain. For me, philosophy and technology aren’t just subjects I studied, they’re the threads I’ve been trying to weave together in everything I do. I started with code, but I kept asking bigger questions: what does it mean, who does it serve, and what kind of future are we building with it? That’s what led me from the streets of India to classrooms in Glasgow, where I spent time wrestling with ideas of justice and fairness.</p>

<p>I don’t see AI as just a tool for efficiency; I see it as a reflection of us, our choices, our biases, our values. My work with e-waste came from the same place: a respect for the environment and a belief that even discarded things still carry meaning and potential.</p>

<p>What drives me is connection — between people, between disciplines, between ideas. Whether I’m writing, mentoring, or building projects, I want to help make technology more humane, more just, and more thoughtful. That’s really my purpose: to bring philosophy into tech so that every line of code, every system we build, can be part of a better story for all of us..</p>
    <p class="reflection">At my core, I’m a dreamer who puts ideas into action, guided by one question: what kind of world are we leaving behind?</p>
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
      <p class="t-note">Studied transparency, epistemic authority, and LLMs from ethical and political lenses. </p>
      <div class="t-reflection">Examined how emerging technologies shape human agency, fairness, privacy, and global justice; explored anticipatory ethics and the governance of AI.</div>
    </div>
    <div class="t-item">
      <div class="t-role">Master’s in Philosophy</div>
      <div class="t-org">University of Glasgow</div>
      <p class="t-note">Dissertation: <em>Towards an Unbiased AI: Integrating Rawls’ Theory of Justice into Ethical AI Frameworks</em>.</p>
      <div class="t-reflection"> <p>Logic & Critical Reasoning: Formal/informal logic, argumentation, and evaluation of ethical and metaphysical claims.</p>

<p>Moral & Political Philosophy: Theories of justice, equality, rights, and responsibility (Rawls, Nozick, Sen, Nussbaum, etc.).</p></div>
    </div>
    <div class="t-item">
      <div class="t-role">Bachelor’s in Information Technology</div>
      <div class="t-org">National Institue of Technology Raipur, India</div>
      <p class="t-note">During my undergraduate studies, I built a strong foundation in both theoretical and applied aspects of computer science. Key areas of learning included:</p>

<p>Programming & Software Development: Proficiency in C, C++, Java, and Python; object-oriented programming; data structures and algorithms; software engineering practices.</p>

<p>Systems & Networks: Operating systems, computer networks, distributed systems, and database management systems (SQL, NoSQL).</p>

<p>Web & Application Development: Fundamentals of front-end and back-end development, exposure to frameworks and APIs.</p>
      <div class="t-reflection"> Projects: Breast Cancer Classification, Bias checker using LIME </div>
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
  <div class="greenbeans-narrative">
    <h3>GreenBeans Initiative: A Movement Born of Purpose</h3>
    <p>I co-founded and continue to serve as the President of GreenBeans, the first-ever student-led e-waste movement in Chhattisgarh. What began as a small group of just three or four friends driven by concern for the environment has now grown into a community of over 30 active members. GreenBeans was born out of a simple but urgent idea: to spread awareness about the dangers of electronic waste in a state where this conversation had never truly begun.</p>
    <div class="timeline-point">As pioneers, we partnered with Raipur Smart City and the Chhattisgarh Environment Conservation Board (CECB), crafting projects that linked young people with city-level sustainability efforts.</div>
    <div class="timeline-point">We launched awareness campaigns, organized plantation drives, and hosted educational workshops, proving that environmental action can be both hands-on and deeply collaborative.</div>
    <div class="timeline-point">What started as a small initiative among friends has blossomed into a movement that inspires others to rethink waste, sustainability, and their role in protecting our shared future.</div>
    <div class="video-container">
      <iframe src="https://www.youtube.com/embed/OgPp5OKAzEU" title="GreenBeans Society Intro Video" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
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
        <summary>SWIP UK · MAP · The Aristotelian Society</summary>
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
  gsap.utils.toArray('.t-item, .chip, .log-item, .media-card, .acc-item, .timeline-point').forEach((item, i) => {
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
