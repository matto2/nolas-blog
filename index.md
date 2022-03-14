---
layout: layout.njk
title: Nola’s Blog
---

<!-- # {{ title }} -->


<nav class="nav">
  <div class="nav-left">
    <a class="brand" href="/"><img src="/assets/img/nola-logo.png">Nola’s Blog</a>
  </div> 
  <div class="nav-right">
    <div class="tabs">
      <a  class="active" href="/">Home</a>
      <a href="/about">About</a>

  </div>
</nav>


# Welcome to my blog!

<!-- {%- for post in collections.blog %}
* [{{ post.data.title }}]({{ post.url }})
{%- endfor %}  -->


<ul>
  {%- for post in collections.blog | reverse -%}
    <li>
      <h3><a href="{{ post.url | url }}">{{ post.data.title }}</a> | {{ post.date | readableDate }}
</h3>
      <!-- {% if post.data.teaser %}
        <p>{{ post.data.teaser }}</p>
      {% endif %}  -->
    </li>
  {%- endfor -%}
</ul>