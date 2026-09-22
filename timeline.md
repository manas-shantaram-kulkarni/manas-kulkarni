---
title: "Timeline"
permalink: /timeline/
---

{% for item in site.data.timeline %}
<section class="timeline-year">
  <h2>{{ item.year }}</h2>
  {% if item.items and item.items.size > 0 %}
    <ul>
      {% for bullet in item.items %}
        <li>{{ bullet | markdownify | remove: '<p>' | remove: '</p>' }}</li>
      {% endfor %}
    </ul>
  {% endif %}
</section>
{% endfor %}
