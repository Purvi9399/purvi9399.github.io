---
title: Projects
icon: fas fa-toolbox
order: 2
---


<!-- Custom Styling for Projects Page -->
<style>
  .projects-header {
    max-width: 900px;
    margin: 0 auto;
    text-align: center;
    padding: 2.5rem 1rem 1rem;
    font-family: 'Space Grotesk', sans-serif;
  }
  .projects-header h1 {
    font-size: 2.2rem;
    font-weight: 700;
    color: #2c2c2c;
    margin-bottom: 1rem;
  }
  .projects-header p {
    font-size: 1.1rem;
    color: #444;
    line-height: 1.7;
  }
  .project-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 2rem;
    justify-content: center;
    padding: 2rem 1rem;
  }
  .project-card {
    background-color: #f3e6ed;
    border-radius: 14px;
    padding: 1.5rem;
    max-width: 340px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    font-family: 'Space Grotesk', sans-serif;
  }
  .project-card h3 {
    font-size: 1.3rem;
    margin-bottom: 0.5rem;
    color: #222;
  }
  .project-card p {
    font-size: 1rem;
    color: #333;
  }
  .project-card img {
    width: 100%;
    border-radius: 10px;
    margin-bottom: 0.8rem;
  }
  .project-card a {
    display: inline-block;
    margin-top: 0.5rem;
    color: #8a2be2;
    font-weight: bold;
  }
</style>

<!-- Header Section -->
<div class="projects-header">
  <h1>Welcome to my <span style="color:#8a2be2;">Mini-Project Portfolio</span></h1>
  <p>
    Each of these projects explores a real-world AI ethics dilemma — from bias in toxic language models to responsible design and explainability. They combine reflection and research with working code, and are part of my ongoing effort to bridge tech with philosophy.
  </p>
</div>

<!-- Projects Grid -->
<div class="project-grid">

  <!-- Project 1: Bias Checker -->
  <div class="project-card">
    <img src="/assets/img/bias-project.png" alt="Bias Checker Project Screenshot" />
    <h3>Bias Checker with LIME</h3>
    <p>A hands-on explainable AI project using LIME and Google Perspective API to audit model bias across identity groups.</p>
    <a href="https://github.com/Purvi9399/bias-audit-toxic-language" target="_blank">View on GitHub</a>
  </div>

  <!-- Project 2 -->
  <div class="project-card">
    <img src="/assets/img/second-project.png" alt="Project 2" />
    <h3>Coming Soon</h3>
    <p>This space will feature my upcoming work on digital rights, data privacy, or LLM transparency tools.</p>
  </div>

  <!-- Project 3 -->
  <div class="project-card">
    <img src="/assets/img/third-project.png" alt="Project 3" />
    <h3>Coming Soon</h3>
    <p>Another ethically-grounded AI project — exploring fairness, sustainability, or digital governance.</p>
  </div>

</div>
