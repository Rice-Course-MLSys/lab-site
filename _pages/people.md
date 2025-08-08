---
title: "People"
permalink: /people/
layout: single
author_profile: false
classes: wide
header:
  overlay_color: "#000"
  overlay_filter: "0.6"
  overlay_image: /assets/images/people-banner.webp
  caption: "Photo credit: OpenAI-Sora"
excerpt: "Meet the brilliant minds driving innovation in machine learning and systems research"

# Lab members organized by role
faculty:
  - name: "Dr. Yuke Wang"
    title: "Principal Investigator"
    image: "/assets/images/people/yuke-wang.jpg"
    research_interests: "Machine learning systems, distributed computing, AI optimization"
    website: "https://www.wang-yuke.com"
    email: "yuke.wang@rice.edu"
    linkedin: "#"

phd_students:
  - name: "Fanjiang Ye"
    title: "PhD Student"
    image: "/assets/images/people/fanjiang-ye.jpeg"
    research_interests: "Research interests to be updated..."
    website: "https://home.fanjiang.net"
    email: "fanjye@iu.edu"
    placeholder: true
  - name: "Kaijian Wang"
    title: "First Year PhD Student"
    image: "/assets/images/people/kaijian-wang.jpeg"
    research_interests: "Research interests to be updated..."
    website: "https://github.com/AlbedoWang"
    email: "Kaijian.Wang@rice.edu"
    placeholder: true
  - name: "Jingwei Zuo"
    title: "First Year PhD Student"
    image: "/assets/images/people/jingwei-zuo.jpg"
    research_interests: "Research interests to be updated..."
    website: "https://jingwei-zuo.com"
    email: "jz201@rice.edu"
    placeholder: true

master_students:
  - name: "Xinrui Zhong"
    title: "Master Student"
    image: "/assets/images/people/xinrui-zhong.jpg"
    research_interests: "Research interests to be updated..."
    website: "#"
    linkedin: "https://www.linkedin.com/in/xinrui-zhong-519b2a327"
    email: "xz118@rice.edu"
    placeholder: true

alumni:
#   - name: "Alumni Name"
#     title: "PhD Graduate (2024)"
#     current_position: "Research Scientist at Google"
#     image: "/assets/images/people/alumni-placeholder.jpg"
#     website: "#"

# Template for adding new members
# Copy this structure to add new people:
# new_member:
#   - name: "Full Name"
#     title: "Position/Title"
#     image: "/assets/images/people/firstname-lastname.jpg"
#     research_interests: "Detailed research interests..."
#     website: "https://personal-website.com"
#     email: "email@rice.edu"
#     linkedin: "https://linkedin.com/in/username"
#     twitter: "https://twitter.com/username"
#     google_scholar: "https://scholar.google.com/citations?user=..."

join_cta:
  title: "Join Our Team"
  description: "We are always looking for passionate researchers to join our team. If you're interested in machine learning and systems research, we'd love to hear from you!"
  buttons:
    # - label: "How to Join"
    #   url: "/join/"
    #   class: "btn--primary"
    #   icon: "fas fa-users"
    - label: "Contact Us"
      url: "mailto:yuke.wang@rice.edu"
      class: "btn--primary"
      icon: "fas fa-envelope"
---

## Faculty

<div class="people-grid">
    {% for person in page.faculty %}
    <div class="person-card">
      <div class="person-photo">
        <img src="{{ person.image | relative_url }}" alt="{{ person.name }}" class="person-image">
      </div>
      <div class="person-info">
        <h3 class="person-name">{{ person.name }}</h3>
        <p class="person-title">{{ person.title }}</p>
        <div class="person-research">
          <h4>Research Interests:</h4>
          <p>{{ person.research_interests }}</p>
        </div>
        <div class="person-links">
          {% if person.website and person.website != "#" %}
          <a href="{{ person.website }}" class="person-link" target="_blank">
            <i class="fas fa-home"></i> Website
          </a>
          {% endif %}
          {% if person.email %}
          <a href="mailto:{{ person.email }}" class="person-link">
            <i class="fas fa-envelope"></i> Email
          </a>
          {% endif %}
          {% if person.linkedin and person.linkedin != "#" %}
          <a href="{{ person.linkedin }}" class="person-link" target="_blank">
            <i class="fab fa-linkedin"></i> LinkedIn
          </a>
          {% endif %}
        </div>
      </div>
    </div>
    {% endfor %}
  </div>

