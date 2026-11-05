---
layout: default
title: Posts
---
<section>
  <h1>Posts</h1>
  <p class="subtitle">Security engineering research and local inference</p>
  {% if site.posts.size > 0 %}
  <ul class="post-list">
    {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span class="date">{{ post.date | date: "%B %-d, %Y" }}</span>
    </li>
    {% endfor %}
  </ul>
  {% else %}
  <p>Nothing published yet.</p>
  {% endif %}
</section>
