---
layout: default
title: StanH
---

## Welcome to StanH 

{% for post in site.posts limit:3 %}
- [{{ post.title }}]({{ post.url | relative_url }}) - {{ post.date | date: "%B %d, %Y" }}
{% endfor %}

[View all updates &rarr;]({{ "/updates/" | relative_url }})
