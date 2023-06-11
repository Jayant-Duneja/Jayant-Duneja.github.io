---
layout: page
title: Work
permalink: /work/
description: My work experiences over the years. Click to read more in detail about each.
nav: true
horizontal: true
---
<div class="work">
  {% assign sorted_work = site.work | sort: "date" | reverse %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
    <div class="container">
      <div class="row row-cols-1">
      {% for work in sorted_work %}
        {% include work_horizontal.html %}
      {% endfor %}
      </div>
    </div>
  {% else %}
    <div class="grid">
      {% for work in sorted_work %}
        {% include work.html %}
      {% endfor %}
    </div>
  {% endif %}
</div>
