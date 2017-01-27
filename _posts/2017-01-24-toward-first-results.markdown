---
layout: post
title:  "Toward First Results"
---

<!-- KaTeX -->
<link rel="stylesheet" href="/ducefd/ercblog/_site/public/katex.min.css">
<link rel="stylesheet" href="/ducefd/ercblog/_site/public/css/site.css">
<script src="/ducefd/ercblog/_site/public/katex.min.js"></script>
<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=AM_HTMLorMML-full"></script>
<!---<script src="/ducefd/ercblog/_site/public/ASCIIMathTeXImg.js"></script>--> 
<script src="/ducefd/ercblog/_site/public/ASCIIMathML.js"></script>
<script src="/ducefd/ercblog/_site/public/LaTeXMathML.js"></script>

{% raw %}
<!-- The Normal Distribution -->
<div class="equation" data-expr="\displaystyle P(x)=\frac{1}{\sigma\sqrt{2\pi}}e^{-\frac{(x-\mu)^2}{2\sigma ^2}}">
</div>
<!--{% endraw }-->

$$
\begin{align}
\sqrt{37} & = \sqrt{\frac{73^2-1}{12^2}} \\
 & = \sqrt{\frac{73^2}{12^2}\cdot\frac{73^2-1}{73^2}} \\ 
 & = \sqrt{\frac{73^2}{12^2}}\sqrt{\frac{73^2-1}{73^2}} \\
 & = \frac{73}{12}\sqrt{1 - \frac{1}{73^2}} \\ 
 & \approx \frac{73}{12}\left(1 - \frac{1}{2\cdot73^2}\right)
\end{align}
$$

<div>
``(1, 2)``
</div>

<div>
``o+``
``((a,b),(c,d))``
</div>

$$
o+
$$

Einstein's famous formula is

`E=mc^2`,

where `E` is energy, `m` is mass and `c` is the speed of light.
			
<script type="text/javascript">

    // grab all elements in DOM with the class 'equation'
    var tex = document.getElementsByClassName("equation");

    // for each element, render the expression attribute
    Array.prototype.forEach.call(tex, function(el) {
        katex.render(el.getAttribute("data-expr"), el);
    });
</script>
