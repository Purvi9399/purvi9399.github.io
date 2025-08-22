---
title: Home
layout: default
permalink: /
icon: home
order: 0
---

<!-- Custom Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Fira+Sans:wght@400;600&family=DM+Serif+Display&display=swap" rel="stylesheet">

<!-- Parallax Background -->
<div style="background: url('/assets/img/parallax-bg.jpg'); background-size: cover; background-position: center; background-repeat: no-repeat; padding: 5rem 1rem; text-align: center; color: white;">
  <img src="/assets/img/avatar.jpg" alt="Purvi Jain" style="width: 150px; height: 150px; border-radius: 50%; border: 2px solid #fff; box-shadow: 0 0 15px rgba(255,255,255,0.3);" loading="lazy">
  
  <h1 id="typed-text" style="font-size: 2.8rem; font-family: 'DM Serif Display', serif; margin-top: 1rem;"></h1>
  
  <p style="font-size: 1.2rem; max-width: 700px; margin: 1rem auto; font-family: 'Fira Sans', sans-serif;">
    Exploring AI, ethics, and digital futures, one idea at a time.
  </p>
  
  <a href="/tabs/projects" class="btn-custom" style="display: block; margin: 0 auto; width: fit-content; background-color: #a855f7; color: white; padding: 12px 24px; border-radius: 12px; text-decoration: none; font-family: 'Fira Sans', sans-serif; font-weight: 600; border: 2px solid #a855f7; transition: all 0.3s ease;">
    View Latest Project
  </a>
</div>

<!-- Featured Sections -->
<div style="max-width: 900px; margin: 4rem auto; font-family: 'Fira Sans', sans-serif;">
  <h2 style="font-family: 'Philosopher', serif; font-weight: 700; color: #4A5568; text-shadow: 0 2px 4px rgba(0,0,0,0.1);">Featured Sections</h2>

  <style>
    .feature-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 2rem; /* Increased gap for more space */
      max-width: 900px;
      margin: 0 auto;
    }
    .feature-card .title {
      display: flex; align-items: center; gap: 0.5rem; font-weight: 700; font-family: 'Philosopher', serif;
    }
    .feature-card i { color: #667EEA; }
    .feature-card {
      background: #F7FAFC;
      padding: 1.5rem;
      border-radius: 12px;
      box-shadow: 0 6px 12px rgba(0,0,0,0.05);
      transition: transform 0.3s ease;
    }
    .feature-card:hover {
      transform: translateY(-5px);
    }
    @media (max-width: 600px) {
      .feature-grid {
        grid-template-columns: 1fr;
      }
    }
    .btn-custom {
      background-color: #a855f7;
      color: white;
      padding: 12px 24px;
      border-radius: 12px;
      text-decoration: none;
      font-weight: 600;
      font-family: 'Fira Sans', sans-serif;
      border: 2px solid #a855f7;
      transition: all 0.3s ease;
    }
    .btn-custom:hover {
      background-color: #7c3aed;
      border-color: #7c3aed;
    }
    .card-hover {
      flex: 1 1 250px;
      background: #F3F4F6;
      padding: 1.5rem;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.05);
      text-decoration: none;
      color: #111;
      transition: transform 0.2s ease, background 0.3s ease;
    }
    .card-hover:hover {
      background: #E0E7FF;
      transform: translateY(-5px);
    }
  </style>

  <div class="feature-grid">
    <a href="/tabs/projects" class="card-hover feature-card">
      <div class="title"><i class="fas fa-code"></i> Projects</div>
      <div>Mini tools, ethical experiments, and AI prototypes.</div>
    </a>

    <a href="/tabs/ethical" class="card-hover feature-card">
      <div class="title"><i class="fas fa-pen-nib"></i> Ethical Writing</div>
      <div>Essays on fairness, justice, and tech futures.</div>
    </a>

    <a href="/posts" class="card-hover feature-card">
      <div class="title"><i class="fas fa-feather-alt"></i> Blogs</div>
      <div>Thoughts on research, reflection, and learning.</div>
    </a>

    <a href="https://peppy-crepe-048cfc.netlify.app/" target="_blank" rel="noopener" class="card-hover feature-card">
      <div class="title"><i class="fas fa-compass"></i> Travel Vlog</div>
      <div style="margin-top: 1rem;">A scrapbook of journeys with my best friend, where every trip becomes a postcard of laughter, love, and natsukashii memories.</div>
    </a>
  </div>

  <h2 style="margin-top: 3rem; font-family: 'Philosopher', serif; font-weight: 700; color: #4A5568; text-shadow: 0 2px 4px rgba(0,0,0,0.1);">Why AI Needs Philosophy?</h2>
  <p style="font-family: 'Fira Sans', sans-serif; line-height: 1.6; color: #2D3748;">
    Technology shapes the world, but ethics shapes technology. This space is where code meets conscience.
  </p>
  <p style="font-family: 'Fira Sans', sans-serif; line-height: 1.6; color: #2D3748;">
    AI is not just about data and decisions, it’s about values, power, and people. Philosophy asks the questions that
    technology often ignores: What is fairness? Who gets to decide? What kind of future are we building? This section is
    where I reflect on the ethical assumptions embedded in our systems and ask how we can do better, not just as engineers,
    but as citizens. Philosophy doesn’t slow down innovation; it gives it direction.
  </p>

  <h3 style="font-family: 'Philosopher', serif; font-weight: 700; color: #4A5568;">Recent Blog</h3>
  <p><a href="/posts/2025-07-22-welcome" style="color: #667EEA; text-decoration: none; transition: color 0.3s;">Welcome to AI Ethics Explorer →</a></p>
