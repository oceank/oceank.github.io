---
layout: page
permalink: /publications/
title: Publications
description:
years: [2014, 2019, 2020, 2022, 2023]
nav: true
---

<div class="publications">

{% assign sorted_years = page.years | sort | reverse %}
{% for y in sorted_years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
