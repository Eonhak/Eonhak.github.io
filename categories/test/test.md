---
layout: single
title: "test"          # 화면 제목은 자유롭게
permalink: /categories/test/  # ← 원하는 경로
author_profile: true
classes: home-feed          # (선택) 홈과 동일한 스타일을 쓰고 싶을 때
---

<ul class="home-feed-list">
{% assign posts_by_tag = site.posts | where_exp: "post", "post.tags contains 'test'" %}
{% for post in posts_by_tag %}
  <li class="home-feed-item">
    <a class="home-feed-title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <div class="home-feed-meta">{{ post.date | date: "%Y-%m-%d" }}</div>
    <p class="home-feed-excerpt">
      {{ post.excerpt | strip_html | normalize_whitespace | truncate: 140 }}
    </p>
  </li>
{% endfor %}
</ul>