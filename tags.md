---
layout: page
title: Tags
permalink: /tags
---

{% comment %}
<!--
- Create an empty array.
- Obtain a tag name and push it to the array.
- Sort the tag names.
- List tags as a tag cloud.
-->
{% endcomment %}

# Tags

{% assign tag_names = "" | split: "|"  %}

{% for posts_by_tag in site.tags %}
  {% assign tag_names = tag_names | push: posts_by_tag.first %}
{% endfor %}

{% assign tag_names = tag_names | sort %}

{% include tag_cloud.html tag_names=tag_names %}



<section class="posts-by-tags">
  {% for tag_name in tag_names %}
    <div>
      <h2 id="{{ tag_name }}">
        {{ tag_name | replace: "_", " " }}
      </h2>

      {% for post in site.tags[tag_name] %}
        <a href="{{ post.url | prepend: baseurl }}">
          {{ post.title }}
        </a><br />
      {% endfor %}
    </div>
  {% endfor %}
</section>
