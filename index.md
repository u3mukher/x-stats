---
layout: default
title: Home
---

<section class="latest-posts">
  <h2>Latest Blog Post</h2>
  <div class="posts-container">
    {% for post in site.posts limit:1 %}
      <div class="post-item">
        {% if post.featured_image %}
          <img src="{{ post.featured_image | relative_url }}" alt="{{ post.title }} Image" class="post-image">
        {% endif %}
        <h3 class="post-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <h4 class="post-subtitle">{{ post.subtitle }}</h4>
        <p class="post-excerpt">{{ post.excerpt }}</p>
        <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
      </div>
    {% endfor %}
  </div>
</section>
