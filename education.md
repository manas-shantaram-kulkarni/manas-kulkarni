---
title: "Education"
permalink: /education/
---

{% for item in site.data.education %}
<article class="entry education-entry">
  <div class="entry-header">
    <h3>{% include markdown-inline.html text=item.institution %}</h3>
    {% if item.location and item.location != "" %}
      <p class="meta entry-location">{% include markdown-inline.html text=item.location %}</p>
    {% endif %}
    {% if item.degree and item.degree != "" %}
      <p class="meta entry-subtitle">{% include markdown-inline.html text=item.degree %}</p>
    {% endif %}
    {% if item.dates and item.dates != "" %}
      <p class="meta entry-dates">{% include markdown-inline.html text=item.dates %}</p>
    {% endif %}
    {% if item.grades and item.grades != "" %}
      <p class="meta entry-grades">{% include markdown-inline.html text=item.grades %}</p>
    {% endif %}
  </div>
  {% if item.description and item.description != "" %}
    <div class="entry-description">{{ item.description | markdownify }}</div>
  {% endif %}
  {% if item.links and item.links.size > 0 %}
    <p class="entry-links">
      {% for link in item.links %}
        <a href="{{ link.url }}">{% include markdown-inline.html text=link.label %}</a>
      {% endfor %}
    </p>
  {% endif %}
</article>
{% endfor %}
