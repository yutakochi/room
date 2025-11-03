---
title: "News"
permalink: /news/
layout: single
author_profile: true
categories:
  - News
---

{% assign posts = site.categories.News %}
{% for post in posts %}
<article style="display: flex; align-items: center; margin-bottom: 20px;">
    {% if post.header.image %}
    <img src="{{ site.baseurl }}{{ post.header.image }}" alt="thumbnail"
         style="width:150px; height:100px; object-fit:cover; border-radius:8px; margin-right: 20px;">
    {% endif %}
    <div>
        <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
        <p>{{ post.excerpt }}</p>
    </div>
</article>
{% endfor %}