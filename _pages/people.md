---
title: "DYNAMO - People"
layout: gridlay
excerpt: "DYNAMO: People"
sitemap: false
permalink: /people/
---

# Team


## Lab Director
{% for member in site.data.team_members %}
<div class="row">
<div class="col-sm-6 clearfix">
<img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" class="img-responsive" width="40%" style="float:left; margin-right:10px" />
<h4>{{ member.name }}</h4>
<i>{{ member.role }}</i><br>
{{ member.info }}<br>
email: <{{ member.email }}><br>
<a href="{{ member.website }}" target="_blank">Website</a>
</div>
</div>
{% endfor %}


## Collaborators
{% assign count = 0 %}
{% for member in site.data.collaborators %}
{% if count == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
<img
  src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}"
  class="profile-photo"
  style="float:left; margin-right:10px"
/>
<h4>{{ member.name }}</h4>
<i>{{ member.affiliation }}</i><br>
<strong>Research Area:</strong> {{ member.research }}<br>
<a href="{{ member.website }}" target="_blank">Website</a>
</div>

{% assign count = count | plus: 1 %}
{% if count == 2 %}
</div>
{% assign count = 0 %}
{% endif %}
{% endfor %}
{% if count == 1 %}
</div>
{% endif %}


## Graduate Students
{% assign count = 0 %}
{% for member in site.data.students %}
{% if count == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
<img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" class="img-responsive" width="30%" style="float:left; margin-right:10px" />
<h4>{{ member.name }}</h4>
<i>{{ member.level }}</i><br>
<strong>Topic:</strong>: {{ member.topic }}<br>
Started: {{ member.start }}<br>
email: <{{ member.email }}>
</div>

{% assign count = count | plus: 1 %}
{% if count == 2 %}
</div>
{% assign count = 0 %}
{% endif %}
{% endfor %}
{% if count == 1 %}
</div>
{% endif %}


## Alumni
{% assign count = 0 %}
{% for member in site.data.alumni %}

{% if count == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" class="img-responsive" width="30%" style="float:left; margin-right:10px" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.degree}}</i><br>
  <strong>Current Position:</strong> {{ member.current_position }}
</div>

{% assign count = count | plus: 1 %}
{% if count == 2 %}
</div>
{% assign count = 0 %}
{% endif %}

{% endfor %}
{% if count == 1 %}
</div>
{% endif %}
