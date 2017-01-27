---
layout: post
title:  "Toward First Results"
---

<!-- KaTeX -->
<link rel="stylesheet" href="/ducefd/ercblog/_site/public/katex.min.css">
<link rel="stylesheet" href="/ducefd/ercblog/_site/public/css/site.css">
<script src="/ducefd/ercblog/_site/public/katex.min.js"></script>
<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=AM_HTMLorMML-full"></script>

{% raw %}
<!-- The Normal Distribution -->
<div class="equation" data-expr="\displaystyle P(x)=\frac{1}{\sigma\sqrt{2\pi}}e^{-\frac{(x-\mu)^2}{2\sigma ^2}}">
</div>
<!--{% endraw }-->

			
<script type="text/javascript">

    // grab all elements in DOM with the class 'equation'
    var tex = document.getElementsByClassName("equation");

    // for each element, render the expression attribute
    Array.prototype.forEach.call(tex, function(el) {
        katex.render(el.getAttribute("data-expr"), el);
    });
</script>
