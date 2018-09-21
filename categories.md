---
layout: page
title: Categories
permalink: /categories/
---


  <div style = "font-size: 25px;">
    {% for tag in site.categories %}
        <a href="#{{ tag[0] | slugify }}" class="post-tag">{{ tag[0] }}</a>
        <span class="size">({{ tag | last | size }})</span>
    {% endfor %}
  </div>
  <div >
    {% for tag in site.categories %}
    <h2 id="{{ tag[0] | slugify }}">{{ tag[0] }}</h2>
    <ul>
      {% for post in tag[1] %}
        <a class="post-title" href="{{ site.baseurl }}{{ post.url }}">
      <li>
        {{ post.title }}
      <small class="post-date">{{ post.date | date_to_string }}</small>
      </li>
      </a>
      {% endfor %}
    </ul>
    {% endfor %}
  </div>
