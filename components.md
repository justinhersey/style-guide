---
layout: page
title: Components
---

Components make up most of our reusable elements.

{% assign components = site.components | group_by:"type" %}

<nav id="component-selector" class="wrap">
  <select name="section" id="component-select">
    <option value>Jump to component...</option>
    {% for component in components %}
    <optgroup label="{{ component.name | capitalize }}">
    {% for entry in component.items %}
    <option value="#guide-{{ entry.title | slugify }}">{{ entry.title }}</option>
    {% endfor %}
    </optgroup>
    {% endfor %}
  </select>
</nav>

<!-- component selector option list -->
<script>    
  (function (document, undefined) {
    // component selector
    document.getElementById('component-select').onchange = function() {
      //document.location=this.options[this.selectedIndex].value;
      var val = this.value;
      if (val !== "") {
        window.location = val;
      }
    }
  })(document);
</script>

{% for component in components %}
<h1 id="guide-{{ component.name }}" class="cf">{{ component.name | capitalize }}</h1>
{% for entry in component.items %}
<h2 id="guide-{{ entry.title | slugify }}">{{ entry.title }}</h2>
{% if entry.summary %}{{ entry.summary }}{% endif %}
{% if entry.content %}{{ entry.content }}{% endif %}
{% endfor %}
{% endfor %}
