---
layout: page
title: Components
---

Components make up most of our reusable elements.

{% assign components = site.components | group_by:"type" %}
{% for component in components %}
<h2 id="guide-{{ component.name }}" class="cf">{{ component.name | capitalize }}</h2>
{% for entry in component.items %}
{% include component.html %}
{% endfor %}
{% endfor %}

{% for buttons in site.components %}
  {{ buttons }}
{% endfor %}

## Disabled state

<button class="flat primary action" type="button" disabled>Disabled button</button>
<a class="flat primary action disabled" href="#" role="button">Disabled button</a>

```
<button class="flat primary action" type="button" disabled>Disabled button</button>
<a class="flat primary action disabled" href="#" role="button">Disabled button</a>
```

## Button Groups

Button groups are used for multiple buttons where each action compliments the other.

<div class="button-group">
    <button class="flat primary" type="button">Button button</button>
    <button class="flat primary action" type="button">Button button</button>
</div>

```
<div class="button-group">
    <button class="flat" type="button">Button button</button>
    <button class="flat" type="button">Button button</button>
</div>
```
