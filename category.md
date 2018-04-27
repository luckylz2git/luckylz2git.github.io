---
layout: page
title: Category
permalink: /category/
---

<div class="tags-expo">
  <div class="tags-expo-list">
    {% for tag in site.categories %}
    <a href="#{{ tag[0] | slugify }}" class="post-tag">{{ tag[0] }}</a>
    {% endfor %}
  </div>
  <hr/>
  <div class="tags-expo-section">
    {% for tag in site.categories %}
    <h2 id="{{ tag[0] | slugify }}">{{ tag[0] }}</h2>
    <ul class="tags-expo-posts">
      {% for post in tag[1] %}
        <a class="post-title" href="{{ site.baseurl }}{{ post.url }}">
      <li>
        <div class="post-card__header">
          <h4>{{ post.title }}</h4>
          {% assign date_format = site.sleek.date_format | default: "%b %-d, %Y" %}
          <span class="post-card__meta">
            <time>{{ post.date | date: date_format }}</time>
          </span>
        </div>
      </li>
      </a>
      {% endfor %}
    </ul>
    {% endfor %}
  </div>
</div>
