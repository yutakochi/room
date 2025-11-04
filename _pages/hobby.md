---
# title: "Hobby"
layout: single
permalink: /hobby/
author_profile: true
categories:
  - Hobby
---

<style>
.news-article {
    display: flex;
    align-items: center;
    margin-bottom: 20px; /* 記事間の間隔 */
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


<h1>Travel</h1>
{% assign travel_posts = site.categories.Travel %}
{% for post in travel_posts %}
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

<h1>Craft</h1>
{% assign craft_posts = site.categories.Hobby | where_exp:"post","post.categories contains 'Craft'" %}
{% for post in craft_posts %}
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

<h1>Music</h1>
{% assign music_posts = site.categories.Hobby | where_exp:"post","post.categories contains 'Music'" %}
{% for post in music_posts %}
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


