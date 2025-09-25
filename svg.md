---
layout: page
title: "SVG"
permalink: /SVG/
---

<svg width="100" height="100" viewBox="0 0 100 100">
  <circle cx="50" cy="50" r="40" fill="skyblue"
          style="animation:pulse 2s infinite"/>
</svg>

<style>
@keyframes pulse {
  0%   { fill: skyblue; }
  50%  { fill: steelblue; }
  100% { fill: skyblue; }
}
</style>

<svg width="400" height="300" viewBox="0 0 400 300">

  <!-- Parent 1 -->
  <circle cx="150" cy="80" r="25" fill="skyblue" stroke="black" stroke-width="2">
    <!-- Pulse effect -->
    <animate attributeName="r" values="25;28;25" dur="3s" repeatCount="indefinite"/>
  </circle>
  <text x="150" y="85" font-size="10" text-anchor="middle">Parent A</text>

  <!-- Parent 2 -->
  <circle cx="250" cy="80" r="25" fill="pink" stroke="black" stroke-width="2">
    <!-- Pulse effect -->
    <animate attributeName="r" values="25;28;25" dur="3s" begin="1s" repeatCount="indefinite"/>
  </circle>
  <text x="250" y="85" font-size="10" text-anchor="middle">Parent B</text>

  <!-- Connector line between parents -->
  <line x1="175" y1="80" x2="225" y2="80" stroke="black" stroke-width="2">
    <!-- Flicker highlight -->
    <animate attributeName="stroke-width" values="2;4;2" dur="4s" repeatCount="indefinite"/>
  </line>

  <!-- Child -->
  <circle cx="200" cy="180" r="25" fill="lightgreen" stroke="black" stroke-width="2">
    <!-- Bounce animation -->
    <animateTransform attributeName="transform" type="translate"
      values="0,0; 0,5; 0,0" dur="2s" repeatCount="indefinite"/>
  </circle>
  <text x="200" y="185" font-size="10" text-anchor="middle">Child</text>

  <!-- Lines from parents to child -->
  <line x1="150" y1="105" x2="200" y2="155" stroke="black" stroke-width="2"/>
  <line x1="250" y1="105" x2="200" y2="155" stroke="black" stroke-width="2"/>

</svg>