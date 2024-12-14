---
layout: default
title: Home
---

<section class="latest-posts">
  <h2>Latest Blog Posts</h2>
  <ul>
    {% for post in site.posts limit:5 %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span>
      </li>
    {% endfor %}
  </ul>
</section>

