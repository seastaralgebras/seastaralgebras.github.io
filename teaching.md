---
layout: page
title: Teaching
permalink: /teaching
---

<ul>
	{% for course in site.teaching %}
	<li>
	{{ course.semester }} {{ course.year}}: <a href="{{ site.url }}{{ course.url }}/">{{ course.course_name }} ({{ course.course_number }})</a>
	</li>
	{% endfor %}
</ul>
