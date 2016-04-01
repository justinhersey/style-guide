---
layout: page
title: Components
---

Components make up most of our reusable elements.

{% assign components = site.components | group_by:"type" %}
{% for component in components %}
<h1 id="guide-{{ component.name }}" class="cf">{{ component.name | capitalize }}</h1>
{% for entry in component.items %}
## {{ entry.title }}
{% if entry.summary %}{{ entry.summary }}{% endif %}
{{ entry.content }}
{% endfor %}
{% endfor %}
