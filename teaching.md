---
layout: page
title: Teaching
permalink: /teaching.html
---

<ul>
	{% for course in site.teaching %}
	<li>
	{{ course.semester }} {{ course.year}}: <a href="{{ site.url }}{{ course.url }}.html">{{ course.course_name }} ({{ course.course_number }})</a>
	</li>
	{% endfor %}
</ul>
