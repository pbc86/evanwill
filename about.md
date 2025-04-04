---
layout: dark
title: About
example: this is an example value
---

This page describes the amazing {{ site.title }} by {{ site.author.name }}.
{{ page.example }}

{% include big-cat.html %}

{% for animal in site.data.animals %}
- The {{ animal.name }} is a {{ animal.size }} animal.
{% endfor %}

Some Markdown contents describing your site.

## About About Pages

The About page is a common convention found on websites.

It is your opportunity to let us know all the details "about" your project:

- focus and topic area
- people involved
- code and projects used.
