---
layout: default
title: Family Trees
---

{% assign family_tree01 = site.data.family_tree01.family_trees %}
{% assign family_tree02 = site.data.family_tree02.family_trees %}

## Family Tree01

<ul>
  {% for family in family_tree01 %}
    <li>Debug: {{ family.name | default: "No name" }}</li>
    {% include family_tree.html data=family %}
  {% endfor %}
</ul>

## Family Tree02

<ul>
  {% for family in family_tree02 %}
    <li>Debug: {{ family.name | default: "No name" }}</li>
    {% include family_tree.html data=family %}
  {% endfor %}
</ul>