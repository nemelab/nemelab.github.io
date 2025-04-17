---
title: Members
nav:
  order: 1
  tooltip: About our lab members
---

# {% include icon.html icon="fa-solid fa-users" %}Members

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

{% include section.html %}

<h2>Professor</h2>
<div class="member-section">
  {% include list.html data="members" component="portrait" filter="role == 'pi'" %}
</div>

<h2>Member</h2>
<div class="member-section">
  {% include list.html data="members" component="portrait" filter="role == 'student'" %}
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
