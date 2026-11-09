---
title: Blog Posts
permalink: /blog/
layout: collection
---

<ul id="blog-posts">
  {% if site.posts.size == 0 %}
  <p>No posts...yet.</p>
  {% else %}
  {% for post in site.posts limit:3 %}
  <li class="blog-posts__item">
    {% if post.image %}
    <img class="post-image" src="{{ post.image }}">
    {% endif %}
    <div class="post-details">
      <p class="type-text size-tiny">{{ post.date | date: '%m.%d.%Y' }}</p>
      <a href="{{ post.url }}">{{ post.title }} {% include icons/move-left.html %}</a>
    </div>
  </li>
  {% endfor %}
  {% endif %}
</ul>
