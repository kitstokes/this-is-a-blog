---
layout: dark
title: About
example: penguin text
---

This page describes the astonishing staggering stunning {{ site.title }} by {{ site.author.name }}.
{{ page.example }}

{% include big-cat.html %}

## An Incredible New Blog

This is it. 

{% for animal in site.data.animals %}
- The {{ animal.name }} is a {{ animal.size }} animal.
{% endfor %}

## Large animals are bigger!

{% for animal in site.data.animals %}
{% if animal.size == "large" %}- <strong style."color: {{ animal.color }};">{{ animal.name }}</strong>
{% else %}- <small>{{ animal.name }}</small>
{% endif %}
{% endfor %}

## Small animals only

{% assign small_animals = site.data.animals | where: "size", "small" %}
{% for animal in small_animals %}
- {{ animal.name | upcase }}
{% endfor %}
