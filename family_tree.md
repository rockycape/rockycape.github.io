---
layout: family_tree
title: Family Trees
---

{% assign family_tree01 = site.data.family_tree01.family_trees %}
{% assign family_tree02 = site.data.family_tree02.family_trees %}

<h2>Family Tree01</h2>
<ul>
  {% for family in family_tree01 %}
    {% include family_tree.html data=family %}
  {% endfor %}
</ul>

<h2>Family Tree02</h2>
<ul>
  {% for family in family_tree02 %}
    {% include family_tree.html data=family %}
  {% endfor %}
</ul>
