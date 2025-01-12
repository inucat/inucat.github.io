---
layout: page
title: "Posts"
permalink: /posts
theme: jekyll-theme-minimal
---

# 全ての記事 / All posts

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.created_date | date: "%Y-%m-%d %H:%M" }} - {{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
