---
layout: course
title: Classical Mechanics II
permalink: /cm-II/
---

Welcome to Classical Mechanics II. This course will expand on the ideas of Classical Mechanics I by talking about mechanics of many particle systems.

The prerequisites are as follows:
1. A working knowledge of classical mechanics I
2. A working knowledge of ordinary differential equations

{% assign unitNames = "Unit 1 - Vectors#Unit 2 - Kinematics on the Line#Unit 3 - Dynamics on the Line#Unit 4 - Momentum#Unit 5 - Circular Motion#Supplementary Material" | split: '#' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/, unit5/, supplements/" | split: ', ' %}

{% assign lessonNames1 = "" | split: ', ' %}

{% assign lessonNames2 = "Displacement,_Time,_and_Velocity#Instantaneous Velocity#Average and Instantaneous Acceleration#Motion with Constant Acceleration#Freely Falling Bodies#Velocity and Position by Integration" | split: '#' %}

{% assign lessonNames3 = "" | split: ', ' %}

{% assign lessonNames4 = "" | split: ', ' %}

{% assign lessonNames5 = "" | split: ', ' %}

{% assign lessonNames6 = "" | split: ', ' %}

<ul>
{% for unitName in unitNames %}
{% assign unitLink = page.permalink | append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> {{unitName}} </a> </li>
<ol> {%assign unitIndex = forloop.index0 %}
{% if unitIndex == 0 %} {% assign lessonNames = lessonNames1 %}
{% elsif unitIndex== 1 %}  {% assign lessonNames = lessonNames2 %}
{% elsif unitIndex == 2 %}  {% assign lessonNames = lessonNames3 %}
{% elsif unitIndex == 3 %}  {% assign lessonNames = lessonNames4 %}
{% endif %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
{% endfor %}
</ul>

**Sources**

1. Calculus, 7 ed. - Stewart, James (2012)
2. Vector Analysis - Spiegel, Murray R. (1959)
3. Differential Geometry of Curves and Surfaces - 2 ed. do Carmo, Manfredo (2016)
4. Calculus on Manifolds - Spivak, Michael (1965)
