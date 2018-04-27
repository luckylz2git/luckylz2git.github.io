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
      <a style="color:#343851;" href="{{ site.baseurl }}{{ post.url }}">
      <li>
        <div>
          {{ post.title }}
          {% assign date_format = site.sleek.date_format | default: "%b %-d, %Y" %}
          <small style="padding-left:7px;color:#a0a0a0;">{{ post.date | date: date_format }}</small>
        </div>
      </li>
      </a>
      {% endfor %}
    </ul>
    {% endfor %}
  </div>
</div>
