---
layout: page
permalink: /publications/
title: publications
description: # publications by categories in reversed chronological order. generated by jekyll-scholar.
years: [2022, 2021, 2020, 2019, 2018, 2017, 2015]
nav: true
nav_order: 1
---

My full publication list can be found <a href="https://ui.adsabs.harvard.edu/public-libraries/jrLQy960Q4u3Lx5DEQlpFA">here</a>. 
Below is a selection of my lead-author papers. 

<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
