---
layout: page
permalink: /publications/
title: Publications
#description:
years: [2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013]
---
My full list of publications can be also found in my [Google Scholar Profile](https://scholar.google.com/citations?user=A3CAMtYAAAAJ&hl=en&oi=ao).

{% for y in page.years %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}