</div>

<!-- Glossary of Terminology on Ethics of AI -->
<div style="max-width: 900px; margin: 4rem auto; text-align: center; font-family: 'Fira Sans', sans-serif;">
  <h2 style="font-family: 'Philosopher', serif; font-weight: 700; color: #F472B6; text-shadow: 0 2px 4px rgba(0,0,0,0.1);">Glossary of Terminology on Ethics of AI</h2>
  <p style="max-width: 700px; margin: 1rem auto; font-size: 1.1rem; line-height: 1.6; color: #2D3748;">
    Hover over the cards to flip and explore key ethical concepts in AI.
  </p>
  <div style="display: grid; grid-template-columns: 1fr 1fr; grid-template-rows: 1fr 1fr; gap: 1.5rem; perspective: 1000px;">
    <div class="flip-card" style="background: #F7FAFC; padding: 1.5rem; border-radius: 12px; box-shadow: 0 6px 12px rgba(0,0,0,0.05); transition: transform 0.6s; transform-style: preserve-3d;">
      <div class="flip-card-inner" style="position: relative; width: 100%; height: 100%; transform-style: preserve-3d; transition: transform 0.6s;">
        <div class="flip-card-front" style="position: absolute; width: 100%; height: 100%; backface-visibility: hidden;">
          <h3 style="font-family: 'Philosopher', serif; color: #4A5568;">Fairness</h3>
        </div>
        <div class="flip-card-back" style="position: absolute; width: 100%; height: 100%; backface-visibility: hidden; transform: rotateY(180deg); padding: 1rem; background: #FCE7F3; border-radius: 12px; box-shadow: inset 0 0 10px rgba(0,0,0,0.05);">
          <p style="font-family: 'Fira Sans', sans-serif; color: #831843; line-height: 1.5;">Fairness in AI ensures equitable treatment across all individuals, mitigating discrimination based on race, gender, or socioeconomic status. It involves designing systems that prioritize justice and equal opportunity.</p>
          <div style="margin-top: 1rem; border-left: 4px solid #F472B6; padding-left: 0.5rem;">🌱 Ethical Balance</div>
        </div>
      </div>
    </div>

    <div class="flip-card" style="background: #F7FAFC; padding: 1.5rem; border-radius: 12px; box-shadow: 0 6px 12px rgba(0,0,0,0.05); transition: transform 0.6s; transform-style: preserve-3d;">
      <div class="flip-card-inner" style="position: relative; width: 100%; height: 100%; transform-style: preserve-3d; transition: transform 0.6s;">
        <div class="flip-card-front" style="position: absolute; width: 100%; height: 100%; backface-visibility: hidden;">
          <h3 style="font-family: 'Philosopher', serif; color: #4A5568;">Bias</h3>
        </div>
        <div class="flip-card-back" style="position: absolute; width: 100%; height: 100%; backface-visibility: hidden; transform: rotateY(180deg); padding: 1rem; background: #FCE7F3; border-radius: 12px; box-shadow: inset 0 0 10px rgba(0,0,0,0.05);">
          <p style="font-family: 'Fira Sans', sans-serif; color: #831843; line-height: 1.5;">Bias in AI occurs when models reflect human prejudices embedded in training data, leading to skewed outcomes. Addressing bias requires rigorous data auditing and inclusive design.</p>
          <div style="margin-top: 1rem; border-left: 4px solid #F472B6; padding-left: 0.5rem;">📊 Data Reflection</div>
        </div>
      </div>
    </div>

    <div class="flip-card" style="background: #F7FAFC; padding: 1.5rem; border-radius: 12px; box-shadow: 0 6px 12px rgba(0,0,0,0.05); transition: transform 0.6s; transform-style: preserve-3d;">
      <div class="flip-card-inner" style="position: relative; width: 100%; height: 100%; transform-style: preserve-3d; transition: transform 0.6s;">
        <div class="flip-card-front" style="position: absolute; width: 100%; height: 100%; backface-visibility: hidden;">
          <h3 style="font-family: 'Philosopher', serif; color: #4A5568;">Privacy</h3>
        </div>
        <div class="flip-card-back" style="position: absolute; width: 100%; height: 100%; backface-visibility: hidden; transform: rotateY(180deg); padding: 1rem; background: #FCE7F3; border-radius: 12px; box-shadow: inset 0 0 10px rgba(0,0,0,0.05);">
          <p style="font-family: 'Fira Sans', sans-serif; color: #831843; line-height: 1.5;">Privacy in AI protects user data from misuse, balancing innovation with individual autonomy. It demands robust safeguards to maintain trust in digital systems.</p>
          <div style="margin-top: 1rem; border-left: 4px solid #F472B6; padding-left: 0.5rem;">🔒 Personal Sanctuary</div>
        </div>
      </div>
    </div>

    <div class="flip-card" style="background: #F7FAFC; padding: 1.5rem; border-radius: 12px; box-shadow: 0 6px 12px rgba(0,0,0,0.05); transition: transform 0.6s; transform-style: preserve-3d;">
      <div class="flip-card-inner" style="position: relative; width: 100%; height: 100%; transform-style: preserve-3d; transition: transform 0.6s;">
        <div class="flip-card-front" style="position: absolute; width: 100%; height: 100%; backface-visibility: hidden;">
          <h3 style="font-family: 'Philosopher', serif; color: #4A5568;">Trustworthiness</h3>
        </div>
        <div class="flip-card-back" style="position: absolute; width: 100%; height: 100%; backface-visibility: hidden; transform: rotateY(180deg); padding: 1rem; background: #FCE7F3; border-radius: 12px; box-shadow: inset 0 0 10px rgba(0,0,0,0.05);">
          <p style="font-family: 'Fira Sans', sans-serif; color: #831843; line-height: 1.5;">Trustworthiness in AI reflects reliability, transparency, and accountability. It ensures systems are dependable and their decisions can be understood and verified by users.</p>
          <div style="margin-top: 1rem; border-left: 4px solid #F472B6; padding-left: 0.5rem;">🤝 Reliable Bond</div>
        </div>
      </div>
    </div>
  </div>
  <style>
    .flip-card:hover .flip-card-inner {
      transform: rotateY(180deg);
    }
    .flip-card {
      position: relative;
      min-height: 150px;
    }
    .flip-card-front, .flip-card-back {
      position: absolute;
      top: 0; left: 0; width: 100%; height: 100%;
      display: flex; align-items: center; justify-content: center;
      backface-visibility: hidden;
    }
    @media (max-width: 600px) {
      .flip-card {
        min-height: 120px;
      }
    }
  </style>
