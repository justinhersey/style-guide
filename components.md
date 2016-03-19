---
layout: page
title: Components
---
{% for buttons in site.components %}
  {{ buttons }}
{% endfor %}

Buttons are used for actions, like in forms, while textual hyperlinks are used for destinations, or moving from one page to another.

## Default Buttons

Use the `.flat` class for form actions and primary page actions. These are used extensively throughout the site.

When using a `<button>` element, always specify a type. When using a `<a>` element, always add `role="button"` for accessibility.

<button class="flat primary action" type="button">Button Button</button>
<a class="btn" href="#" role="button">Link button</a>

```
<button class="flat primary action" type="button">Button button</button>
<a class="flat primary action" href="#" role="button">Link button</a>
```

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
