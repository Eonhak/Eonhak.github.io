---
layout: single
title: "Hak_Devlog"
permalink: /
author_profile: true
sidebar:
  nav: "docs"   # _data/navigation.yml에서 정의한 사이드바 그룹
---

## Recent posts

{% raw %}{% for post in site.posts limit:10 %}
- [{{ post.title }}]({{ post.url | relative_url }}) <small>({{ post.date | date: "%Y-%m-%d" }})</small>
{% endfor %}{% endraw %}
