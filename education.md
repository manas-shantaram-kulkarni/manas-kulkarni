---
title: "Education"
permalink: /education/
---

{% for item in site.data.education %}
<article class="entry education-entry">
  <div class="entry-header">
    <h3>{{ item.institution }}</h3>
    {% if item.location and item.location != "" %}
      <p class="meta entry-location">{{ item.location }}</p>
    {% endif %}
    {% if item.degree and item.degree != "" %}
      <p class="meta entry-subtitle">{{ item.degree }}</p>
    {% endif %}
    {% if item.dates and item.dates != "" %}
      <p class="meta entry-dates">{{ item.dates }}</p>
    {% endif %}
    {% if item.grades and item.grades != "" %}
      <p class="meta entry-grades">{{ item.grades }}</p>
    {% endif %}
  </div>
  {% if item.description and item.description != "" %}
    <p>{{ item.description }}</p>
  {% endif %}
  {% if item.links and item.links.size > 0 %}
    <p class="entry-links">
      {% for link in item.links %}
        <a href="{{ link.url }}">{{ link.label }}</a>
      {% endfor %}
    </p>
  {% endif %}
</article>
{% endfor %}
