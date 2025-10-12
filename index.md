---
layout: default
title: Home
---

<section class="section hero hero-grid">
  <div class="hero-photo">
    <img src="{{ '/assets/images/portrait.jpg' | relative_url }}" alt="Dmytro Vorobiov" class="portrait">
  </div>
  <div class="hero-text">
    <h1>{{ site.title }}</h1>
    <p class="tag">{{ site.description }}</p>
    <p class="bio">
      Dmytro Vorobiov is a progressive jazz fusion musician. His music blends atmospheric textures with complex harmonies and rhythmic structures.
      Currently releasing his debut album in a waterfall format.
    </p>
    {% include streaming-badges.html %}
  </div>
</section>


<section id="music" class="section">
  <h2>Music</h2>
  <p style="color:var(--muted);margin-top:-8px;margin-bottom:24px;">Selected releases — click any platform to listen.</p>
  <div class="grid">
  {% assign sorted_releases = site.music | sort: 'release_date' | reverse %}
  {% for release in sorted_releases %}
    <div class="card">
      {% if release.cover %}
        <img src="{{ release.cover }}" alt="{{ release.title }} cover" style="width:100%;border-radius:10px;">
      {% endif %}
      <h3>{{ release.title }}</h3>
      {% if release.release_date %}
        <p style="color:var(--muted);font-size:0.9em;margin-top:-8px;">
          {{ release.release_date | date: "%B %-d, %Y" }}
        </p>
      {% endif %}
      {% if release.description %}
        <p>{{ release.description }}</p>
      {% endif %}
      {% if release.platforms %}
        <div class="platform-icons" style="margin-top:8px;">
          {% include release-badges.html platforms=release.platforms %}
        </div>
      {% endif %}
    </div>
  {% endfor %}
  </div>
</section>




<section id="contact" class="section">
  <h2>Contact</h2>
  <p><a href="mailto:{{ site.email }}">{{ site.email }}</a></p>
  <div class="social-icons" style="margin-top:10px;">
  {% for s in site.social %}
    {% if s.name == 'tiktok' %}
      <a class="icon" href="{{ s.url }}" aria-label="TikTok">
        <img src="/assets/icons/tiktok.svg" alt="TikTok" style="height:24px;width:24px;">
        <span style="margin-left:6px;">TikTok</span>
      </a>
    {% elsif s.name == 'instagram' %}
      <a class="icon" href="{{ s.url }}" aria-label="Instagram">
        <img src="/assets/icons/instagram.svg" alt="Instagram" style="height:24px;width:24px;border-radius:6px;">
        <span style="margin-left:6px;">Instagram</span>
      </a>
    {% endif %}
  {% endfor %}
</div>
</section>
