---
layout: family_tree
title: Family Tree
---

{% assign family_tree = site.data.family_tree.family_trees %}
{% assign family_tree01 = site.data.family_tree01.family_trees %}

<h2>Family Tree</h2>
{% for family in family_tree %}
  {% include family_tree.html family=family %}
{% endfor %}

<h2>Family Tree01</h2>
{% for family in family_tree01 %}
  {% include family_tree.html family=family %}
{% endfor %}