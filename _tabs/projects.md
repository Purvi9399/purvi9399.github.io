---
title: Projects
icon: fas fa-code
order: 2
permalink: /projects/
layout: default
---

<!-- Project Page Custom Styles & Animations -->
<style>
  .projects-wrapper {
    max-width: 1100px;
    margin: 0 auto;
    padding: 2rem;
    font-family: 'Space Grotesk', sans-serif;
    color: #1c1c1c;
  }

  .projects-header {
    text-align: center;
    margin-bottom: 2.5rem;
    opacity: 0;
    animation: fadeIn 1.4s ease-in forwards;
  }

  .projects-header h1 {
    font-size: 2.2rem;
    font-weight: 700;
    margin-bottom: 0.5rem;
  }

  .projects-header p {
    font-size: 1.1rem;
    color: #555;
    max-width: 750px;
    margin: 0 auto;
  }

  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(-20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  .projects-grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 2rem;
  }

  .project-card {
    background-color: #f9f1f6;
    border-radius: 12px;
    padding: 1.5rem;
    width: 280px;
    text-align: center;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.07);
    opacity: 0;
    transform: translateY(30px);
    transition: all 0.6s ease-in-out;
  }

  .project-card.reveal {
    opacity: 1;
    transform: translateY(0);
  }

  .project-card:hover {
    transform: translateY(-8px);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    box-shadow: 0 10px 18px rgba(0, 0, 0, 0.15);
  }

  .project-card h3 {
    font-size: 1.3rem;
    margin-bottom: 0.8rem;
    color: #111;
  }

  .project-card p {
    font-size: 0.95rem;
    color: #333;
    margin-bottom: 1rem;
  }

  .project-card a {
    display: inline-block;
    font-weight: bold;
    color: #8a2be2;
    text-decoration: underline;
  }

  .project-card a:hover {
    text-decoration: none;
  }
</style>

<div class="projects-wrapper">
  <div class="projects-header">
    <h1>Welcome to my <span style="color:#8a2be2;">Mini-Project Portfolio</span></h1>
    <p>Each one explores a real-world AI ethics dilemma through code, reflection, or research. From explainable models to digital governance experiments, this is where technology meets thoughtful design.</p>
  </div>

  <div class="projects-grid">


    <!-- Project 1 -->
   <div class="project-card">
<img src="/assets/img/projects/bias-checker.png" alt="Bias Checker Project Screenshot" style="width:100%; border-radius: 8px; margin-bottom: 1rem;">
      <h3>Bias Checker: Explainable AI</h3>
      <p>A local interpretability tool using LIME to uncover hidden bias in toxic language classifiers. Includes identity-swapped templates and fairness analysis.</p>
  <button onclick="openModal('biasModal')"></button>
</div>

<!-- Modal for Bias Checker Project -->
<div id="biasModal" class="modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal('biasModal')">&times;</span>
    <h2 style="color:#6f1cb1; font-family:'Space Grotesk',sans-serif;">Bias Checker: Explainable AI</h2>

   <p><strong>What’s this project about?</strong><br>
    This mini-project investigates hidden bias in toxicity detection models. Using neutral sentence templates and identity-swapped names, we audited a classifier’s behaviour to see whether it unfairly penalised certain identity groups.</p>

   <p><strong>Why does it matters?</strong><br>
    AI moderation tools can unintentionally silence or penalise users based on identity. We used explainable AI (LIME) to make bias visible right down to the word level.</p>

   <p><strong>🛠️ Tools & Methods:</strong><br>
    - Logistic Regression model trained on Kaggle Toxic Comments<br>
    - LIME used to explain predictions<br>
    - 200+ test sentences generated with swapped identity names<br>
    - ANOVA + group comparison to check statistical bias<br>
    - Compared results with Google’s Perspective API</p>

  <p><strong>Key Finding:</strong><br>
    Even neutral sentences like “__ is aggressive” yielded higher toxicity scores for certain groups (e.g. Arabic, Black, Indian) compared to others (e.g. White).
Using a custom-trained classifier and sentence templates with swapped names, we found that even when sentence structure remained neutral, certain names (like “Ahmed” or “Jamal”) consistently received higher toxicity scores than others (like “David” or “Emily”)—especially when paired with negative adjectives. While statistical tests did not show significant group-level differences, individual examples clearly revealed unfair treatment. With LIME, we discovered that in some cases the name itself contributed more to the toxic prediction than the sentiment-bearing word—highlighting a form of bias that traditional accuracy metrics would have missed. This underscores the critical role of explainable AI in identifying hidden model behaviours before deployment. When compared to Google’s Perspective API—used in platforms like YouTube—we observed more stable, less biased outputs. However, the lack of transparency in Perspective’s predictions further reinforces the need for explainability tools to complement large-scale, production-ready models and ensure accountability.</p>

   <img src="/assets/img/Bias_Results.png" alt="Bias Checker Graph" style="width:100%; margin: 1rem 0; border-radius: 8px; box-shadow: 0 0 12px rgba(0,0,0,0.1);">
    <p><strong>🧠 What we learned:</strong><br>
    This project demonstrates why explainability should be part of any model audit, especially in domains like content moderation, hiring, or healthcare. Even seemingly fair models can behave unfairly in specific contexts.

Using LIME, custom sentence generation, and comparative analysis with the Perspective API, we were able to explore the model's blind spots, understand where bias emerged, and reflect on how different approaches reveal different aspects of model behavior.</p>

   <a href="https://github.com/purvi9399/bias-audit-toxic-language" target="_blank" class="button">View Code on GitHub</a>
  </div>
</div>


   <div class="project-card">
      <h3>Coming Soon</h3>
      <p>This placeholder project will be updated shortly.</p>
      <a href="#">Stay tuned</a>
    </div>

    <!-- Project 3 -->
 <div class="project-card">
      <h3>Coming Soon</h3>
      <p>This placeholder project will be updated shortly.</p>
      <a href="#">Stay tuned</a>
    </div>
  </div>
</div>

<!-- Scroll Reveal Animation Script -->
<script>
  document.addEventListener("DOMContentLoaded", function () {
    const cards = document.querySelectorAll(".project-card");

    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add("reveal");
        }
      });
    }, {
      threshold: 0.2
    });

    cards.forEach(card => {
      observer.observe(card);
    });
  });
</script>

