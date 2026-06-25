---
layout: archive
title: "Sitemap"
permalink: /sitemap/
---

The main pages on this site. Crawlers can also use the [XML sitemap]({{ "/sitemap.xml" | relative_url }}).

## Pages
<ul>
  <li><a href="{{ "/" | relative_url }}">Home</a></li>
  <li><a href="{{ "/blog/" | relative_url }}">Blog Posts</a></li>
  {% for link in site.data.navigation.main %}
  <li><a href="{% if link.url contains "://" %}{{ link.url }}{% else %}{{ link.url | relative_url }}{% endif %}">{{ link.title }}</a></li>
  {% endfor %}
</ul>

{% if site.posts.size > 0 %}
## Posts
<ul>
  {% for post in site.posts %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> &mdash; {{ post.date | date: "%-d %b %Y" }}</li>
  {% endfor %}
</ul>
{% endif %}
