---
title: Projects
icon: fas fa-code
order: 2
layout: default
---

<!-- Project Page Styles & Modal Logic -->
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
    color: #8a2be2;
  }

  .projects-header p {
    font-size: 1.1rem;
    color: #555;
    max-width: 750px;
    margin: 0 auto;
  }

  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(-20px); }
    to { opacity: 1; transform: translateY(0); }
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
    cursor: pointer;
    transition: all 0.3s ease-in-out;
  }

  .project-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 10px 18px rgba(0, 0, 0, 0.15);
  }

  .project-card h3 {
    font-size: 1.3rem;
    margin-top: 0.6rem;
    color: #111;
  }

  .modal {
    display: none;
   position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%); /* this centers the box */
  z-index: 1000;
  background: white;
  padding: 2rem;
  box-shadow: 0 0 20px rgba(0,0,0,0.3);
  border-radius: 10px;
  max-width: 600px;
  width: 90%;
  }

  .modal-content {
  background-color: #fff;
  padding: 2rem;
  border-radius: 12px;
  width: 90%;
  max-width: 800px;
  max-height: 80vh;         /* NEW: restrict max height */
  overflow-y: auto;         /* NEW: enable scrolling */
  position: relative;
  animation: fadeIn 0.4s ease-in-out;
}



  .close {
    color: #aaa;
    position: absolute;
    top: 12px;
    right: 20px;
    font-size: 1.8rem;
    cursor: pointer;
  }

  .close:hover {
    color: #000;
  }
</style>

<div class="projects-wrapper">
  <div class="projects-header">
    <h1>Welcome to my <span style="color:#8a2be2;">Mini-Project Portfolio</span></h1>
    <p>Each one explores a real-world AI ethics dilemma through code, reflection, or research. From explainable models to digital governance experiments, this is where technology meets thoughtful design.</p>
  </div>

  <div class="projects-grid">
    <!-- Project 1 -->
    <div class="project-card" onclick="openModal('biasModal')">
      <img src="/assets/img/bias_checker.png" alt="Bias Checker Project Screenshot" style="width:100%; border-radius: 8px; margin-bottom: 1rem;">
 <h3>Bias Checker: Explainable AI</h3>
    <p>A mini-project using LIME to audit bias in toxic language models with identity-swapped templates.</p>
    <a href="https://github.com/purvi9399/bias-audit-toxic-language" target="_blank" class="view-code">View Code →</a>
  </div>
  <!-- Project 2 Placeholder -->
    <div class="project-card">
      <h3>Coming Soon</h3>
    </div>
 <!-- Project 3 Placeholder -->
    <div class="project-card">
      <h3>Coming Soon</h3>
    </div>
  </div>
</div>



<!-- Modal Content -->
<div id="biasModal" class="modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal('biasModal')">&times;</span>
    <h2 style="color:#6f1cb1; font-family:'Space Grotesk',sans-serif;">Bias Checker: Explainable AI</h2>
    <p><strong>What’s this project about?</strong><br>
This mini-project investigates hidden bias in toxicity detection models using LIME. We used neutral sentence templates with different names to see if the model gave higher toxicity scores to some people than others, revealing any kind of racial or sexual biases in the model. </p>
    <p><strong>Why does it matter?</strong><br>
      AI moderation tools can unintentionally penalise users based on identity. We used explainability to uncover and visualise this problem.</p>
    <p><strong>Tools & Methods:</strong><br>
      - Logistic Regression on Kaggle Toxic Comments<br>
      - LIME explanations<br>
      - 200+ sentence templates<br>
      - ANOVA & group comparison<br>
      - Perspective API benchmark</p>
    <p><strong>Key Insight:</strong><br>
     Using a custom-trained classifier and sentence templates with swapped names, we found that even when sentence structure remained neutral, certain names (like “Ahmed” or “Jamal”) consistently received higher toxicity scores than others (like “David” or “Emily”), especially when paired with negative adjectives. 

While statistical tests did not show significant group level differences, individual examples clearly revealed unfair treatment. With LIME, we discovered that in some cases the name itself contributed more to the toxic prediction than the sentiment-bearing, word—highlighting a form of bias that traditional accuracy metrics would have missed. 

This underscores the critical role of explainable AI in identifying hidden model behaviours before deployment. When compared to Google’s Perspective API, used in platforms like YouTube comments, we observed more stable, less biased outputs. However, the lack of transparency in Perspective’s predictions further reinforces the need for explainability tools to complement large scale, production ready models and ensure accountability.</p>
    <img src="/assets/img/Bias_Results.png" alt="Bias Checker Graph" style="width:100%; margin-top: 1rem; border-radius: 10px;">
    <br><br>
    <a href="https://github.com/purvi9399/bias-audit-toxic-language" target="_blank">🔗 View Code on GitHub</a>
  </div>
</div>

<!-- Modal Toggle Script -->
<script>
  function openModal(id) {
    document.getElementById(id).style.display = 'block';
  }
  function closeModal(id) {
    document.getElementById(id).style.display = 'none';
  }
</script>
