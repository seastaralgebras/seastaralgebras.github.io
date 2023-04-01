---
layout: project
show: true
title: Math Visualizations
proj-collection: site.math-visualizations
desc: >
  Images, animations, and other things that visually represent various constructs in math.
link: #"https://github.com/seastaralgebras/"
---

Mathematics is full of cool visuals, and I couldn't help but code a few of them into existence.

{% for project in site.math-visualizations %}
  {% include project-preview.html %}
{% endfor %}
