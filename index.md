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
      <div class="chapter-card">
        <h2>
          <a href="{{ chapter.url }}">
            {{ chapter.title }}
          </a>
        </h2>

        {% if chapter.description %}
          <p class="chapter-desc">
            {{ chapter.summary }}
          </p>
        {% endif %}
      </div>
    {% endfor %}
  </div>

</div>
