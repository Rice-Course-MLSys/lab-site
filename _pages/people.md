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
excerpt: "Meet our dedicated team of researchers, students, and collaborators driving innovation in machine learning and systems research."

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
    image: "/assets/images/people/fanjiang-ye.png"
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

interns:
  - name: "Yi Mu"
    title: "Intern"
    image: "/assets/images/people/default.webp"
    research_interests: "Research interests to be updated..."
    website: "#"
    email: "#"
    placeholder: true
  - name: "Zepeng Zhao"
    title: "Intern"
    image: "/assets/images/people/default.webp"
    research_interests: "Research interests to be updated..."
    website: "#"
    email: "#"
    placeholder: true
  - name: "Xinze Feng"
    title: "Intern"
    image: "/assets/images/people/default.webp"
    research_interests: "Research interests to be updated..."
    website: "#"
    email: "#"
    placeholder: true
  - name: "Juncheng (Jack) Shen"
    title: "Intern"
    image: "/assets/images/people/default.webp"
    research_interests: "Research interests to be updated..."
    website: "#"
    email: "#"
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
    <div class="person-item">
      <div class="person-photo">
        <img src="{{ person.image | relative_url }}" alt="{{ person.name }}" class="person-image">
      </div>
      <div class="person-info">
        <h3 class="person-name">{{ person.name }}</h3>
        <p class="person-title">{{ person.title }}</p>
        <div class="person-links">
          {% if person.website and person.website != "#" %}
          <a href="{{ person.website }}" target="_blank">Website</a>
          {% endif %}
          {% if person.email %}
          <a href="mailto:{{ person.email }}">Email</a>
          {% endif %}
          {% if person.linkedin and person.linkedin != "#" %}
          <a href="{{ person.linkedin }}" target="_blank">LinkedIn</a>
          {% endif %}
        </div>
      </div>
    </div>
    {% endfor %}
  </div>

## PhD Students

<div class="people-grid">
    {% for person in page.phd_students %}
    <div class="person-item">
      <div class="person-photo">
        <img src="{{ person.image | relative_url }}" alt="{{ person.name }}" class="person-image">
      </div>
      <div class="person-info">
        <h3 class="person-name">{{ person.name }}</h3>
        <p class="person-title">{{ person.title }}</p>
        <div class="person-links">
          {% if person.website and person.website != "#" %}
          <a href="{{ person.website }}" target="_blank">Website</a>
          {% else %}
          <!-- <span class="disabled">Website (TBA)</span> -->
          {% endif %}
          {% if person.email %}
          <a href="mailto:{{ person.email }}">Email</a>
          {% endif %}
        </div>
      </div>
    </div>
    {% endfor %}
  </div>

## Master Students

<div class="people-grid">
    {% for person in page.master_students %}
    <div class="person-item">
      <div class="person-photo">
        <img src="{{ person.image | relative_url }}" alt="{{ person.name }}" class="person-image">
      </div>
      <div class="person-info">
        <h3 class="person-name">{{ person.name }}</h3>
        <p class="person-title">{{ person.title }}</p>
        <div class="person-links">
          {% if person.website and person.website != "#" %}
          <a href="{{ person.website }}" target="_blank">Website</a>
          {% else %}
          <!-- <span class="disabled">Website (TBA)</span> -->
          {% endif %}
          {% if person.email %}
          <a href="mailto:{{ person.email }}">Email</a>
          {% endif %}
        </div>
      </div>
    </div>
    {% endfor %}
  </div>

## Interns

<div class="people-grid">
    {% for person in page.interns %}
    <div class="person-item">
      <div class="person-photo">
        <img src="{{ person.image | relative_url }}" alt="{{ person.name }}" class="person-image">
      </div>
      <div class="person-info">
        <h3 class="person-name">{{ person.name }}</h3>
        <p class="person-title">{{ person.title }}</p>
        <div class="person-links">
          {% if person.website and person.website != "#" %}
          <a href="{{ person.website }}" target="_blank">Website</a>
          {% else %}
          <!-- <span class="disabled">Website (TBA)</span> -->
          {% endif %}
          {% if person.email and person.email != "#" %}
          <a href="mailto:{{ person.email }}">Email</a>
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
    <div class="person-item alumni-item">
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
          <a href="{{ person.website }}" target="_blank">Website</a>
          {% endif %}
        </div>
      </div>
    </div>
    {% endfor %}
  </div>
{% endif %}

<!-- ## {{ page.join_cta.title }} -->

<!-- <div class="join-section">
    <p>{{ page.join_cta.description }}</p>
    <div class="join-buttons">
      {% for button in page.join_cta.buttons %}
      <a href="{{ button.url }}" class="btn {{ button.class }} btn--large">
        <i class="{{ button.icon }}"></i> {{ button.label }}
      </a>
      {% endfor %}
    </div>
  </div> -->

<style>
.people-grid {
  display: flex;
  gap: 3rem;
  margin: 2rem 0 4rem 0;
  overflow-x: auto;
  padding-bottom: 1rem;
}

.person-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  min-width: 200px;
  flex-shrink: 0;
}

.person-photo {
  margin-bottom: 0.8rem;
}

.person-image {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  object-fit: cover;
  border: 2px solid #f0f0f0;
  transition: border-color 0.3s ease;
}

.person-image:hover {
  border-color: #007bff;
}

.person-info {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.person-name {
  font-size: 1rem;
  font-weight: 600;
  color: #333;
  margin-bottom: 0.2rem;
}

.person-title {
  font-size: 0.8rem;
  color: #666;
  font-weight: 400;
  margin-bottom: 0.8rem;
  text-transform: none;
  letter-spacing: normal;
}

.current-position {
  font-size: 0.75rem;
  color: #28a745;
  font-weight: 400;
  margin-bottom: 0.8rem;
  font-style: italic;
}

.person-links {
  display: flex;
  gap: 0.8rem;
  justify-content: center;
  flex-wrap: wrap;
}

.person-links a {
  color: #007bff;
  text-decoration: none;
  font-size: 0.8rem;
  transition: color 0.3s ease;
}

.person-links a:hover {
  color: #0056b3;
  text-decoration: underline;
}

.person-links .disabled {
  color: #999;
  font-size: 0.8rem;
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
    gap: 2rem;
  }
  
  .person-item {
    min-width: 150px;
  }
  
  .person-image {
    width: 80px;
    height: 80px;
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
  .people-grid {
    gap: 1.5rem;
  }
  
  .person-links {
    flex-direction: column;
    align-items: center;
    gap: 0.4rem;
  }
}
</style>