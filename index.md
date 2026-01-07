---
layout: default
title: Index
---

# About me

My name is Rune Aamodt and I'm a software developer living in Norway. Welcome to my blog, if you have any feedback feel free to reach out via [LinkedIn](https://www.linkedin.com/in/runeaam/).

# Blog posts

{% for post in site.posts %}

## [{{ post.title }}]({{ post.url | relative_url }})

_{{ post.date | date: "%Y-%m-%d" }}_{% if post.categories and post.categories.size > 0 %} — {{ post.categories | join: ", " }}{% endif %}

{{ post.excerpt | strip_html | truncate: 240 }}

[Read more →]({{ post.url | relative_url }})

{% endfor %}
