---
title: About Me
layout: page
icon: fas fa-stream
order: 1
---

<!-- Custom Styles -->
<style>
  :root {
    --ink: #111;
    --muted: #595959;
    --accent: #FFB6C1;
    --accent-2: #FFDAB9;
    --chip: #FFF0F5;
    --card: #fff;
    --ring: rgba(0,0,0,.08);
    --background-gradient: linear-gradient(to bottom, #FFE4E1 0%, #FFFFFF 100%);
  }

  .categories-wrap {
    max-width: 980px;
    margin: 0 auto;
    padding: 2.25rem 1.25rem 4rem;
    font-family: "Space Grotesk", system-ui, -apple-system, Segoe UI, Roboto, sans-serif;
    color: var(--ink);
    background: var(--background-gradient);
    border-radius: 16px;
  }

  .hero {
    margin-bottom: 1.75rem;
    padding: 1rem;
    border-radius: 12px;
    background: rgba(255,182,193,0.1);
    text-align: center;
  }
  .hero h1 {
    font-size: clamp(1.6rem, 1.1rem + 2vw, 2.25rem);
    color: var(--accent);
  }
  .hero p { color: var(--muted); margin-top: 0.5rem; }

  .filter-bar {
    display: flex;
    gap: 0.5rem;
    margin-bottom: 1.5rem;
    flex-wrap: wrap;
  }
  .filter-btn {
    padding: 0.5rem 1rem;
    border: 1px solid var(--accent);
    border-radius: 8px;
    background: var(--chip);
    cursor: pointer;
    color: var(--ink);
    transition: background 0.3s ease, transform 0.3s ease;
  }
  .filter-btn:hover {
    background: var(--accent);
    color: #fff;
    transform: scale(1.05);
  }
  .filter-btn.active { background: var(--accent); color: #fff; }

  .category-grid {
    display: grid;
    gap: 1rem;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  }
  .category-card {
    background: var(--card);
    border: 1px solid rgba(255,182,193,.1);
    border-radius: 12px;
    padding: 1rem;
    box-shadow: 0 4px 12px var(--ring);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  .category-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 20px rgba(255,182,193,.2);
  }
  .category-card h3 { color: var(--accent); font-weight: 700; margin-bottom: 0.5rem; }
  .category-card p { color: var(--muted); font-size: 0.95rem; }
  .category-card a { color: var(--accent); text-decoration: none; font-weight: 600; }
  .category-card a:hover { text-decoration: underline; }

  .random-btn {
    display: inline-block;
    padding: 0.55rem 1rem;
    border-radius: 10px;
    background: var(--accent);
    color: #fff;
    text-decoration: none;
    font-weight: 700;
    margin-top: 1.5rem;
    transition: transform 0.3s ease;
  }
  .random-btn:hover { transform: scale(1.05); }

  @media (max-width: 700px) {
    .category-grid { grid-template-columns: 1fr; }
  }
</style>

<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>

<div class="categories-wrap" role="main">
  <section class="hero" role="banner" aria-label="Categories Introduction">
    <h1>Explore My Ideas</h1>
    <p>Dive into topics that fuel my curiosity—from AI ethics to sustainable tech.</p>
  </section>

  <div class="filter-bar" role="navigation" aria-label="Category filters">
    <button class="filter-btn active" data-filter="all">All</button>
    <button class="filter-btn" data-filter="ai-ethics">AI Ethics</button>
    <button class="filter-btn" data-filter="philosophy">Philosophy</button>
    <button class="filter-btn" data-filter="e-waste">E-Waste</button>
    <button class="filter-btn" data-filter="podcasts">Podcasts</button>
  </div>

  <div class="category-grid" role="region" aria-label="Category cards">
    <div class="category-card" data-category="ai-ethics">
      <h3>AI Ethics</h3>
      <p>Exploring fairness, transparency, and responsibility in AI.</p>
      <a href="/categories/ai-ethics">See Posts →</a>
    </div>
    <div class="category-card" data-category="philosophy">
      <h3>Philosophy</h3>
      <p>Big questions about mind, morality, and technology.</p>
      <a href="/categories/philosophy">See Posts →</a>
    </div>
    <div class="category-card" data-category="e-waste">
      <h3>E-Waste</h3>
      <p>Advocating for sustainable tech through recycling.</p>
      <a href="/categories/e-waste">See Posts →</a>
    </div>
    <div class="category-card" data-category="podcasts">
      <h3>Podcasts</h3>
      <p>Conversations on AI, ethics, and learning.</p>
      <a href="/categories/podcasts">See Posts →</a>
    </div>
  </div>

  <a class="random-btn" href="#" onclick="randomPost()">Discover a Random Idea</a>
</div>

<script>
  document.querySelectorAll('.filter-btn').forEach(btn => {
    btn.addEventListener('click', () => {
      document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      const filter = btn.getAttribute('data-filter');
      document.querySelectorAll('.category-card').forEach(card => {
        card.style.display = filter === 'all' || card.getAttribute('data-category') === filter ? 'block' : 'none';
      });
    });
  });

  function randomPost() {
    const posts = [
      '/categories/ai-ethics',
      '/categories/philosophy',
      '/categories/e-waste',
      '/categories/podcasts'
    ];
    const random = posts[Math.floor(Math.random() * posts.length)];
    window.location.href = random;
  }

  gsap.registerPlugin(ScrollTrigger);
  gsap.utils.toArray('.category-card').forEach((card, i) => {
    gsap.from(card, {
      opacity: 0,
      y: 30,
      duration: 0.8,
      delay: i * 0.1,
      scrollTrigger: {
        trigger: card,
        start: 'top 80%',
        end: 'top 50%',
        toggleActions: 'play none none none'
      }
    });
  });
</script>
