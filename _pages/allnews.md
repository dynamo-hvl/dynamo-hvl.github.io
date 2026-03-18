---
title: "Home"
layout: default
excerpt: "Orthotron"
sitemap: false
permalink: /allnews.html
---

# News
{% for article in site.data.news %}
<div style="margin-bottom: 15px;">
  <strong>{{ article.date }}</strong><br>
  <em>{{ article.headline }}</em><br>
  <em>{{ article.description }}</em><br>
  {% if article.image %}
  <img src="{{ article.image | relative_url }}" style="max-width: 400px;">
  {% endif %}
</div>
{% endfor %}