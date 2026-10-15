---
layout: default
title: Home
---

Hi, I'm **wequal**, an independent developer in San Jose, CA. This site collects my apps and open-source projects.

## Apps

<div class="app-grid">
{% for app in site.data.apps %}
  <div class="app-card">
    <h3><a href="{{ '/' | append: app.slug | append: '/' | relative_url }}">{{ app.name }}</a></h3>
    <p>{{ app.tagline }}</p>
    <p class="badges">
      {% for p in app.platforms %}<span class="badge">{{ p }}</span>{% endfor %}
    </p>
    <p class="links">
      <a href="{{ '/' | append: app.slug | append: '/' | relative_url }}">About</a> ·
      <a href="{{ '/' | append: app.slug | append: '/support/' | relative_url }}">Support</a> ·
      <a href="{{ '/' | append: app.slug | append: '/privacy/' | relative_url }}">Privacy</a> ·
      <a href="{{ app.repo }}">Source</a>
    </p>
  </div>
{% endfor %}
</div>

## All projects on GitHub

{% assign repos = site.github.public_repositories | where: "fork", false | sort: "pushed_at" | reverse %}
{% if repos and repos.size > 0 %}
<ul class="repo-list">
{% for repo in repos %}
  {% if repo.name == site.github.repository_name %}{% continue %}{% endif %}
  <li>
    <a href="{{ repo.html_url }}"><strong>{{ repo.name }}</strong></a>
    {% if repo.language %}<span class="badge">{{ repo.language }}</span>{% endif %}
    {% if repo.description %}<br><span class="repo-desc">{{ repo.description }}</span>{% endif %}
  </li>
{% endfor %}
</ul>
{% else %}
See all repositories at <a href="https://github.com/wequal?tab=repositories">github.com/wequal</a>.
{% endif %}

<p class="footnote">This list is generated automatically from my public GitHub repositories at build time.</p>
