---
layout: default
title: Eastern Art
permalink: /tag/eastern-art/
---

<div class="c-page-hero">
  <div class="o-grid">
    <div class="o-grid__col">
      <div class="c-page-hero__content c-page-hero__content--no-image">
        <h1 class="c-page-hero__title">Eastern Art</h1>
      </div>
    </div>
  </div>
</div>

<div style="column-count: 3; column-gap: 20px; column-fill: auto; width: 95%; margin: 0 auto; padding: 20px 0;">
{% for post in site.posts %}
  {% if post.tags contains "Eastern Art" %}
    <div style="break-inside: avoid; margin-bottom: 20px; display: inline-block; width: 100%;">
      <article class="c-post-card" style="margin-bottom: 0;">
        <div class="c-post-card__media">
          <a class="c-post-card__image-link" href="{{ post.url | relative_url }}">
            <img class="c-post-card__image" src="{{ post.image | relative_url }}" alt="{{ post.title }}" style="width: 100%; height: auto;">
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