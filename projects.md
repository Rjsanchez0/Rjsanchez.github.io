---
layout: page
title: "Projects"
permalink: /projects/
---

Below are my projects organized for quick review. Click any project to open its detail page.

{% assign sorted = site.projects | sort: "priority" %}
{% for project in sorted %}
<div class="project-card">
  <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
  <div class="project-meta">{{ project.category }} • {{ project.stack }}</div>
  <p>{{ project.summary }}</p>
  {% if project.tags %}
    {% for t in project.tags %}
      <span class="tag">{{ t }}</span>
    {% endfor %}
  {% endif %}
</div>
{% endfor %}
