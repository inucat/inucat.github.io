---
layout: page
title: "Posts"
permalink: /posts
theme: jekyll-theme-minimal
---

# All posts

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ site.time | date: "%Y-%m-%d %H:%M" }} - {{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
