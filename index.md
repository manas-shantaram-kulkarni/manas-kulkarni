---
title: "Manas Kulkarni"
permalink: /
excerpt: "UWC, Harvard, Oxford, NYU, Meta"
hide_title: true
---

## About Me

I am a **junior research scientist** at **NYU Stern**, where I study **social capital** and **economic connectedness** with Johannes Stroebel and Theresa Kuchler. I am also a **researcher at Meta** and a **research associate at Opportunity Insights**.

I am applying to economics PhD programs and hope to become an academic economist.

I graduated *magna cum laude* from **Harvard** with high honors in **Economics and Government**, and was a visiting student in **Philosophy, Politics, and Economics** at **Oriel College, Oxford**.

Before college, I attended **United World College Dilijan**, an international boarding school in Armenia. Before that, I lived in **India**: I was born in **Belgaum** and raised in **Mumbai** and **Pune**.

## Published and Forthcoming Papers

{% for item in site.data.research.published %}
<article class="entry">
  <h3>{{ item.title }}</h3>
  {% if item.coauthors and item.coauthors != "" %}
    <p class="meta">{{ item.coauthors }}</p>
  {% endif %}
  {% if item.publication_info and item.publication_info != "" %}
    <p class="meta"><strong>{{ item.publication_info }}</strong></p>
  {% endif %}
  {% if item.presented and item.presented != "" %}
    <p class="meta">{{ item.presented }}</p>
  {% endif %}
  {% if item.abstract and item.abstract != "" or item.links and item.links.size > 0 %}
    <div class="entry-links">
      {% if item.abstract and item.abstract != "" %}
        <details class="abstract-toggle">
          <summary>Abstract</summary>
        </details>
      {% endif %}
      {% for link in item.links %}
        <a href="{{ link.url }}">{{ link.label }}</a>
      {% endfor %}
      {% if item.abstract and item.abstract != "" %}
        <p class="abstract-text">{{ item.abstract }}</p>
      {% endif %}
    </div>
  {% endif %}
</article>
{% endfor %}

## Working Papers and Independent Projects

{% for item in site.data.research.working %}
<article class="entry">
  <h3>{{ item.title }}</h3>
  {% if item.coauthors and item.coauthors != "" %}
    <p class="meta">{{ item.coauthors }}</p>
  {% endif %}
  {% if item.publication_info and item.publication_info != "" %}
    <p class="meta"><strong>{{ item.publication_info }}</strong></p>
  {% endif %}
  {% if item.presented and item.presented != "" %}
    <p class="meta">{{ item.presented }}</p>
  {% endif %}
  {% if item.abstract and item.abstract != "" or item.links and item.links.size > 0 %}
    <div class="entry-links">
      {% if item.abstract and item.abstract != "" %}
        <details class="abstract-toggle">
          <summary>Abstract</summary>
        </details>
      {% endif %}
      {% for link in item.links %}
        <a href="{{ link.url }}">{{ link.label }}</a>
      {% endfor %}
      {% if item.abstract and item.abstract != "" %}
        <p class="abstract-text">{{ item.abstract }}</p>
      {% endif %}
    </div>
  {% endif %}
</article>
{% endfor %}
