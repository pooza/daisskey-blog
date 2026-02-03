---
layout: default
title: Home
---

<h1>Posts</h1>
<ul class="post-list">
  {% for post in site.posts %}
    <li class="post-item">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small>{{ post.date | date: "%Y-%m-%d" }}</small>
    </li>
  {% endfor %}
</ul>
