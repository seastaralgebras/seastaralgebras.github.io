---
layout: page
title: Projects
permalink: /projects.html
---

<ul>
	{% for project in site.projects %}
	<li>
	  <a href="{{ site.url }}{{ project.url }}.html">{{ project.title }}</a>:
	  {{ project.desc }}
	</li>
	{% endfor %}
</ul>
