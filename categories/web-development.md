---
layout: page
permalink: /blog/web-development/
title: "Articles in Category Web Development"
---

<h4><a href="/categories">All Categories</a> | <a href="/blog">Most Recent</a></h4> 

<div>
{% for post in site.categories.Web-Development %}
 {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
 <span class="post-meta">{{ post.date | date: date_format }}</span> 
<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
{% endfor %}
</div>