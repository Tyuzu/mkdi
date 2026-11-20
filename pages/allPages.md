---
pageTitle: All
navTitle: All
permalink: /all/
---
Static page content goes here.

{%- for post in collections.pages reversed -%}
    <article>
        <h2><a href="{{ post.url }}">{{ post.data.pageTitle }}</a></h2>
        <time datetime="{{ post.date | date: '%Y-%m-%d' }}">{{ post.date | date: "%Y-%m-%d" }}</time>
        {%- if post.data.subtitle -%}
            <p>{{ post.data.subtitle }}</p>
        {%- endif -%}
    </article>
{%- endfor -%}