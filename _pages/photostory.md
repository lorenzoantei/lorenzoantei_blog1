---
layout: default
title: Photostory
---

<div>

{% for post in site.tags.photostory %}

  {% assign currentdate = post.date | date: "%Y" %}
  {% if currentdate != date %}
    {% unless forloop.first %}{% endunless %}
      <br><br><br>
      <div id="y{{post.date | date: "%Y"}}" style="text-align: center">
        {{ currentdate }}

      </div>
<br>
      {% assign date = currentdate %}
    {% endif %}

  <article role="article">
      <div style="text-align: center">
      <a href="{{ site.baseurl }}{{ post.url }}">

            {{ post.title }}
<br>


        <time class="date" datetime="{{ post.date | date_to_xmlschema }}"> {{ post.date | date: "%F" }} </time>
      </a>
      <br><br>
      </div>

  </article>

  {% if forloop.last %}{% endif %}
{% endfor %}
</div>
