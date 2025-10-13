---
layout: default
title: Music
permalink: /music/
---

<h1>Releases</h1>

<div class="grid">
{% assign sorted_releases = site.music | sort: 'release_date' | reverse %}
{% for release in sorted_releases %}
  <div class="card">
    {% if release.cover %}
      <img src="{{ release.cover }}" alt="{{ release.title }} cover" style="width:100%;border-radius:10px;">
    {% endif %}
    <h3>
      {{ release.title }}
      {% if release.pre_release_label and release.release_date %}
        {% include date-compare.html date=release.release_date %}
        {% if is_future %}
          <span class="pre-release-label">{{ release.pre_release_label }}</span>
        {% endif %}
      {% endif %}
    </h3>
    {% if release.release_date %}
      {% include date-compare.html date=release.release_date %}
      <p style="color:var(--muted);font-size:0.9em;margin-top:-8px;">
        {{ formatted_date }}
      </p>
    {% endif %}
    {% if release.description %}
      <p>{{ release.description }}</p>
    {% endif %}
    {% if release.platforms %}
      <div class="icons" style="margin-top:8px;">
        {% include release-badges.html platforms=release.platforms %}
      </div>
    {% endif %}
  </div>
{% endfor %}
</div>

