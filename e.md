---
title: e.md Test page
description: A simple test about whether pages are rendered or not
---

{%- for p in site.pages %}
<p>{{p.name}}
      {%- if p.content contains "#" %}
         unrendered
      {%- else %}
         rendered
      {%- endif %}
</p>
{%- endfor %}
