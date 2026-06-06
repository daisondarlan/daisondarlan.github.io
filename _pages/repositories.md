---
layout: page
permalink: /repositories/
title: repositories
description: Selected code, research tools, and experiments from my attempts to make intelligent systems behave a little more intelligently. Some are tied to publications, some are prototypes, and some are simply ideas I found worth testing.
nav: true
nav_order: 4
---

{% if site.data.repositories.github_repos %}

## Selected repositories

<div class="repositories">
  <div class="row row-cols-1 row-cols-md-2">
  {% for repo in site.data.repositories.github_repos %}
    <div class="col mb-4">
      <article class="card h-100 hoverable">
        <div class="card-body">
          <h3 class="card-title">
            <a href="{{ repo.url }}" target="_blank" rel="external nofollow noopener">{{ repo.name }}</a>
          </h3>
          <p class="card-text">{{ repo.description }}</p>
          <p class="post-meta">
            <a href="{{ repo.url }}" target="_blank" rel="external nofollow noopener">
              <i class="fa-brands fa-github fa-sm"></i> {{ repo.repository }}
            </a>
          </p>
          {% if repo.tags %}
          <p class="post-tags">
            {% for tag in repo.tags %}
              <span><i class="fa-solid fa-tag fa-sm"></i> {{ tag }}</span>{% unless forloop.last %}&nbsp;{% endunless %}
            {% endfor %}
          </p>
          {% endif %}
        </div>
      </article>
    </div>
  {% endfor %}
  </div>
</div>
{% endif %}
