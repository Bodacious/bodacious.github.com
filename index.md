---
layout: default
title: Simple ideas to increase productivity, health and happiness
tagline: Supporting tagline
---

{% include JB/setup %}


{% for post in site.posts limit:5 %}

  <article id="post">
    <header>
      <h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
    </header>

    <p class="meta">
      <time datetime="{{ post.date | date_to_xmlschema }}" pubdate="pubdate">{{ post.date | date_to_long_string }}</time>
      {% if post.location %} - {{ post.location }}{% endif %}
    </p>
  
    {{ post.content }}

  </article>


{% endfor %}


