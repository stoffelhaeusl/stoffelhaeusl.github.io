---
title: Neuigkeiten
permalink: /neuigkeiten
layout: blog
---
<section class='page blog'>
  {% for post in site.posts %}
    <article>
      <header>
        <h1><a class='post-link' href='{{ post.url | prepend: site.baseurl }}'>{{ post.title }}</a></h1>
      </header>
        {% if post.content contains '<!--more-->' %}
          {{ post.content | split: '<!--more-->' | first }}
        {% else %}
          {{ post.excerpt }}
        {% endif %}
      <footer>
        <a href='{{ post.url | prepend: site.baseurl }}'>Weiterlesen … </a>
      </footer>
    </article>
  {% endfor %}
</section>
