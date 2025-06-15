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

<ul style="list-style: none; padding-left: 0;">
  {% for post in site.posts %}
    <li style="display: flex; gap: 15px; align-items: flex-start; margin-bottom: 2em;">
      {% if post.thumbnail-img %}
        <img src="{{ post.thumbnail-img }}" alt="Thumbnail for {{ post.title }}" style="width: 120px; height: auto; border-radius: 6px;" />
      {% endif %}
      <div>
        <a href="{{ post.url }}"><strong style="font-size: 1.1em;">{{ post.title }}</strong></a><br />

        {% assign words = post.content | number_of_words %}
        {% assign minutes = words | divided_by:200 %}
        <small>{{ post.date | date: "%B %d, %Y" }} — 📖 Reading time: {{ minutes | ceil }} minutes</small><br />

        {% if post.excerpt %}
          <p style="margin-top: 5px; margin-bottom: 0;">{{ post.excerpt }}</p>
        {% endif %}
      </div>
    </li>
  {% endfor %}
</ul>
