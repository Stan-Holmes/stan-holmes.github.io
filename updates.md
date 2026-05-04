---
layout: default
title: Updates
permalink: /updates/
---

<p class="updates-intro">Thoughts, updates, and ideas from Stan Holmes.</p>

{% assign posts = site.posts | sort: "date" | reverse %}

<div class="post-list">
{% for post in posts %}
<article class="post-card">
  <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
  <p class="post-date">
    {{ post.date | date: "%B %d, %Y" }}
  </p>
  <div>
    {{ post.excerpt }}
  </div>
  <p class="read-more"><a href="{{ post.url | relative_url }}">Read more &rarr;</a></p>
</article>
{% endfor %}
</div>

{% if posts.size == 0 %}
<p>No updates yet. Come back soon!</p>
{% endif %}
