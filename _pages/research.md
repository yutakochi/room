---
title: "Researchs"
permalink: /research/
layout: single
author_profile: true
categories:
  - Research
---

{% assign posts = site.categories.Hobby %}
{% for post in posts %}
<article>
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  {% if post.header.image %}
  <img src="{{ post.header.image }}" alt="thumbnail" style="width:150px; height:100px; object-fit:cover;">
  {% endif %}
  <p>{{ post.excerpt }}</p>
</article>
{% endfor %}