---
title: English
permalink: /en/
icon: fas fa-language
order: 5
---

{% assign posts = site.posts | where: 'lang', 'en' %}

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
<p>No English posts yet.</p>
{% endif %}
