---
layout: page
title: Projects
permalink: /projects.html
---

<ul>
	{% for project in site.projects %}
	{% if project.show %}
	<li>
	  <a href="{{ site.url }}{{ project.url }}.html">{{ project.title }}</a>:
	  {{ project.desc }}
	</li>
	{% endif %}
	{% endfor %}
</ul>
