---
layout: page
title: Projects
permalink: /projects.html
---

{% for project in site.projects %}
{% if project.show %}
- [{{ project.title }}]({{ site.url }}{{ project.url }}.html):
  {{ project.desc }}
{% endif %}
{% endfor %}
