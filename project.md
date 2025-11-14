---
layout: default
title: "Projects"
permalink: /projects/
---

<section class="section projects">
  <div class="container">
    <h1 class="section-title">Projects</h1>
    <p class="section-subtitle">A collection of my main works and experiments.</p>

    {% for group in site.data.projects %}
      <h2 class="project-category">{{ group.category }}</h2>
      <div class="timeline">
        {% for project in group.projects %}
          <div class="timeline-item">
            <div class="timeline-icon"><i class="fa-solid {{ project.icon }}"></i></div>
            <div class="timeline-content">
              <h3>{{ project.name }}</h3>
              <span class="timeline-date">{{ project.year }}</span>
              <p>{{ project.desc }}</p>
              {% if project.img %}
                <img src="{{ project.img }}" alt="{{ project.name }}" style="width:100%;max-width:500px;border-radius:10px;margin:10px 0;">
              {% endif %}
              {% if project.link %}
                <a href="{{ project.link }}" class="btn" target="_blank">View project</a>
              {% endif %}
            </div>
          </div>
        {% endfor %}
      </div>
    {% endfor %}
  </div>
</section>
