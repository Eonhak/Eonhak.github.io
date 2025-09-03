---
layout: single
permalink: /
title : Recent Posts
author_profile: true
sidebar:
  nav: "docs"   # _data/navigation.yml에서 정의한 사이드바 그룹
---

{% for post in site.posts limit:10 %}
- [{{ post.title | escape }}]({{ post.url | relative_url }}) <small>({{ post.date | date: "%Y-%m-%d" }})</small>
{% endfor %}
