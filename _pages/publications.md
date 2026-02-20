---
title: "Publications"
layout: default
permalink: /publications/
---

# Publications

{% assign sorted_pubs = site.data.publications | sort: "year" | reverse %}

{% for pub in sorted_pubs %}
<p class="publication-entry">
  {{ pub.authors }}. ({{ pub.year }}). 
  <a href="{{ pub.url }}" target="_blank">
    {{ pub.title }}
  </a>. 
  {{ pub.journal }}.<br>
  {{ pub.type }}
</p>
{% endfor %}
