---
pageTitle: News
navTitle: News
permalink: /news/
---

{%- for post in collections.posts reversed -%}
  <article>
    <h2><a href="{{ post.url | escape }}">{{ post.data.pageTitle | default: post.data.title | escape }}</a></h2>
    {%- if post.date -%}
      <time datetime="{{ post.date | date: '%Y-%m-%d' }}">{{ post.date | date: "%Y-%m-%d" }}</time>
    {%- endif -%}
    {%- if post.data.subtitle != blank -%}
      <p>{{ post.data.subtitle | escape }}</p>
    {%- endif -%}
  </article>
{%- endfor -%}