---
layout: family_tree
title: Family Trees
---

{% assign family_tree = site.data.family_tree %}
{% assign family_tree01 = site.data.family_tree01 %}

<h2>Family Tree</h2>
{% for family in family_tree.family_trees %}
  {% include family_tree.html data=family %}
{% endfor %}

<h2>Family Tree01</h2>
{% for family in family_tree01.family_trees %}
  {% include family_tree.html data=family %}
{% endfor %}