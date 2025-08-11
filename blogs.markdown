---
layout: page
title: Stories
permalink: /stories/
---

<div class="home">
  {%- if site.posts.size > 0 -%}
    <!-- <h2 class="post-list-heading">{{ page.list_title | default: "Posts" }}</h2> -->
    <ul class="post-list">
      {%- for post in site.posts -%}
      <li>
        {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <span class="post-meta">{{ post.date | date: date_format }}</span>
        <h3>
          <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
        </h3>
        <!-- {%- if site.show_excerpts -%}
          {{ post.excerpt }}
        {%- endif -%} -->
        {% if post.excerpt %}
        <p class="excerpt">{{ post.excerpt | strip_html | truncatewords: 25 }}</p>
        {% endif %}
      </li>
      {%- endfor -%}
    </ul>

    <!-- <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | relative_url }}">via RSS</a></p> -->
  {%- endif -%}
</div>

<style>
html {
  overflow-y: scroll;
}

  .post-list .excerpt {
  margin-top: -10px;
  margin-bottom: 20px;
  color: #666;
  font-size: 0.9em;
  line-height: 1.4;
  padding-left: 0;
}

.post-list li {
  margin-bottom: 30px;
}

.post-list h3 {
  margin-bottom: 8px;
}

.site-title {
  font-weight: normal;    /* or bold, 300, 400, 500, etc. */
  font-size: 26px;
  color: #424242;
}
</style>