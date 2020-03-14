---
layout: default
title: blog
---

<h1> {{ page.title }} </h1>

<div>
{% for post in site.posts %}

  {% include style-post-list.html %}
{% endfor %}
</div>
