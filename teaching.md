---
layout: page
title: Teaching
permalink: /teaching.html
---
## Current Teaching

I currently work as a tutor in the Math Help Center at Rutgers, a drop-in tutoring center that serves students taking undergraduate math courses -- primarily students in 100- and 200-level courses, but occasionally those in upper division undergraduate math courses.

## Past Teaching
<ul>
	{% for course in site.teaching %}
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
	{% endfor %}
</ul>
