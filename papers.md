---
layout: page
title: Papers
permalink: /papers/
---

Below is a list of my published papers. Click on the title to access more details including abstracts and PDF downloads.

<div class="papers-list">
  {% for paper in site.data.papers %}
    <div class="paper-item">
      <h3><a href="{{ paper.url | relative_url }}">{{ paper.title }}</a></h3>
      <p class="authors">{{ paper.authors }}</p>
      <p class="venue">{{ paper.venue }}, {{ paper.year }}</p>
      {% if paper.tags %}
        <div class="paper-tags">
          {% for tag in paper.tags %}
            <span class="paper-tag">{{ tag }}</span>
          {% endfor %}
        </div>
      {% endif %}
    </div>
  {% endfor %}
</div>