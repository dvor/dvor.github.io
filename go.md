---
layout: default
permalink: /go/
---

<section class="section links-page">
  <h1 style="font-size:2rem;">{{ site.title }}</h1>
  <p class="tag">{{ site.description }}</p>
  
  {% include streaming-links.html style="links" %}
  
  <div class="more-info">
    <a href="{{ '/' | relative_url }}">More about artist</a>
  </div>
</section>