---
layout: default
permalink: /go/
---

<section class="section links-page">
  <h1 style="font-size:2rem;">{{ site.title }}</h1>
  <p class="tag">{{ site.description }}</p>
  
  <!-- Mailing list signup button -->
  <div class="mailing-list-cta">
    <a class="ml-onclick-form cta-button" href="javascript:void(0)" onclick="ml('show', 'R2ISyG', true)">
      🎧 Get early access to new music
    </a>
  </div>
  
  {% include streaming-links.html style="links" %}
  
  <div class="more-info">
    <a href="{{ '/' | relative_url }}">More about artist</a>
  </div>
</section>