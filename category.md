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
    <ul style="margin-top:15px;margin-bottom:15px;">
      {% for post in tag[1] %}
      <a style="color:#343851;" href="{{ site.baseurl }}{{ post.url }}">
      <li style="margin-top:5px;margin-bottom:5px;">
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
