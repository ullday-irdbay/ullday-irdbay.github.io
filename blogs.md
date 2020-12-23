---
layout: lecture
title: "全部文章"
---

<ul>
{% assign blogs = site['blogs/learning'] | sort: 'date' %}
{% for blog in blogs %}
    <li>
    <strong>Update at {{ blog.date | date: '%-m/%d' }}</strong>:
    <a href="{{ blog.url }}">{{ blog.title }}</a>
    </li>
{% endfor %}
</ul>