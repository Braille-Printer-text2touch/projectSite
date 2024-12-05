---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Text2Type
permalink: /
---
## [About]({{ site.baseurl }}{% link about.md %})

## Vision

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
