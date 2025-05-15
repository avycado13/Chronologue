---
---

# Chronuelogue

Welcome to Chronuelogue, a beautiful timeline theme for Jekyll.

<div class="timeline">
  {% assign sorted_posts = site.posts | sort: 'date' %}
  {% for post in sorted_posts %}
    <div class="sticky-note">
      <div class="timeline-event-date">{{ post.date | date: '%Y-%m-%d' }}</div>
      <div class="timeline-event-title">{{ post.title }}</div>
      <div class="timeline-event-content">{{ post.excerpt | strip_html | truncatewords: 30 }} <a href="{{ post.url }}">Read more</a></div>
    </div>
  {% endfor %}
</div>