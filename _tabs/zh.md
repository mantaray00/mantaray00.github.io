---
title: 中文
permalink: /zh/
icon: fas fa-language
order: 6
---

{% assign posts = site.posts | where: 'lang', 'zh-CN' %}

{% if posts.size > 0 %}
<ul>
  {% for post in posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span> — {{ post.date | date: '%Y-%m-%d' }}</span>
    </li>
  {% endfor %}
</ul>
{% else %}
<p>还没有中文文章。</p>
{% endif %}
