---
title: Neuigkeiten
permalink: /neuigkeiten/
layout: blog
---
<section class='page blog'>
  {% for post in site.posts %}
    <article>
      <header>
        <h1><a class='post-link' href='{{ post.url | prepend: site.baseurl }}'>{{ post.title }}</a></h1>
      </header>
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
</section>