## PhD Students

<div class="people-grid">
    {% for person in page.phd_students %}
    <div class="person-card">
      <div class="person-photo">
        <img src="{{ person.image | relative_url }}" alt="{{ person.name }}" class="person-image">
      </div>
      <div class="person-info">
        <h3 class="person-name">{{ person.name }}</h3>
        <p class="person-title">{{ person.title }}</p>
        <div class="person-research">
          <h4>Research Interests:</h4>
          <p class="{% if person.placeholder %}research-placeholder{% endif %}">
            {% if person.placeholder %}<em>{{ person.research_interests }}</em>{% else %}{{ person.research_interests }}{% endif %}
          </p>
        </div>
        <div class="person-links">
          {% if person.website and person.website != "#" %}
          <a href="{{ person.website }}" class="person-link" target="_blank">
            <i class="fas fa-home"></i> Website
          </a>
          {% else %}
          <a href="#" class="person-link disabled">
            <i class="fas fa-home"></i> Website (TBA)
          </a>
          {% endif %}
          {% if person.email %}
          <a href="mailto:{{ person.email }}" class="person-link">
            <i class="fas fa-envelope"></i> Email
          </a>
          {% endif %}
        </div>
      </div>
    </div>
    {% endfor %}
  </div>

## Master Students

<div class="people-grid">
    {% for person in page.master_students %}
    <div class="person-card">
      <div class="person-photo">
        <img src="{{ person.image | relative_url }}" alt="{{ person.name }}" class="person-image">
      </div>
      <div class="person-info">
        <h3 class="person-name">{{ person.name }}</h3>
        <p class="person-title">{{ person.title }}</p>
        <div class="person-research">
          <h4>Research Interests:</h4>
          <p class="{% if person.placeholder %}research-placeholder{% endif %}">
            {% if person.placeholder %}<em>{{ person.research_interests }}</em>{% else %}{{ person.research_interests }}{% endif %}
          </p>
        </div>
        <div class="person-links">
          {% if person.website and person.website != "#" %}
          <a href="{{ person.website }}" class="person-link" target="_blank">
            <i class="fas fa-home"></i> Website
          </a>
          {% else %}
          <a href="#" class="person-link disabled">
            <i class="fas fa-home"></i> Website (TBA)
          </a>
          {% endif %}
        </div>
      </div>
    </div>
    {% endfor %}
  </div>

  {% if page.alumni and page.alumni.size > 0 %}
## Alumni

<div class="people-grid alumni-grid">
    {% for person in page.alumni %}
    <div class="person-card alumni-card">
      <div class="person-photo">
        <img src="{{ person.image | relative_url }}" alt="{{ person.name }}" class="person-image">
      </div>
      <div class="person-info">
        <h3 class="person-name">{{ person.name }}</h3>
        <p class="person-title">{{ person.title }}</p>
        {% if person.current_position %}
        <p class="current-position">{{ person.current_position }}</p>
        {% endif %}
        <div class="person-links">
          {% if person.website and person.website != "#" %}
          <a href="{{ person.website }}" class="person-link" target="_blank">
            <i class="fas fa-home"></i> Website
          </a>
          {% endif %}
        </div>
      </div>
    </div>
    {% endfor %}
  </div>
{% endif %}

## {{ page.join_cta.title }}

