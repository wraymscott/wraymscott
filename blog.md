---
layout: page
title: Blog
permalink: blog
---

<div>
  {% for post in site.posts %}
    <div class="py-4 flex items-center gap-4"> 
      {% if post.thumbnail %}
        <img src="{{ post.thumbnail | relative_url }}" 
             alt="{{ post.title }}" 
             style="width: 60px; height: 60px; object-fit: cover; border-radius: 4px; margin-right: 30px;">
      {% endif %}

      <div>
        <h3 class="m-0">
          <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
        </h3>
        <div class="text-sm text-gray-400">
          {{ post.date | date: "%B %-d, %Y" }}
        </div>
      </div>
    </div>
  {% endfor %}
</div>