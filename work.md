---
layout: default
title: Work
permalink: /work/
---
<div class="single-column page">
  <h1>Work</h1>
  <ul class="item-list">
    {% for item in site.portfolio %}
    <li>
      <a href="{{ item.url | relative_url }}">
        <span class="item-title">{{ item.title }}</span>
        {% if item.summary %}<span class="item-summary">{{ item.summary }}</span>{% endif %}
      </a>
    </li>
    {% endfor %}
  </ul>
</div>