<div class="join-section">
    <p>{{ page.join_cta.description }}</p>
    <div class="join-buttons">
      {% for button in page.join_cta.buttons %}
      <a href="{{ button.url }}" class="btn {{ button.class }} btn--large">
        <i class="{{ button.icon }}"></i> {{ button.label }}
      </a>
      {% endfor %}
    </div>
  </div>

<style>
.people-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(350px, 450px));
  gap: 2rem;
  margin: 2rem 0 4rem 0;
  justify-content: start;
}

.person-card {
  background: #fff;
  border: 1px solid #e0e0e0;
  border-radius: 12px;
  padding: 1.5rem;
  transition: all 0.3s ease;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  display: flex;
  flex-direction: column;
  height: 100%;
  min-height: 450px;
}

.person-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 25px rgba(0,0,0,0.15);
  border-color: #007bff;
}

.person-photo {
  text-align: center;
  margin-bottom: -2rem;
}

.person-image {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  object-fit: cover;
  border: 4px solid #f8f9fa;
  transition: border-color 0.3s ease;
}

.person-card:hover .person-image {
  border-color: #007bff;
}

.person-info {
  text-align: center;
  display: flex;
  flex-direction: column;
  flex-grow: 1;
}

.person-name {
  font-size: 1.4rem;
  font-weight: 600;
  color: #333;
  margin-bottom: 0.5rem;
}

.person-title {
  font-size: 1rem;
  color: #007bff;
  font-weight: 500;
  margin-bottom: 0em;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.current-position {
  font-size: 0.9rem;
  color: #28a745;
  font-weight: 500;
  margin-bottom: 0rem;
  font-style: italic;
}

.person-research {
  text-align: left;
  margin-bottom: 0rem;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
}

.person-research h4 {
  font-size: 1rem;
  color: #333;
  margin-bottom: 0.8rem;
  font-weight: 600;
}

.person-research p {
  font-size: 0.95rem;
  line-height: 1.5;
  color: #666;
  flex-grow: 1;
}

.research-placeholder {
  color: #999 !important;
}

.person-links {
  display: flex;
  justify-content: center;
  gap: 0.8rem;
  flex-wrap: wrap;
  margin-top: auto;
}

.person-link {
  display: inline-flex;
  align-items: center;
  gap: 0.4rem;
  padding: 0.5rem 0.8rem;
  background: #f8f9fa;
  color: #333;
  text-decoration: none;
  border-radius: 6px;
  font-size: 0.85rem;
  transition: all 0.3s ease;
  border: 1px solid #dee2e6;
}

.person-link:hover:not(.disabled) {
  background: #007bff;
  color: white;
  border-color: #007bff;
  transform: translateY(-2px);
}

.person-link.disabled {
  opacity: 0.5;
  cursor: not-allowed;
}

.alumni-grid .person-card {
  border-color: #6c757d;
}

.alumni-card:hover {
  border-color: #6c757d;
}

.alumni-card .person-image {
  border-color: #e9ecef;
}

.alumni-card:hover .person-image {
  border-color: #6c757d;
}

.join-section {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 3rem 2rem;
  border-radius: 12px;
  text-align: center;
  margin-top: 4rem;
}

.join-section p {
  font-size: 1.1rem;
  margin-bottom: 2rem;
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
}

.join-buttons {
  display: flex;
  gap: 1rem;
  justify-content: center;
  flex-wrap: wrap;
}

.join-buttons .btn {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .people-grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
  
  .person-card {
    padding: 1rem;
  }
  
  .person-image {
    width: 120px;
    height: 120px;
  }
  
  .person-name {
    font-size: 1.2rem;
  }
  
  .join-buttons {
    flex-direction: column;
    align-items: center;
  }
  
  .join-buttons .btn {
    width: 100%;
    max-width: 250px;
  }
}

@media (max-width: 480px) {  
  .person-links {
    flex-direction: column;
    align-items: center;
  }
  
  .person-link {
    width: 100%;
    max-width: 200px;
    justify-content: center;
  }
}
</style>