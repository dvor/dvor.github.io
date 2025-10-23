---
layout: default
description: "Electronic Press Kit for ambient jazz fusion composer Dmytro Vorobiov. Bio, album info, press photos, streaming links, and contact."
permalink: /epk/
---

<section class="epk-page">
  <!-- Header -->
  <header class="epk-header">
    <h1>Electronic Press Kit — Dmytro Vorobiov — Wandering Spaces</h1>
    
    <div class="epk-meta">
      <p><strong>Genre:</strong> Ambient Jazz Fusion</p> 
      <p><strong>Streaming release:</strong> Nov 21, 2025</p>
      <p><strong>Location:</strong> Amsterdam, Netherlands</p>
      
      <div class="epk-quick-links">
        {% assign bandcamp = site.streaming | where: 'name', 'bandcamp' | first %}
        {% assign spotify = site.streaming | where: 'name', 'spotify' | first %}
        <p><strong>Listen now:</strong> 
          <a href="{{ bandcamp.url }}" target="_blank">Bandcamp (full album)</a> • 
          <a href="{{ spotify.url }}" target="_blank">Spotify</a>
        </p>
        <p><strong>Press photos (ZIP):</strong> <a href="/download/press-photos.zip" target="_blank">Download</a></p>
        <p class="epk-last-updated"><strong>Last updated:</strong> October 24, 2025</p>
      </div>
    </div>
  </header>

  <!-- One-line hook -->
  <section class="epk-hook">
    <h2>Ambient jazz fusion built around space, improvisation, and long-form structure.</h2>
  </section>

  <!-- Artist Bio with Photo -->
  <section class="epk-section">
    <h3>Short bio</h3>
    
    <div class="epk-bio-grid">
      <div class="epk-bio-photo">
        <img src="{{ '/assets/images/portrait.jpg' | relative_url }}" alt="Dmytro Vorobiov" class="epk-portrait">
      </div>
      <div class="epk-bio-text">
        <p>
          Dmytro Vorobiov is a composer and multi-instrumentalist exploring the space between ambient soundscapes and jazz improvisation. His work draws on the energy and openness of Miles Davis' electric period, reframed through a modern, forward-looking lens. Working solo, he performs and records all instruments himself, building layered pieces that emphasize structure, texture, and emotional movement. Wandering Spaces is his debut full-length — a continuous journey that favors extended forms over song-by-song singles, and invites listeners into a patient, immersive sound world.
        </p>
      </div>
    </div>
  </section>

  <!-- About the Album & Listen -->
  <section class="epk-section">
    <h3>About the album — Wandering Spaces</h3>
    
    <p>
      Wandering Spaces channels the spirit of electric-era jazz — space, extended forms, improvisation — and translates it into a contemporary ambient context. Instead of discrete tracks, the record unfolds as a single arc with gradual shifts, layered textures, and evolving harmonic landscapes.
    </p>
    
    <div class="epk-listen-links">
      {% assign bandcamp = site.streaming | where: 'name', 'bandcamp' | first %}
      {% assign spotify = site.streaming | where: 'name', 'spotify' | first %}
      <p><strong>Listen now:</strong> 
        <a href="{{ bandcamp.url }}" target="_blank">Bandcamp (full album)</a> • 
        <a href="{{ spotify.url }}" target="_blank">Spotify</a>
      </p>
    </div>
    
    <div class="epk-focus-tracks">
      <h4>Focus tracks / starting points</h4>
      <ul>
        <li><strong>This & That</strong></li>
        <li><strong>For What Happens After</strong></li>
      </ul>
    </div>
    
    <div class="epk-player">
      <iframe style="border: 0; width: 100%; height: 406px;" src="https://bandcamp.com/EmbeddedPlayer/album=3291845933/size=large/bgcol=333333/linkcol=0f91ff/artwork=small/transparent=true/" seamless>
        <a href="https://dmytrovorobiov.bandcamp.com/album/wandering-spaces">Wandering Spaces by Dmytro Vorobiov</a>
      </iframe>
    </div>
    
    <div class="epk-credits-inline">
      <h4>Credits</h4>
      <p>Written, performed, produced, and mixed by Dmytro Vorobiov<br>
      Release date: Nov 21, 2025 • Label: Independent • Format: Digital / Bandcamp / Streaming</p>
    </div>
  </section>

  <!-- Contact & Links -->
  <section class="epk-section">
    <h3>Contact & links</h3>
    
    <div class="epk-contact-simple">
      {% assign tiktok = site.social | where: 'name', 'tiktok' | first %}
      {% assign instagram = site.social | where: 'name', 'instagram' | first %}
      <p><strong>Email:</strong> <a href="mailto:{{ site.email }}">{{ site.email }}</a></p>
      <p><strong>Instagram:</strong> <a href="{{ instagram.url }}" target="_blank">{{ instagram.url }}</a></p>
      <p><strong>TikTok:</strong> <a href="{{ tiktok.url }}" target="_blank">{{ tiktok.url }}</a></p>
      <p><strong>Website:</strong> <a href="{{ '/' | relative_url }}">{{ site.url }}</a></p>
    </div>
  </section>
</section>