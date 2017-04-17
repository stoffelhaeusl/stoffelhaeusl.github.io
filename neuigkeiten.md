---
title: Neuigkeiten
permalink: /neuigkeiten/
layout: default
---
{% for post in site.posts %}
  <article class="content">
    {% include post_header.html post=post %}
    {% if post.content contains '<!--more-->' %}
      {% assign content = post.content | split: '<!--more-->' | first%}
      {% include post_content.html content=content %}
      <footer>
        <a href='{{ post.url | prepend: site.baseurl }}'>Weiterlesen … </a>
      </footer>
    {% else %}
      {% include post_content.html content=post.content %}
    {% endif %}
  </article>
{% endfor %}
