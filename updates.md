---
layout: default
title: Updates
permalink: /updates/
---

## Thoughts, updates, and ideas from Stan Holmes.
<p></p>

{% assign posts = site.posts | sort: "date" | reverse %}

{% for post in posts %}
<div style="margin-bottom: 40px; padding-bottom: 30px; border-bottom: 1px solid #eee;">
  <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
  <p style="color: #666; font-size: 0.95em;">
    {{ post.date | date: "%B %d, %Y" }}
  </p>
  <div>
    {{ post.excerpt }}
  </div>
  <p><a href="{{ post.url | relative_url }}">Read more &rarr;</a></p>
</div>
{% endfor %}

{% if posts.size == 0 %}
<p>No updates yet. Come back soon!</p>
{% endif %}
