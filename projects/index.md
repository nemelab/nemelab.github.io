---
title: Projects
nav:
  order: 2
  tooltip: Our LAB's projects
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
