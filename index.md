---
layout: default
title: Main
---

<section class ="landing">
  <p class="intro">
    The Dancing Neutrino.
    A collection of the things that pop through my mind.
    Everything is posted on Instagram and Tiktok (hopefully)
  </p>

  <div class="chapters">
    {% for chapter in site.chapters %}
      <div class="chapter-card">
        <h2>
          <a href="{{ chapter.url }}">{{ chapter.title }}</a>
        </h2>

        {% if chapter.description %}
          <p class="chapter-desc">{{ chapter.description }}</p>
        {% endif %}
      </div>
    {% endfor %}
  </div>


</section>
