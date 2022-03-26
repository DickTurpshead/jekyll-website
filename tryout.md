---
layout: default
title: tryout
example: This is an example value.
---

This page describes the amazing {{ site.title }} by {{ site.author.name }}.
{{ page.example }}

## About About Pages

The About page is a ...


## List of Animals

{% for animal in site.data.animals %}
- The {{ animal.name }} is a {{ animal.size }} animal.
{% endfor %}

## Large Animals are Better

{% for animal in site.data.animals %}
{% if animal.size == "large" %}- <strong style="color: {{ animal.color }};">{{ animal.name }}</strong>
{% else %}- <small>{{ animal.name }}</small>
{% endif %}
{% endfor %}

## List of Small Animals

{% assign small_animals = site.data.animals | where: "size", "small" %}
{% for animal in small_animals %}
- {{ animal.name | upcase }}
{% endfor %}
