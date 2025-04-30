---
---

<div style="text-align:center;">

<h1><b>NEME LAB</b></h1>

차세대 배터리 소재 및 전기 화학에 관한 연구실입니다.<br>
함께 연구하고 싶거나 관심있는 학생들은 연락주세요.<br>
<b>minkyungkim@kw.ac.kr</b>

</div>

## Highlights

{% capture text %}

<div style="text-align:center;">
publicated research
</div>

{%
  include button.html
  link="research"
  text="See our publications"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}

{% endcapture %}

{%
  include feature.html
  image="images/photo.jpg"
  link="research"
  title="Our Research"
  text=text
%}

{% capture text %}

<div style="text-align:center;">
진행하고 있는 project들
</div>

{%
  include button.html
  link="projects"
  text="Browse our projects"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}

{% endcapture %}

{%
  include feature.html
  image="images/photo.jpg"
  link="projects"
  title="Our Projects"
  flip=true
  style="bare"
  text=text
%}

{% capture text %}

<div style="text-align:center;">
차세대 배터리 양극/전해질/분리막 연구실 members
</div>

{%
  include button.html
  link="members"
  text="Meet our members"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}

{% endcapture %}

{%
  include feature.html
  image="images/members.jpg"
  link="members"
  title="Our members"
  text=text
%}
