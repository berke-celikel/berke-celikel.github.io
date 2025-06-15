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

<ul style="padding-left: 0;">
  {% for post in site.posts %}
    <li style="margin-bottom: 2em; list-style: none;">
      <div style="display: flex; align-items: flex-start;">
        {% if post.thumbnail-img %}
          <img src="{{ post.thumbnail-img }}" alt="Thumbnail for {{ post.title }}" style="width: 100px; height: auto; margin-right: 15px; border-radius: 4px;" />
        {% endif %}
        <div>
          <a href="{{ post.url }}"><strong>{{ post.title }}</strong></a><br />
          <small>{{ post.date | date: "%B %d, %Y" }}</small><br />
          {% if post.excerpt %}
            <p style="margin-top: 5px;">{{ post.excerpt }}</p>
          {% endif %}
        </div>
      </div>
    </li>
  {% endfor %}
</ul>
