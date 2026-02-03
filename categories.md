---
layout: default
title: Categories
permalink: /categories/
---

<h1>Categories</h1>

<ul class="category-list">
  {% assign categories = site.categories | sort %}
  {% for category in categories %}
    {% assign category_name = category[0] %}
    {% assign posts = category[1] %}
    <li class="category-item">
      <div class="category-title">
        <strong>{{ category_name }}</strong>
        <span>({{ posts | size }})</span>
      </div>
      <ul class="post-list">
        {% for post in posts %}
          <li class="post-item">
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
            <small>{{ post.date | date: "%Y-%m-%d" }}</small>
          </li>
        {% endfor %}
      </ul>
    </li>
  {% endfor %}
</ul>
