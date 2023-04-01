---
layout: project
show: true
title: Mandelbrot Set
image: assets/images/mandelbrot_2000px_1000steps.png
image-desc: "A black and white image of the Mandelbrot set, where points have been shaded according to how many iterations it takes for them to exceed some threshold. The threshold can be any number greater than 2."
desc: >
    Generated an image approximating the Mandelbrot set.
link: "https://github.com/seastaralgebras/mandelbrot"
---

Some python and javascript code generating the Mandelbrot set and \\( z^2 + c \\) Julia sets.


## Python

<img src="{{ site.url }}/assets/images/mandelbrot_and_julia.png" width="500" max-width="100%">

## Javascript


<script>
    var mathjs_script = document.createElement('script');
    mathjs_script.type = 'text/javascript';
    mathjs_script.src = 'https://unpkg.com/mathjs@11.7.0/lib/browser/math.js'
    var mandy_script = document.createElement('script');
    mandy_script.type = 'text/javascript';
    mandy_script.src = '/assets/js/mandelbrot.js';
    document.head.appendChild(mathjs_script);
    document.head.appendChild(mandy_script);
</script>

<div class="js_container">
<p>The following is a Javascript program that will generate a Mandelbrot set when you press the button labeled "Draw Mandelbrot set!"</p>

<canvas id="mandelbrot" width="500" height="500" stype="border:1px solid #000000;"></canvas>
<br>
<button onclick="drawMandelbrot(mandelbrot_pic)">Draw Mandelbrot set!</button>
</div>

<div class="js_container">
<p>The following is a Javascript program that will generate a Julia set with c given by the specified real and imaginary parts when you press the button labeled "Draw Julia set!"</p>

<canvas id="julia" width="500" height="500" stype="border:1px solid #000000;"></canvas>

<form id="julia_point">
    Real: <input id="tiny_form" type="number" name="real_c" value="0.0" step="0.001" min="-2.1" max="2.1">
    <br>
    Imaginary: <input id="tiny_form" type="number" name="imag_c" value="0.0" step="0.001" min="-2.1" max="2.1">
</form> 
<button onclick="julia_start()">Draw Julia set!</button>
</div>

<script>
    var mandelbrot_pic = document.getElementById("mandelbrot");
    var julia_pic = document.getElementById("julia");

    function julia_start() {
      var z = document.getElementById("julia_point");
      var x;
      var y;
      x = z.real_c.value;
      y = z.imag_c.value;
      drawJulia(julia_pic, x, y);
    }
    
</script>
