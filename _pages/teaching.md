---
layout: archive
title: "Teaching & Supervision"
permalink: /teaching/
author_profile: true
---

{% assign sections = "teaching:Teaching,supervision:Supervision" | split: "," %}
{% for s in sections %}
{% assign parts = s | split: ":" %}
{% assign key = parts[0] %}
<h2 class="teach-heading">{{ parts[1] }}</h2>
<ol class="teach-list">
  {% for item in site.data.teaching[key] %}
  <li class="teach-item">
    <span class="teach-year">{{ item.year }}</span>
    <div class="teach-body">
      <div class="teach-title">{{ item.title }}</div>
      <div class="teach-meta"><span class="teach-role">{{ item.role }}</span> · {{ item.details }}</div>
    </div>
  </li>
  {% endfor %}
</ol>
{% endfor %}
