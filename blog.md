---
layout: default
title: Blog
permalink: /blog/
---

# Blog

Welcome to our blog! Here you'll find all our posts.

{% for post in site.posts %}
  <article>
    <h2>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h2>
    <time datetime="{{ post.date | date_to_xmlschema }}">
      {{ post.date | date: "%B %d, %Y" }}
    </time>
    <p>{{ post.excerpt }}</p>
  </article>
{% endfor %}