</div>

<!-- 🎙️ YouTube Podcast Section -->
<div style="max-width: 900px; margin: 4rem auto; text-align: center; font-family: 'Fira Sans', sans-serif;">
  <h2 style="font-family: 'Philosopher', serif; font-weight: 700; color: #4A5568; text-shadow: 0 2px 4px rgba(0,0,0,0.1);">🎙️ United by Fascination for Learning</h2>
  <p style="max-width: 700px; margin: 1rem auto; font-size: 1.1rem;">
    I also host a podcast and YouTube channel exploring curiosity, meaning, and interdisciplinary learning. 
    Join me as I talk about philosophy, tech, ethics, and everything in between.
  </p>
  <iframe width="100%" height="315" src="https://www.youtube.com/embed/O9JnMjOlDcw" 
    title="YouTube video player" frameborder="0" allowfullscreen style="border-radius: 12px; box-shadow: 0 0 15px rgba(0,0,0,0.1);">
  </iframe>
  <p style="margin-top: 1rem;">
    <a href="https://www.youtube.com/@unitedbyfascinationforlearning" target="_blank" class="btn-custom">
      📺 Watch More on YouTube
    </a>
  </p>
</div>

<!-- Typing Animation Script -->
<script src="https://cdn.jsdelivr.net/npm/typed.js@2.0.12"></script>
<script>
  var typed = new Typed("#typed-text", {
    strings: [
      "Hi, I’m Purvi Jain.",
      "Researcher. Writer. Explorer of Ethical AI.",
      "Welcome to my digital garden 🌱"
    ],
    typeSpeed: 50,
    backSpeed: 25,
    loop: true
  });
</script>

<!-- Footer -->
<footer style="text-align: center; margin-top: 5rem; font-size: 0.9rem; color: #888;">
  © 2025 — Built with love, code, and critical questions 
</footer>
