---
title: Projects
nav:
  order: 2
  tooltip: Software, datasets, and more
---

<div style="text-align:center;">

<h1><b>PROJECTS</b></h1>

</div>

<div class="project-list">
  {% assign projects = site.projects | sort: "order" %}
  {% for project in projects %}
    {% include project-card.html project=project %}
  {% endfor %}
</div>
