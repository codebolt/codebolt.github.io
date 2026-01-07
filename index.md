---
layout: default
title: Blog
---

# Blog

{% for post in site.posts %}

## [{{ post.title }}]({{ post.url | relative_url }})

_{{ post.date | date: "%Y-%m-%d" }}_{% if post.categories and post.categories.size > 0 %} — {{ post.categories | join: ", " }}{% endif %}

{{ post.excerpt | strip_html | truncate: 240 }}

[Read more →]({{ post.url | relative_url }})

{% endfor %}
