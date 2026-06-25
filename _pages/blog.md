---
layout: default
title: "Blog Posts"
permalink: /blog/
---

<ul class="post-list">
{% for post in site.posts %}
  <li>
    <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="post-date">{{ post.date | date: "%-d %b %Y" }}</span>
    {% if post.excerpt %}<p class="post-excerpt">{{ post.excerpt | strip_html | normalize_whitespace | truncatewords: 30 }}</p>{% endif %}
  </li>
{% endfor %}
</ul>
