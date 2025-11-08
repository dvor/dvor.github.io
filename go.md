---
layout: default
permalink: /go/
---

<section class="section links-page">
  <h1 style="font-size:2rem;">{{ site.title }}</h1>
  <p class="tag">{{ site.description }}</p>
  
  <!-- Primary mailing list CTA section -->
  <div class="mailing-list-hero" id="mailing-hero">
    <p class="mailing-hook">🎷 Be one of the first listeners</p>
    <h2 class="mailing-headline">Join my private list for unreleased ambient jazz fusion and early track drops.</h2>
    <div class="mailing-cta-primary">
      <a class="ml-onclick-form mailing-button" href="javascript:void(0)" onclick="ml('show', 'R2ISyG', true); if(typeof sa_event !== 'undefined') sa_event('mailing_list_signup_go');">
        Join the list
      </a>
    </div>
    <p class="mailing-disclaimer">No spam — just music, good vibes, and behind-the-scenes notes.</p>
  </div>
  
  {% include streaming-links.html style="links" %}
  
  <div class="more-info">
    <a href="{{ '/' | relative_url }}">More about artist</a>
  </div>
</section>

<!-- Sticky mobile CTA -->
<div class="sticky-cta" id="sticky-cta">
  <div class="sticky-cta-content">
    <span class="sticky-cta-text">🎧 Join the list</span>
    <a class="ml-onclick-form sticky-cta-button" href="javascript:void(0)" onclick="ml('show', 'R2ISyG', true); if(typeof sa_event !== 'undefined') sa_event('mailing_list_signup_go_sticky');">
      Join
    </a>
  </div>
</div>

<script>
// Sticky CTA functionality
document.addEventListener('DOMContentLoaded', function() {
  const hero = document.getElementById('mailing-hero');
  const stickyCta = document.getElementById('sticky-cta');
  
  if (!hero || !stickyCta) return;
  
  let hasScrolledPast = false;
  
  function toggleStickyCta() {
    const heroRect = hero.getBoundingClientRect();
    const scrolledPastHero = heroRect.bottom < 0;
    
    if (scrolledPastHero && !hasScrolledPast) {
      hasScrolledPast = true;
      stickyCta.classList.add('show');
    } else if (!scrolledPastHero && hasScrolledPast) {
      hasScrolledPast = false;
      stickyCta.classList.remove('show');
    }
  }
  
  // Check on scroll
  window.addEventListener('scroll', toggleStickyCta);
  
  // Check initially
  toggleStickyCta();
});
</script>