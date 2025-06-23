---
layout: page
title: Blog
permalink: /blog/
---

**Welcome to my blog—where I focus on Investor-State Dispute Settlement (ISDS) within the wider framework of international arbitration and commercial law.**

Here you’ll find plain-spoken takes on the latest ISDS awards, shifts in treaty wording and interpretation, and the legal twists that steer global business and investment. When it helps put things in context, I’ll dip into related corners of public international law too.

The goal is to make complex issues understandable, without losing sight of how these rules play out in the real world.

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
