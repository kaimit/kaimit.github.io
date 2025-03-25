---
layout: page
title: Writings
permalink: /blog/
---

Here are my latest thoughts, insights, and research notes on various topics.

<div class="posts-list">
  {% for post in site.posts %}
    <div class="post-item">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
      {% if post.categories.size > 0 %}
        <div class="post-categories">
          {% for category in post.categories %}
            <span class="post-category">{{ category }}</span>
          {% endfor %}
        </div>
      {% endif %}
      <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
      <p class="read-more"><a href="{{ post.url | relative_url }}">Read more →</a></p>
    </div>
  {% endfor %}
</div>