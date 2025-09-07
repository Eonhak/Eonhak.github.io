---
layout: single
title: "Recent Posts"
author_profile: true
classes: home-feed   # ← 추가
sidebar:
  nav: "docs"   # _data/navigation.yml에서 정의한 사이드바 그룹
---

<ul class="home-feed-list">
{% for post in site.posts limit: 3 %}  {# ← 원하는 개수로 변경 #}
  <li class="home-feed-item">
    <a class="home-feed-title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <div class="home-feed-meta">
      {{ post.date | date: "%Y-%m-%d" }}
      {% comment %} 읽는시간을 쓰고 싶으면 아래 라인 주석 해제 {% endcomment %}
      {%- comment -%} · {% include read-time.html content=post.content %} {%- endcomment -%}
    </div>
    <p class="home-feed-excerpt">
      {{ post.excerpt | strip_html | normalize_whitespace | truncate: 140 }}
    </p>
  </li>
{% endfor %}
</ul>
