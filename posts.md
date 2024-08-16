---
layout: page
title: Posts
permalink: /posts/
---

# My Blog Posts

{% for post in site.posts %}
  <article>
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <time datetime="{{ post.date | date: "%Y-%m-%d" }}">{{ post.date | date_to_long_string }}</time>
    {% if post.tags %}
      <p class="tags">Tags: {{ post.tags | join: ", " }}</p>
    {% endif %}
    <p>{{ post.description | default: post.excerpt }}</p>
    <a href="{{ post.url | relative_url }}">Read more</a>
  </article>
{% endfor %}