---
layout: blog
title: blog
---

{% for post in site.posts %}
<h2><a href="{{ site.baseurl }}{{ post.url }}">
    {{ post.title }}
  </a></h2>
  <p>{{ post.summary }}</p>
    <time class="date" datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %-d, %Y" }}</time>
{% endfor %}
