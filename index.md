---
layout: single
title: "Recent Posts"
author_profile: true
classes: home-feed   # ← 추가
sidebar:
  nav: "docs"   # _data/navigation.yml에서 정의한 사이드바 그룹
---

<div class="archive">
{% for post in site.posts limit:10 %}
  {% include archive-single.html %}
{% endfor %}
</div>
