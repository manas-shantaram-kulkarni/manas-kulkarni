---
title: "Timeline"
permalink: /timeline/
---

{% for item in site.data.timeline %}
<section class="timeline-year">
  <h2>{% include markdown-inline.html text=item.year %}</h2>
  {% if item.items and item.items.size > 0 %}
    <ul>
      {% for bullet in item.items %}
        <li>{% include markdown-inline.html text=bullet %}</li>
      {% endfor %}
    </ul>
  {% endif %}
</section>
{% endfor %}
