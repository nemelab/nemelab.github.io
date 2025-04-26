---
title: Members
nav:
  order: 1
  tooltip: About our lab members
---

# {% include icon.html icon="fa-solid fa-users" %}Members

NEME LAB's members

{% include section.html %}

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

{% include section.html background="images/background.jpg" dark=true %}

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

{% include section.html %}

{% capture content %}

{% include figure.html image="images/photo.jpg" %}
{% include figure.html image="images/photo.jpg" %}
{% include figure.html image="images/photo.jpg" %}

{% endcapture %}

{% include grid.html style="square" content=content %}
