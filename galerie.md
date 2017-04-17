---
layout: page
title: Galerie
permalink: /galerie
---
<div class="gallery">
  {% for image in site.data.gallery %}
    <dl class="gallery-item">
      <a href="{{ site.baseurl}}/{{ image.url }}" class="gallery-icon" style="background-image: url('{{ site.baseurl}}/{{ image.url }}')"></a>
    </dl>
  {% endfor%}
</div>
