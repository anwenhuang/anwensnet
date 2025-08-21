---
layout: page
title: Western Art
permalink: /tag/western-art/
---

<div class="c-archive">
  <h1 class="c-archive__title">Western Art</h1>
  <p class="c-archive__description">My Western Art covers a wide range of subjects and mediums - oil paintings, graphite drawings, colored pencil work, and more!</p>
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