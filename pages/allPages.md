---
pageTitle: All
navTitle: All
permalink: /all/
---
Static page content goes here.

{%- for pg in collections.pages reversed -%}
  {%- if pg.url != page.url -%}
    <article>
      <h2><a href="{{ pg.url | escape }}">{{ pg.data.pageTitle | default: pg.data.title | escape }}</a></h2>
      {%- if pg.data.subtitle != blank -%}
        <p>{{ pg.data.subtitle | escape }}</p>
      {%- endif -%}
    </article>
  {%- endif -%}
{%- endfor -%}