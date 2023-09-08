---
layout: page
title: Teaching
permalink: /teaching.html
---

Currently, I am a Math Instructor at AoPS Academy Princeton, and a Part-Time Lecturer at Rutgers University -- New Brunswick.

## Current Teaching

<ul>
  {% for course in site.teaching %}
  {% if course.current %}
	<li>
	{{ course.semester }} {{ course.year}}: 
	{% if course.link %}
	  <a href="{{ site.url }}{{ course.url }}.html">
	{% endif %}
	{{ course.course_name }} ({{ course.course_number }})
	{% if course.link %}
	  </a>
	{% endif %}
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
	{{ course.semester }} {{ course.year}}: 
	{% if course.link %}
	  <a href="{{ site.url }}{{ course.url }}.html">
	{% endif %}
	{{ course.course_name }} ({{ course.course_number }})
	{% if course.link %}
	  </a>
	{% endif %}
	<br>
	Institution: {{ course.institution }}
	<br>
	Role: {{ course.position }}
	</li>
	{% endunless %}
	{% endfor %}
</ul>
