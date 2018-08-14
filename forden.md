---
layout: default
title: Για τα μέλη
---


## For De

 <h1>Blog Posts</h1>
  <ul class="posts">
    {% for post in site.categories.misc %}
      <li><a href="{{ post.url | relative_url}}">{{ post.title }}</a></li>
    {% endfor %}
</ul>


<h1>Blog tags</h1>
<ul>
    {% for tag in site.tags %}		
        <li><a href="/tags/{{ tag[0] }}">{{ tag[0] }}</a></li>
    {% endfor %}
</ul>



<h1>Posts and tags</h1>
{% for tag in site.tags %}
  {% assign t = tag | first %}
  {% assign posts = tag | last %}

{{ t | downcase }}
<ul>
{% for post in posts %}
  {% if post.tags contains t %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    <span class="date">{{ post.date | date: "%B %-d, %Y"  }}</span>
  </li>
  {% endif %}
{% endfor %}
</ul>
{% endfor %}
