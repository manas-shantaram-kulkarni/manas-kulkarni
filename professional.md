---
title: "Professional"
permalink: /professional/
---

{% for item in site.data.experience %}
<article class="entry professional-entry">
  <div class="entry-header">
    <h3>{{ item.company }}</h3>
    <p class="meta entry-location">{{ item.location }}</p>
    <p class="meta entry-subtitle">{{ item.position }}</p>
    <p class="meta entry-dates">{{ item.dates }}</p>
  </div>
  <p>{{ item.description }}</p>
  {% if item.links and item.links.size > 0 %}
    <p class="entry-links">
      {% for link in item.links %}
        <a href="{{ link.url }}">{{ link.label }}</a>
      {% endfor %}
    </p>
  {% endif %}
</article>
{% endfor %}
