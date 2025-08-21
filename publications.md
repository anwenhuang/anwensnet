---
layout: page
title: Publications
permalink: /tag/publications/
---

<div class="o-grid js-grid" style="display: flex; flex-wrap: wrap; align-items: flex-start;">
{% for post in site.posts %}
  {% if post.tags contains "Publications" %}
    <div style="flex: 0 0 auto; width: 300px; margin: 20px; max-width: calc(50% - 40px);">
      <article class="c-post-card" style="margin-bottom: 0;">
        <div class="c-post-card__media">
          <a class="c-post-card__image-link" href="{{ post.url | relative_url }}">
            <img class="c-post-card__image" src="{{ post.image | relative_url }}" alt="{{ post.title }}" style="width: 100%; height: auto; object-fit: cover;">
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