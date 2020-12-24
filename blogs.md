---
layout: lecture
title: "全部文章"
---

# 技术

<ul>
{% assign blogs = site['blogs_learning'] | sort: 'date' %}
{% for blog in blogs %}
    <li>
    <strong>Update at {{ blog.date | date: '%-m/%d' }}</strong>:
    <a href="{{ blog.url }}">{{ blog.title }}</a>
    </li>
{% endfor %}
</ul>

# 随笔

<ul>
{% assign blogs = site['blogs_weekly'] | sort: 'date' %}
{% for blog in blogs %}
    <li>
    <a href="{{ blog.url }}"><strong>{{ blog.date | date: '%-m/%d' }}</strong></a>
    </li>
{% endfor %}
</ul>

<!-- <ul>
{% assign blogs = site['blogs'] | sort: 'date' %}
{% for blog in blogs %}
    <li>
    <strong>Update at {{ blog.date | date: '%-m/%d' }}</strong>:
    <a href="{{ blog.url }}">{{ blog.title }}</a>
    </li>
{% endfor %}
</ul> -->
