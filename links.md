---
layout: default
title: Links
permalink: /links/
---

<section class="section hero" style="text-align:center;">
  <h1 style="font-size:2rem;">{{ site.title }}</h1>
  <p class="tag">{{ site.description }}</p>
  {% include streaming-badges.html %}
</section>

<section class="section" style="text-align:center;">
  <div class="icons" style="justify-content:center;margin-top:16px;">
    {% for s in site.social %}
      {% if s.name == 'tiktok' %}
        <a class="icon" href="{{ s.url }}" aria-label="TikTok">TikTok</a>
      {% elsif s.name == 'instagram' %}
        <a class="icon" href="{{ s.url }}" aria-label="Instagram">Instagram</a>
      {% endif %}
    {% endfor %}
  </div>
</section>
