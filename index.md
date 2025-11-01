---
layout: default
---

<section class="section hero hero-grid">
  <div class="hero-photo">
    <img src="{{ '/assets/images/portrait.jpg' | relative_url }}" alt="Dmytro Vorobiov" class="portrait">
  </div>
  <div class="hero-text">
    <h1>{{ site.title }}</h1>
    <p class="tag">{{ site.description }}</p>
    <p class="bio">
      Dmytro is an Amsterdam-based multi-instrumentalist sculpting immersive soundscapes at the crossroads of jazz, ambient fusion, and rock. On Wandering Spaces, his latest album, he explores not just notes—but the silence between them—drawing inspiration from Miles Davis’ electric period and filtering it through a forward-leaning, progressive lens.
    </p>
    {% include streaming-links.html style="badges" %}
  </div>
</section>

<!-- Mailing list CTA -->
<section class="section mailing-cta-section">
  <div class="mailing-list-hero">
    <p class="mailing-hook">Be part of the inner circle 💌</p>
    <h2 class="mailing-headline">🎧 Join my list and get unreleased tracks + early access to new music.</h2>
    <div class="mailing-cta-primary">
      <a class="ml-onclick-form mailing-button" href="javascript:void(0)" onclick="ml('show', 'R2ISyG', true); if(typeof sa_event !== 'undefined') sa_event('mailing_list_signup_home');">
        Join the list
      </a>
    </div>
    <p class="mailing-disclaimer">No spam. Just music and good vibes.</p>
  </div>
</section>

<section id="music" class="section">
  <h2>Music</h2>
  <p class="music-intro">Selected releases — click any platform to listen.</p>
  <div class="grid">
    {% assign sorted_releases = site.music | sort: 'release_date' | reverse %}
    {% for release in sorted_releases %}
      <div class="card">
        <div class="cover-wrapper">
          {% if release.cover %}
            <img src="{{ release.cover }}" alt="{{ release.title }} cover">
            {% if release.pre_release_label and release.release_date %}
              {% include date-compare.html date=release.release_date %}
              {% if is_future %}
                <div class="pre-release-ribbon">{{ release.pre_release_label }}</div>
              {% endif %}
            {% endif %}
          {% endif %}
        </div>
        <h3>
          {{ release.title }}
        </h3>
        {% if release.release_date %}
          {% include date-compare.html date=release.release_date %}
          <p style="color:var(--muted);font-size:0.9em;margin-top:-8px;">
            {{ formatted_date }}
          </p>
        {% endif %}
        {% if release.pre_release_note and release.release_date %}
          {% include date-compare.html date=release.release_date %}
          {% if is_future %}
            <p class="pre-release-note">{{ release.pre_release_note }}</p>
          {% endif %}
        {% endif %}
        {% if release.description %}
          <p>{{ release.description }}</p>
        {% endif %}
        {% if release.platforms %}
          <div class="platform-icons">
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
  <div class="social-icons">
    {% for s in site.social %}
      {% if s.name == 'tiktok' %}
        <a class="icon" href="{{ s.url }}" aria-label="TikTok">
          <img src="/assets/icons/tiktok.svg" alt="TikTok">
          <span>TikTok</span>
        </a>
      {% elsif s.name == 'instagram' %}
        <a class="icon" href="{{ s.url }}" aria-label="Instagram">
          <img src="/assets/icons/instagram.svg" alt="Instagram" class="instagram-icon">
          <span>Instagram</span>
        </a>
      {% endif %}
    {% endfor %}
  </div>
</section>
