---
layout: archive
title: "Publications of Sophia N. Wilson"
permalink: /publications/
author_profile: true
---

{% include base_path %}
{% if author.googlescholar %}
You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

## Sustainable / Resource-Efficient Machine Learning

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
