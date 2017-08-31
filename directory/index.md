---
layout: page
title: directory
---
<div id="item-wrapper">
{% for tag in site.tags %}
<div class="tag-item">
  {% assign t = tag | first %}
  {% assign posts = tag | last %}

{{ t | downcase }}
<ul>
{% for post in posts %}
  {% if post.tags contains t %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
  </li>
  {% endif %}
{% endfor %}
</ul>
</div>
{% endfor %}
</div>
