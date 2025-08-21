---
layout: page
title: Publications
permalink: /tag/publications/
---

<div style="column-count: 3; column-gap: 20px; column-fill: auto; width: 100%; max-width: 1200px; margin: 0 auto; padding: 0 20px; box-sizing: border-box;">
{% for post in site.posts %}
  {% if post.tags contains "Publications" %}
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