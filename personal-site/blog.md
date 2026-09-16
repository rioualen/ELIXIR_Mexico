---
layout: default
title: Blog
permalink: /blog/
---
<div class="single-column page">
  <h1>Blog</h1>
  <ul class="item-list">
    {% for post in paginator.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">
        <span class="item-title">{{ post.title }}</span>
        <span class="item-date">{{ post.date | date: "%b %-d, %Y" }}</span>
      </a>
      {% if post.excerpt %}<p class="item-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>{% endif %}
    </li>
    {% endfor %}
  </ul>

  <nav class="pagination">
    {% if paginator.previous_page %}
      <a href="{{ paginator.previous_page_path | relative_url }}">&larr; Newer</a>
    {% endif %}
    {% if paginator.next_page %}
      <a href="{{ paginator.next_page_path | relative_url }}">Older &rarr;</a>
    {% endif %}
  </nav>
</div>
