---
layout: default
title: Blog
permalink: /blog/
---

# Blog

Welcome to my blog — a space dedicated to exploring **international arbitration**, **commercial law**, and **cross-border dispute resolution**.

Here you'll find commentary on landmark cases, treaty interpretation, and evolving legal frameworks in the global economy. Whether you're a legal practitioner, academic, or policy follower, this space offers concise and well-researched analysis grounded in international practice.

---

## Recent Posts

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a><br />
      <small>{{ post.date | date: "%B %d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>
