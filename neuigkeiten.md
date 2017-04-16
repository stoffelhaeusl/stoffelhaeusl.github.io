---
title: Neuigkeiten
permalink: /neuigkeiten/
layout: default
---
{% for post in site.posts %}
  <article class="content">
    {% include post_header.html post=post %}
    {% if post.content contains '<!--more-->' %}
      <div class="article-content">
        {{ post.content | split: '<!--more-->' | first }}
      </div>
      <footer>
        <a href='{{ post.url | prepend: site.baseurl }}'>Weiterlesen … </a>
      </footer>
    {% else %}
      <div class="article-content">
        {{ post.content }}
      </div>
    {% endif %}
  </article>
{% endfor %}
