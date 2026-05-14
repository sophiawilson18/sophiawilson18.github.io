---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

{% include base_path %}

<div class="project-grid">
{% assign sorted_projects = site.projects | sort: "order" %}
{% for project in sorted_projects %}
<a class="project-card" href="{{ project.url }}">
  <div class="project-card__body">
    <div class="project-card__title">{{ project.title }}</div>
    <div class="project-card__description">{{ project.description }}</div>
    {% if project.tags %}
    <div class="project-card__tags">
      {% for tag in project.tags %}
      <span class="project-card__tag">{{ tag }}</span>
      {% endfor %}
    </div>
    {% endif %}
  </div>
</a>
{% endfor %}
</div>
