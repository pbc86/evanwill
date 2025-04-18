---
layout: dark
title: About
example: This is an example value.
---

This page describes the amazing {{ site.title }} by {{ site.author.name }}.
{{ page.example }}

{% include big-cat.html %}

Some Markdown contents describing your site.

<h2> About About Pages </h2>

The About page is a common convention found on websites.

It is your opportunity to let us know all the details "about" your project:

- focus and topic area
- people involved
- code and projects used.

## List of Animals

{% for animal in site.data.animal %}
- The {{ animal.name }} is a {{ animal.size }} animal.
{% endfor %}

## Large Animals are Better

{% for animal in site.data.animal %}
{% if animal.size == "large" %}- <strong style="color: {{ animal.color }};">{{ animal.name }}</strong>
{% else %}- <small>{{ animal.name }}</small>
{% endif %}
{% endfor %}

## List of Small Animals

{% assign small_animals = site.data.animal | where: "size", "small" %}
{% for animal in small_animals %}
- {{ animal.name | upcase }}
{% endfor %}
