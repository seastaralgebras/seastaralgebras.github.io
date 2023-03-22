---
layout: project
title: Mandelbrot Set
desc: >
  Generated an image approximating the Mandelbrot set
link: #"https://github.com/seastaralgebras/mandelbrot"
---
## Python
<img src="{{ site.url }}/assets/images/mandelbrot_2000px_1000steps.png" width="50%">


## Javascript

<canvas id="mandelbrot" width="500" height="500" style="border:1px solid #000000"></canvas>
<br>
<button onclick="drawMandelbrot(canvas)">Draw Mandelbrot set!</button>


<script>
    var canvas = document.getElementById("mandelbrot");
    // drawMandelbrot(canvas);
</script>
