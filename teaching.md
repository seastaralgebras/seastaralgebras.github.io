---
layout: page
title: Teaching
permalink: /teaching.html
---

Currently, I am a Lecturer at Rutgers University--New Brunswick and a Math Instructor at AoPS Academy Princeton.

## Current Teaching

<ul>
  {% for course in site.teaching %}
  {% if course.current %}
	<li>
	{% if course.link %}
	  <a href="{{ site.url }}{{ course.url }}.html">
	{% endif %}
	<b>{{ course.course_name }} ({{ course.course_number }})</b>
	{% if course.link %}
	  </a>
	{% endif %}
	<br>
	Term: {{ course.semester }} {{ course.year}}: 
	<br>
	Institution: {{ course.institution }}
	<br>
	Role: {{ course.position }}
	</li>
  {% endif %}
  {% endfor %}
</ul>

## Past Teaching
<ul>
	{% for course in site.teaching reversed %}
	{% unless course.current %}
	<li>
	{% if course.link %}
	  <a href="{{ site.url }}{{ course.url }}.html">
	{% endif %}
	<b>{{ course.course_name }} ({{ course.course_number }})</b>
	{% if course.link %}
	  </a>
	{% endif %}
	<br>
	Term: {{ course.semester }} {{ course.year}}: 
	<br>
	Institution: {{ course.institution }}
	<br>
	Role: {{ course.position }}
	</li>
	{% endunless %}
	{% endfor %}
</ul>
