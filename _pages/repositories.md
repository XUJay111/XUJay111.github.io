---
layout: page
permalink: /repositories/
title: open source
description: public research repositories, datasets, and resources for embodied AI
nav: true
nav_order: 4
---

Public repositories for my research collaborations, alongside resources I maintain. Repository owners and release details are listed below. You can also browse my [GitHub profile](https://github.com/{{ site.data.socials.github_username }}).

{% for repository in site.data.repositories.github_repos %}
{% assign details = site.data.repositories.repository_details[repository] %}

<article class="card mb-4">
  <div class="card-body">
    <h2 class="card-title"><a href="https://github.com/{{ repository }}">{{ details.title | default: repository | escape }}</a></h2>
    <p><small>{{ repository | escape | replace: '/', '/<wbr>' }} · {{ details.relationship | escape }}</small></p>
    <p>{{ details.description | escape }}</p>
    <p><strong>Release:</strong> {{ details.release | escape }}</p>
    <p>
      <a href="https://github.com/{{ repository }}">GitHub repository</a>
      {% if details.project %} · <a href="{{ details.project | relative_url }}">Project overview</a>{% endif %}
      {% if details.paper_key %} · <a href="{{ '/publications/' | relative_url }}#{{ details.paper_key }}">Paper</a>{% endif %}
      {% if details.dataset %} · <a href="{{ details.dataset }}">Dataset</a>{% endif %}
    </p>
  </div>
</article>

{% endfor %}

{% if site.data.repositories.show_stats %}

## Repository statistics

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repository in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repository %}
  {% endfor %}
</div>
{% endif %}
