---
layout: post
title:  "Toward First Results"
---

<!-- KaTeX -->
<link rel="stylesheet" href="/ducefd/ercblog/_site/public/katex.min.css">
<link rel="stylesheet" href="/ducefd/ercblog/_site/public/css/site.css">
<script src="/ducefd/ercblog/_site/public/katex.min.js"></script>
<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=AM_HTMLorMML-full"></script>
<script src="/ducefd/ercblog/_site/public/ASCIIMathTeXImg.js"></script>

{% raw %}
<!-- The Normal Distribution -->
<div class="equation" data-expr="\displaystyle P(x)=\frac{1}{\sigma\sqrt{2\pi}}e^{-\frac{(x-\mu)^2}{2\sigma ^2}}">
</div>
<!--{% endraw }-->


<b>Instructions for entering ASCIIMath</b>
<div>

Use the <b>backtick</b> character before and after math 

Enter fractions with a forward slash, /, as in `y/z`.

Products and powers of variables: `ab^2`.

Integrals: `int_(0)^(2 pi) sin\ x\ dx = 0`.

Square root is like this: `sqrt(169) = 13`.

Summation notation: `sum_(i=1)^ni^3` 

`3xx3` matrix: `[(1,2,3),(4,8,3),(-5,4,9)]`

Greek, too: `A = pi r^2`

<b>Special note:</b>

When using "less than" or "greater than" signs, put a SPACE before and after them, like this: 

If `x < 3`, then `y > 0`.

</div>
			
<script type="text/javascript">

    // grab all elements in DOM with the class 'equation'
    var tex = document.getElementsByClassName("equation");

    // for each element, render the expression attribute
    Array.prototype.forEach.call(tex, function(el) {
        katex.render(el.getAttribute("data-expr"), el);
    });
</script>
