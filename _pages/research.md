---
title: "DYNAMO - Research"
layout: gridlay
excerpt: "DYNAMO -- Research"
sitemap: false
permalink: /research/
---

# Research Areas 

We in DYNAMO have carried out extensive research on the control and modeling of industrial systems, with a strong emphasis on fault diagnosis, condition monitoring, and robust control strategies. Our work has resulted in multiple peer-reviewed publications covering advanced monitoring techniques, data-driven diagnostics, and control methods for large-scale mechanical and energy systems.

{% assign number_printed = 0 %}
{% for area in site.data.research %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/{{ area.photo }}" class="img-responsive" width="50%" style="float: left" />
  <h4>{{ area.project }}</h4>
  <i>{{ area.desc }}</i>

</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}