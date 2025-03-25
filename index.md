---
layout: default
---

<section class="hero">
  <div class="hero-content">
    <h1>Hello, I'm [Your Name]</h1>
    <p class="subtitle">[Your brief professional description - e.g., Researcher in AI and Machine Learning]</p>
  </div>
</section>

<section class="featured-content">
  <h2>Featured Papers</h2>
  <div class="paper-grid">
    {% for paper in site.data.papers limit:3 %}
    <div class="paper-card">
      <h3><a href="{{ paper.url | relative_url }}">{{ paper.title }}</a></h3>
      <p class="authors">{{ paper.authors }}</p>
      <p class="venue">{{ paper.venue }}, {{ paper.year }}</p>
    </div>
    {% endfor %}
  </div>
  <p class="view-all"><a href="{{ '/papers' | relative_url }}">View all papers →</a></p>
</section>

<section class="recent-posts">
  <h2>Recent Writings</h2>
  <div class="post-list">
    {% for post in site.posts limit:3 %}
    <div class="post-item">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
      <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
    </div>
    {% endfor %}
  </div>
  <p class="view-all"><a href="{{ '/blog' | relative_url }}">View all writings →</a></p>
</section>