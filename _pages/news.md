---
title: "News"
header:
  overlay_image: /assets/images/IMG_5538.jpg
  caption: "Photo by Yuta Kochi"
permalink: /news/
layout: single
author_profile: true
categories:
  - News
---

<style>
.news-article {
    display: flex;
    align-items: center;
    margin-bottom: 40px; /* 記事間の間隔 */
}
.news-article img {
    width: 150px;
    height: 100px;
    object-fit: cover;
    border-radius: 8px;
    margin-right: 20px;
}
.news-article div {
    margin: 0;
}
.news-article h2,
.news-article p {
    margin: 0;
}
.news-article p {
    margin: 0;
    font-size: 14px;  /* ここでフォントサイズを変更 */
    line-height: 1.4; /* 行間も調整可能 */
}
</style>

{% assign posts = site.categories.News %}
{% for post in posts %}
<article class="news-article">
    {% if post.header.image %}
    <img src="{{ site.baseurl }}{{ post.header.image }}" alt="thumbnail">
    {% endif %}
    <div>
        <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
        <p>{{ post.excerpt }}</p>
    </div>
</article>
{% endfor %}