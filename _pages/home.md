---
layout: home
permalink: /home/
author_profile: true
redirect_from:
    - /home/
    - /home.html
header:
  overlay_color: "#000"
  overlay_filter: "0.6"
  overlay_image: /assets/images/banner.webp
  actions:
    - label: "Learn More"
      url: "/research/"
  caption: "Photo credit: OpenAI-Sora"
excerpt: "Welcome to Yuke's Lab at Rice University - Advancing Machine Learning and Systems Research"
intro: 
  - excerpt: "At Yuke's Lab, we are at the forefront of machine learning and systems research, pushing the boundaries of what's possible in AI and computational systems. Our interdisciplinary team works on cutting-edge projects that equip artificial intelligence with efficient system design and secure deployment."
feature_row:
  - image_path: /assets/images/efficient.webp
    alt: "Efficient"
    title: "Efficient"
    excerpt: "We explore advanced techniques for optimizing machine learning models, focusing on reducing computational costs and improving performance."
    url: "/publications/"
    btn_label: "Read More"
    btn_class: "btn--primary"

  - image_path: /assets/images/scalable.webp
    alt: "Scalable"
    title: "Scalable"
    excerpt: "We develop scalable machine learning systems that can handle large datasets and complex models, ensuring robust performance in real-world applications."
    url: "/publications/"
    btn_label: "Read More"
    btn_class: "btn--primary"

  - image_path: /assets/images/secure.webp
    alt: "Secure"
    title: "Secure"
    excerpt: "We focus on building secure machine learning algorithms and systems that protect user data and ensure trustworthiness in AI applications."
    url: "/publications/"
    btn_label: "Read More"
    btn_class: "btn--primary"
# feature_row2:
#   - image_path: /assets/images/team-photo.jpg
#     alt: "Our Team"
#     title: "Join Our Team"
#     excerpt: 'We are always looking for passionate researchers, graduate students, and collaborators. Join us in pushing the boundaries of ML and systems research.'
#     url: "/join/"
#     btn_label: "Learn How to Join"
#     btn_class: "btn--primary"
# feature_row3:
#   - image_path: /assets/images/publications.jpg
#     alt: "Publications"
#     title: "Latest Publications"
#     excerpt: 'Discover our latest research contributions published in top-tier conferences and journals.'
#     url: "/publications/"
#     btn_label: "View Publications"
#     btn_class: "btn--primary"
#   - image_path: /assets/images/news.jpg
#     alt: "News & Updates"
#     title: "News & Updates"
#     excerpt: 'Stay updated with the latest news, announcements, and achievements from our lab.'
#     url: "/news/"
#     btn_label: "Read News"
#     btn_class: "btn--primary"
---

{% include feature_row id="intro" type="center" %}

## Research Areas

{% include feature_row %}

<!-- ## Recent Highlights

<div class="highlights-grid">
  <div class="highlight-card">
    <h3>🏆 Best Paper Award</h3>
    <p>Our paper on "Efficient Large-Scale ML Training" won the best paper award at MLSys 2025.</p>
    <a href="/news/best-paper-2025/" class="btn btn--primary">Read More</a>
  </div>
  
  <div class="highlight-card">
    <h3>🚀 New Funding</h3>
    <p>We received a $2M NSF grant to advance our research in distributed machine learning systems.</p>
    <a href="/news/nsf-grant-2025/" class="btn btn--primary">Learn More</a>
  </div>
  
  <div class="highlight-card">
    <h3>🎓 Student Success</h3>
    <p>Congratulations to our PhD students who recently graduated and joined top tech companies and universities.</p>
    <a href="/news/graduations-2025/" class="btn btn--primary">Celebrate</a>
  </div>
</div> -->

{% include feature_row id="feature_row2" type="left" %}

{% include feature_row id="feature_row3" %}

<!-- ## Lab Statistics

<div class="stats-container">
  <div class="stat-item">
    <div class="stat-number">50+</div>
    <div class="stat-label">Publications</div>
  </div>
  <div class="stat-item">
    <div class="stat-number">15</div>
    <div class="stat-label">PhD Students</div>
  </div>
  <div class="stat-item">
    <div class="stat-number">8</div>
    <div class="stat-label">Faculty</div>
  </div>
  <div class="stat-item">
    <div class="stat-number">25+</div>
    <div class="stat-label">Industry Partners</div>
  </div>
</div> -->

## Get Involved

Whether you're a prospective student, researcher, or industry partner, we welcome collaboration and engagement with our work.

<div class="cta-buttons">
  <a href="{{"/publications/" | relative_url }}" class="btn btn--large btn--secondary">Explore Research</a>
  <a href="{{"/people/" | relative_url }}" class="btn btn--large btn--success">Contact Us</a>
</div>

<style>
.highlights-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin: 3rem 0;
}

.highlight-card {
  background: #f8f9fa;
  padding: 2rem;
  border-radius: 12px;
  border: 1px solid #dee2e6;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.highlight-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0,0,0,0.1);
}

.highlight-card h3 {
  color: #333;
  margin-bottom: 1rem;
  font-size: 1.3rem;
}

.highlight-card p {
  color: #666;
  line-height: 1.6;
  margin-bottom: 1.5rem;
}

.stats-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 2rem;
  margin: 3rem 0;
  text-align: center;
}

.stat-item {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 2.5rem 1.5rem;
  border-radius: 12px;
  transition: transform 0.3s ease;
}

.stat-item:hover {
  transform: scale(1.05);
}

.stat-number {
  font-size: 3rem;
  font-weight: bold;
  margin-bottom: 0.5rem;
}

.stat-label {
  font-size: 1.1rem;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.cta-buttons {
  display: flex;
  gap: 1rem;
  justify-content: center;
  flex-wrap: wrap;
  margin: 3rem 0;
}

@media (max-width: 768px) {
  .highlights-grid {
    grid-template-columns: 1fr;
  }
  
  .stats-container {
    grid-template-columns: repeat(2, 1fr);
  }
  
  .stat-number {
    font-size: 2.5rem;
  }
  
  .cta-buttons {
    flex-direction: column;
    align-items: center;
  }
  
  .cta-buttons .btn {
    width: 100%;
    max-width: 300px;
  }
}
</style>