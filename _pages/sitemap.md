---
layout: archive
title: "Sitemap"
permalink: /sitemap/
author_profile: true
---

A human-readable index of the public pages on this site. For crawlers and other automated tools, the [XML sitemap]({{ '/sitemap.xml' | relative_url }}) is also available.

{% assign sorted_pages = site.pages | sort: "title" %}
{% assign sorted_portfolio = site.portfolio | sort: "title" %}
{% assign sorted_publications = site.publications | sort: "date" | reverse %}

<h2>Pages</h2>
<ul>
  {% for item in sorted_pages %}
    {% if item.path contains '_pages/' and item.sitemap != false and item.url and item.title and item.url != '/404.html' and item.url != page.url %}
      <li><a href="{{ item.url | relative_url }}">{{ item.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>

<h2>Portfolio</h2>
<ul>
  {% for item in sorted_portfolio %}
    {% if item.sitemap != false and item.url and item.title %}
      <li><a href="{{ item.url | relative_url }}">{{ item.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>

<h2>Publications</h2>
<ul>
  {% for item in sorted_publications %}
    {% if item.sitemap != false and item.url and item.title %}
      <li>
        <a href="{{ item.url | relative_url }}">{{ item.title }}</a>
        {% if item.date or item.venue %}
          <br>
          <small>
            {% if item.date %}{{ item.date | date: "%B %d, %Y" }}{% endif %}
            {% if item.date and item.venue %} | {% endif %}
            {% if item.venue %}{{ item.venue }}{% endif %}
          </small>
        {% endif %}
      </li>
    {% endif %}
  {% endfor %}
</ul>
