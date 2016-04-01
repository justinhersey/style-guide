---
title: Default Button
type: buttons
summary: Buttons are used for actions, like in forms, while textual hyperlinks are used for destinations, or moving from one page to another.
---

Use the `.flat` class for form actions and primary page actions. These are used extensively throughout the site.

When using a `<button>` element, always specify a type. When using a `<a>` element, always add `role="button"` for accessibility.

<button class="flat primary action" type="button">Button Button</button>
<a class="btn" href="#" role="button">Link button</a>

```
<button class="flat primary action" type="button">Button button</button>
<a class="flat primary action" href="#" role="button">Link button</a>
```
