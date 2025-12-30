---
title: "DYNAMO - Research"
layout: gridlay
excerpt: "DYNAMO — Research"
sitemap: false
permalink: /research/
---

# Research

We develop theory-driven and data-driven approaches for monitoring, control,
and diagnostics in engineering systems. Below is a selection of ongoing and
completed research projects.

{% for area in site.data.research %}

<div class="row" style="margin-bottom:30px">

<div class="col-sm-12">
  <h3>{{ area.project }}</h3>
</div>

<div class="col-sm-7">
  <p><b>Status:</b> {{ area.status }}</p>
  <p>{{ area.desc }}</p>
  {% if area.collaborators %}
  <p><b>Collaborators:</b> {{ area.collaborators | join: ", " }}</p>
  {% endif %}
</div>

<div class="col-sm-5">
  <img
  src="{{ '/images/' | append: area.photo | relative_url }}"
  class="img-responsive"
  style="max-width: 250px; width: 120%; border-radius:6px; box-shadow:2px 2px 6px #bbb;" />

</div>

</div>


<hr>

{% endfor %}
