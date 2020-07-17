---
layout: page
permalink: /publications/
title: 
description: 
years: [2019, 2018]
nav: true
---

<div class="publications">
<h2>Submissions</h2>
<h2 class="year">2020</h2>
{% bibliography -f papers -q @*[status=working]* %}
</div>

<div class="publications">
<h2>Publications</h2>
{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}, status=published]* %}
{% endfor %}
</div>
