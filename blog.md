---
layout: page
title: Blog
permalink: /blog/
---

**Welcome to my blog—a space dedicated to international arbitration and commercial law.**

Here you’ll find reflections on notable arbitral awards, treaty interpretation, and developments in the legal principles shaping global commerce. Whether you’re a practitioner, academic, or policy observer, this blog aims to offer clear and carefully researched insights grounded in international legal practice.

---

## Recent Posts

<ul style="list-style: none; padding-left: 0;">
  {% for post in site.posts %}
    <li style="display: flex; gap: 15px; align-items: flex-start; margin-bottom: 2em;">
      {% if post.thumbnail-img %}
        <img src="{{ post.thumbnail-img | relative_url }}" alt="Thumbnail for {{ post.title }}" style="width: 120px; height: auto; border-radius: 6px;" />
      {% else %}
        <img src="/assets/img/default-thumb.jpg" alt="Default thumbnail" style="width: 120px; height: auto; border-radius: 6px;" />
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
