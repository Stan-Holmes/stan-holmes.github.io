---
layout: default
title: Blog
permalink: /blog/
---

## Blog

### Thoughts, updates, and ideas from Stan Holmes.
<p></p>

{% for post in site.posts %}
<div style="margin-bottom: 40px; padding-bottom: 30px; border-bottom: 1px solid #eee;">
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <p style="color: #666; font-size: 0.95em;">
    {{ post.date | date: "%B %d, %Y" }}
  </p>
  <div>
    {{ post.excerpt }}
  </div>
  <p><a href="{{ post.url }}">Read more →</a></p>
</div>
{% endfor %}

{% if site.posts.size == 0 %}
<p>No posts yet. Come back soon!</p>
{% endif %}
