---
layout: post
title:  "Fractals are cool, actually (not that anybody was disputing it)."
author: Karuna Sangam
date:   2023-04-22 12:45:00 -0400
tags: math fractals coding projects
categories: math
---








We look at the family of Julia sets \\(f \colon \mathbb{C} \to \mathbb{C}\\) defined by \\(f_c(z) = z^2+c\\), parametrized by the complex number <var>c</var>.

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

<canvas id="mandelbrot" width="500" height="500" stype="border:1px solid #000000;">
Canvas element for drawing Mandelbrot set.</canvas>
<br>
<button onclick="drawMandelbrot(mandelbrot_pic)">Draw Mandelbrot set!</button>
</div>

<div class="js_container">
<p>The following is a Javascript program that will generate a Julia set with \(c = x + i y \) given by the specified real and imaginary parts when you press the button labeled "Draw Julia set!"</p>

<canvas id="julia" width="500" height="500" stype="border:1px solid #000000;">
Canvas element for drawing Julia set with given parameter.</canvas>

<form id="julia_point">
    <var>x</var>: <input id="tiny_form" type="number" name="real_c" value="0.0" step="0.001" min="-2.1" max="2.1">
    &nbsp;
    <var>y</var>: <input id="tiny_form" type="number" name="imag_c" value="0.0" step="0.001" min="-2.1" max="2.1">
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
