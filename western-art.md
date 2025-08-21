---
layout: page
title: Western Art
permalink: /tag/western-art/
---

<div style="text-align: center; margin-bottom: 48px;">
  <h1 style="font-size: 32px; margin-bottom: 0;">Western Art</h1>
</div>

<div class="o-grid js-grid">
{% for post in site.posts %}
  {% if post.tags contains "Western Art" %}
    <div class="o-grid__col o-grid__col--1-4-l o-grid__col--1-2-m">
      <article class="c-post-card">
        <div class="c-post-card__media">
          <a class="c-post-card__image-link" href="{{ post.url | relative_url }}">
            <img class="c-post-card__image" src="{{ post.image | relative_url }}" alt="{{ post.title }}">
          </a>
        </div>
        <div class="c-post-card__content">
          <h2 class="c-post-card__title">
            <a class="c-post-card__title-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </h2>
          <div class="c-post-card__meta">
            <time class="c-post-card__date" datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
          </div>
        </div>
      </article>
    </div>
  {% endif %}
{% endfor %}
</div>