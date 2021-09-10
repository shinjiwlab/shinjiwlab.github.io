---
layout: page
permalink: /publications/
title: Publications
years: [2021, 2020, 2019, 2018, 2017]
nav: true
order: 2
---

- [2021 Papers](https://shinjiwlab.github.io/activities/2021/paper-list/)
- [2020 Papers](https://shinjiwlab.github.io/activities/2020/paper-list/)
- [2019 Papers](https://shinjiwlab.github.io/activities/2019/paper-list/)
- [2018 Papers](https://shinjiwlab.github.io/activities/2018/paper-list/)


<div class="publications">

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>


