---
title: Members
nav:
  order: 1
  tooltip: About our lab members
---

<div style="text-align:center;">

<h1><b>MEMBERS</b></h1>

</div>


<h2>Professor</h2>
<div class="member-section">
  {% for member in site.members %}
    {% if member.role == 'principal-investigator' %}
      <div class="professor-card">
        <a
          {% if page.slug != member.slug %}
            href="{{ member.url | relative_url | uri_escape }}"
          {% endif %}
          class="professor-card-link"
          aria-label="{{ member.name | default: "professor link" | regex_strip }}"
        >
          <div class="professor-photo">
            <img
              src="{{ member.image | relative_url | uri_escape }}"
              alt="professor photo"
              loading="lazy"
              {% include fallback.html %}
            >
          </div>
          <div class="professor-info">
            <div class="professor-name">{{ member.name }}</div>
            <div class="professor-title">Principal Investigator</div>
            <div class="professor-bio">
              {{ member.content | markdownify }}
            </div>
          </div>
        </a>
      </div>
    {% endif %}
  {% endfor %}
</div>

<h2>Master</h2>
<div class="member-section">
  {% assign masters = site.members | where: "role", "master" | sort: "order" %}
  <div class="master-row">
    {% for member in masters %}
      {% if forloop.index0 == 3 %}
        </div><div class="master-row">
      {% endif %}
      {% include portrait.html member=member %}
    {% endfor %}
  </div>
</div>

<h2>Undergraduate</h2>
<div class="member-section">
  {% assign undergrads = site.members | where: "role", "undergrad" | sort: "order" %}
  {% for member in undergrads %}
    {% include portrait.html member=member %}
  {% endfor %}
</div>

<h2>Alumni</h2>
<div class="member-section">
  {% include list.html data="members" component="portrait" filter="role == 'alumni'" %}
</div>
