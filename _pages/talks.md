---
layout: archive
title: "Talks & Panels"
permalink: /talks/
author_profile: true
---

{% assign sections = "academia:Academia,industry:Industry & Professional,public:Public & Outreach,media:Media" | split: "," %}
{% for s in sections %}
{% assign parts = s | split: ":" %}
{% assign key = parts[0] %}
<h2>{{ parts[1] }}</h2>
<ol class="teach-list">
  {% for item in site.data.talks[key] %}
  <li class="teach-item">
    <span class="teach-year">{{ item.date }}</span>
    <div class="teach-body">
      <div class="teach-title">{% if item.url %}<a href="{{ item.url }}">{{ item.title }}</a>{% else %}{{ item.title }}{% endif %}</div>
      <div class="teach-meta"><span class="teach-role">{{ item.kind }}</span> · {{ item.event }}</div>
    </div>
  </li>
  {% endfor %}
</ol>
{% endfor %}
