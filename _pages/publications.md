---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}
{% if author.googlescholar %}
You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

## Sustainable AI and Resource-Efficient ML

{% for post in site.publications reversed %}
  {% if post.pubtype == 'ml' %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}


## Astrophysics and Cosmology

{% for post in site.publications reversed %}
  {% if post.pubtype == 'astro' %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
