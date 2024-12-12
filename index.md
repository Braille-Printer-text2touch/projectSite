---
layout: default
title: Text2Type ⠠⠞⠑⠭⠞⠼⠃⠠⠞⠽⠏⠑
permalink: /
---
## Featured
{% for post in site.posts %}
{% if post.featured == true %}
<article>
  <h3>
    <a href="{{ '.' | append: post.url }}">
      {{ post.title }}
    </a>
  </h3>
</article>
{% endif %}
{% endfor %}

<hr>

## Posts
{% for post in site.posts %}
<article>
  <h3>
    <a href="{{ '.' | append: post.url }}">
      {{ post.title }}
    </a>
  </h3>
  <time datetime="{{ post.date | date: '%Y-%m-%d' }}">{{ post.date | date_to_long_string }}</time>
</article>
{% endfor %}
