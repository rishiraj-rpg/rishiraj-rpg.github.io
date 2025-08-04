---
layout: page
title: Blog
permalink: /blog/
---

<div class="custom-blog">

  
  <div class="posts">
    {% for post in site.posts %}
    <article class="post-item">
      <div class="post-date">{{ post.date | date: "%B %d, %Y" }}
      <a href="{{ post.url }}">{{ post.title }}</a>
      </div>
      <!-- {% if post.excerpt %}
      <p class="excerpt">{{ post.excerpt | strip_html | truncatewords: 25 }}</p>
      {% endif %} -->
    </article>
    {% endfor %}
  </div>
</div>

<style>
html {
  overflow-y: scroll;
}

</style>