---
title: "Professional"
permalink: /professional/
---

{% for item in site.data.experience %}
<article class="entry professional-entry">
  <div class="entry-header">
    <h3>{% include markdown-inline.html text=item.company %}</h3>
    <p class="meta entry-location">{% include markdown-inline.html text=item.location %}</p>
    <p class="meta entry-subtitle">{% include markdown-inline.html text=item.position %}</p>
    <p class="meta entry-dates">{% include markdown-inline.html text=item.dates %}</p>
  </div>
  <div class="entry-description">{{ item.description | markdownify }}</div>
  {% if item.links and item.links.size > 0 %}
    <p class="entry-links">
      {% for link in item.links %}
        <a href="{{ link.url }}">{% include markdown-inline.html text=link.label %}</a>
      {% endfor %}
    </p>
  {% endif %}
</article>
{% endfor %}
