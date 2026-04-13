---
title: e.md Test page
description: A simple test about whether pages are rendered or not
---

<ul>
{%- for p in site.pages %}
<li>{{p.name}}
      {%- if p.content contains "#" %}
         unrendered
      {%- else %}
         rendered
      {%- endif %}
</li>
{%- endfor %}
</ul>
