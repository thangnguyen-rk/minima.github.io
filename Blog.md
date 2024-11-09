---
layout: page
title: Blog
permalink: /Blog/
---

Mục này sẽ trình bày về các project

{% assign blog_posts = site.blog %}
{% if blog_posts.size > 0 %}
   <ul>
      {% for post in blog_posts %}
         <li>
            <a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date: "%b %d, %Y" }}
         </li>
      {% endfor %}
   </ul>
{% else %}
   <p>Chưa có bài viết nào.</p>
{% endif %}
