---
layout: post
title:  "Toward First Results"
---

<link rel="stylesheet" href="/ducefd/ercblog/_site/public/css/site.css">

<script type="text/x-mathjax-config">
  window.MathJax.Hub.Config({
    skipStartupTypeset: true,
    displayAlign: 'left',
    extensions: ['MatchWebFonts.js'],
    TeX: {
      extensions: ['cancel.js', 'enclose.js']
    }
  });
</script>
<script src="//cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>

<!-- KaTeX -->

<link rel="stylesheet" href="/ducefd/ercblog/_site/public/katex.min.css">
<script src="/ducefd/ercblog/_site/public/katex.min.js"></script>

{% raw %}
<!-- The Normal Distribution -->
<div class="equation" data-expr="\displaystyle P(x)=\frac{1}{\sigma\sqrt{2\pi}}e^{-\frac{(x-\mu)^2}{2\sigma ^2}}">
</div>
<!--{% endraw }-->

			

<!--{% raw %}-->
<!-- The Normal Distribution -->
<!--<div class="equation" data-expr="\displaystyle P(x)=\frac{1}{\sigma\sqrt{2\pi}}e^{-\frac{(x-\mu)^2}{2\sigma ^2}}">
</div>-->
<!--{% endraw }-->

<b>KaTeX with MAthJAx fallback</b>

<span class="maths">c = \sqrt{a^2 + b^2}</span>
<p class="maths">J_\alpha(x) = \sum\limits_{m=0}^\infty\frac{(-1)^m}{m! \, \Gamma(m + \alpha + 1)}{\bigl({\frac{x}{2}}\bigr)}^{2 m + \alpha}</p>
			
<script type="text/javascript">

	// grab all elements in DOM with the class 'equation'
    //var tex = document.getElementsByClassName("equation");

    // for each element, render the expression attribute
    //Array.prototype.forEach.call(tex, function(el) {
    //    katex.render(el.getAttribute("data-expr"), el);
    //});
	
	function render(el) {
		  'use strict';

		  var isBlock = window.getComputedStyle(el).display === 'block';
		  var latex = el.textContent;

		  el.setAttribute('data-maths', latex);

		  try {
			el.classList.add('katex-rendered');
			window.katex.render(latex, el, { displayMode: isBlock });
		  } catch(e) {
			el.textContent = '\\' + (isBlock ? '[' : '(') + latex + '\\' + (isBlock ? ']' : ')');
			el.classList.add('mathjax-rendered');
			window.MathJax.Hub.Queue(['Typeset', MathJax.Hub, el]);
		  }
	}

	Array.prototype.slice.call(document.querySelectorAll('.maths')).forEach(function(el) {
		render(el);
	});
    
</script>
