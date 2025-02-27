---
layout: default
permalink: /blog/
title: Blog
nav: true
nav_order: 1
---

<!-- Minimal Blog Page -->

<section class="blog-list">
  <!-- Example: display only the "selected" posts.
       In each post's front matter, add:
         selected: true
       if you want that post shown here.
  -->
  {% assign selected_posts = site.posts | where: "selected", true %}

  {% if selected_posts.size > 0 %}
    <ul>
      {% for post in selected_posts %}
        <li>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </li>
      {% endfor %}
    </ul>
  {% else %}
    <p>No posts to display yet.</p>
  {% endif %}
</section>
