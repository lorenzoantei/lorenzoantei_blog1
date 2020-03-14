---
layout: default
title: projects
---

<h1> {{ page.title }} </h1>

Photos >> [live](/live/)

<div>
{% for post in site.projects %}

  {% include style-post-list.html %}
{% endfor %}
</div>
