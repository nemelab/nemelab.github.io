---
title: Research
nav:
  order: 3
  tooltip: Published works
---

<div style="text-align:center;">
  <h1><b>RESEARCH</b></h1>
</div>

## Highlighted

{% assign latest_citation = site.data.citations | sort: "date" | reverse | first %}
{% include citation.html citation=latest_citation style="rich" %}

{% include section.html %}

## All

{% include search-box.html %}

{% include search-info.html %}

{% include list.html data="citations" component="citation" style="rich" %}
