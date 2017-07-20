---
layout: page
title: Tags
permalink: /tags
---


{% assign tag_names = "" | split: "|"  %}

{% for posts_by_tag in site.tags %}
  {% assign tag_names = tag_names | push: posts_by_tag.first %}
{% endfor %}

{% assign tag_names = tag_names | sort %}

{% include tag_cloud.html tag_names=tag_names %}


{% for tag_name in tag_names %}
<h2 id="{{ tag_name }}">
  {{ tag_name | replace: "_", " " }}
</h2>
<ul>
{% for post in site.tags[tag_name] %}
  <li><a href="{{ post.url | prepend: baseurl }}">
    {{ post.title }}
  </a></li>
{% endfor %}
</ul>
{% endfor %}
