---
layout: default
title: Blog
permalink: /blog/
---

<section class="latest-posts">
  <h2>Blog</h2>
  <div class="posts-container">
    {% for post in site.posts %}
      <div class="post-item">
        {% if post.featured_image %}
          <img src="{{ post.featured_image | relative_url }}" alt="{{ post.title }} Image" class="post-image">
        {% endif %}
        <h3 class="post-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <p class="post-excerpt">{{ post.excerpt }}</p>
        <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
      </div>
    {% endfor %}
  </div>
</section>
