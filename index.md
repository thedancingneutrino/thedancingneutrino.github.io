---
layout: default
title: Home
---

<div class="landing">

  <p class="intro">
    The thoughts that pop into my head, now website version!
  </p>

  <div class="chapters">
    {% assign chapters = site.chapters | sort: "order" %}

    {% for chapter in chapters %}
      <a href="{{ chapter.url }}" class="chapter-card">
        
        <h2 class="chapter-title">
          <span class="chapter-number">
            {{ chapter.title | split: ":" | first }}:
          </span>
          <span class="chapter-name">
             {{ chapter.title | split: ":" | last }}
          </span>
        </h2>

        {% if chapter.summary %}
          <p class="chapter-desc">
            {{ chapter.summary }}
          </p>
        {% endif %}
      </a>
    {% endfor %}
  </div>

</div>
