---
layout: single
title: "test"          # 화면 제목은 자유롭게
permalink: /categories/test/  # ← 원하는 경로
author_profile: true
classes: home-feed          # (선택) 홈과 동일한 스타일을 쓰고 싶을 때
sidebar:
  nav: "docs" 
---

<div class="archive">
{% assign posts_by_tag = site.posts | where_exp: "post", "post.tags contains 'test'" %}
{% for post in posts_by_tag %}
  {% include archive-single.html %}
{% endfor %}
</div>
