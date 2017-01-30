---
layout: post
title:  "Toward First Results"

---
<link rel="stylesheet" href="/ducefd/ercblog/_site/public/css/site.css">

<!-- KaTeX -->

<link rel="stylesheet" href="/ducefd/ercblog/_site/public/katex.min.css">
<script src="/ducefd/ercblog/_site/public/katex.min.js"></script>


<b>Introduction</b>

The formula 
<dtex>V_{ex}\propto\int\left[\int\sin \theta_{ij}\frac{d\epsilon_{i}}{\epsilon_{\text{sum}}}\right]\frac{d\epsilon_{j}}{\epsilon_{\text{sum}}},</dtex>
was introduced by <citep>saevik</citep>. The variable <tex>V_{ex}</tex> is the <em>Excluded Volume</em> <citet>balberg,saevik</citet>. Other interesting formulas include
<dtex id='einstein'>E = mc^2,</dtex>
<dtex id='darcy'>\mathbf{u}=-K\left(\nabla p+\rho g\nabla z\right),</dtex>
where <eqref>einstein</eqref> is <a href="https://en.wikipedia.org/wiki/Mass%E2%80%93energy_equivalence">Einstein's famous formula</a>, and <eqref>darcy</eqref> is <a href="https://en.wikipedia.org/wiki/Darcy%27s_law">Darcy's law</a>.


| 1 | 2 | 2 | 4 |   |
|:-:|:-:|:-:|:-:|:-:|
|   |   |   | <ttex>kg/m^3</ttex>  |   |
|   |   |   |   |   |
|   |   |   |   |   |

<dtex id='einstein'>E = mc^2,</dtex>


<b>References</b>
<ol type="1" class ="references">

<li id="saevik" auth="Sævik et al." year="2013">Sævik, P. N., Berre, I., Jakobsen, M., & Lien, M. (2013). A 3D Computational Study of Effective Medium Methods Applied to Fractured Media. <em>Transport in Porous Media, 100</em>(1), 115–142. <a href="http://dx.doi.org/10.1007/s11242-013-0208-0">doi:10.1007/s11242-013-0208-0</a></li>

<li id="balberg" auth="Berkowitz and Balberg" year="1992">Berkowitz, B., & Balberg, I. (1992). Percolation approach to the problem of hydraulic conductivity in porous media. <em>Transport in Porous Media, 9</em>(3), 275–286. <a href="http://dx.doi.org/10.1007/BF00611971">doi:10.1007/BF00611971</a></li>
</ol>



<script>
	var txlist = document.getElementsByTagName("tex");
	for (var i = 0; i < txlist.length; i++) {
		var tx = txlist[i];
		var txtext = tx.textContent;
		katex.render(txtext, tx);
	}
	
	txlist = document.getElementsByTagName("citep");
	for (var i = 0; i < txlist.length; i++) {
		var tx = txlist[i];
		var citerefs = tx.textContent.split(",");
		var tags = "<a href='#" + citerefs[0] + "'></a>";
		for (var j = 1; j < citerefs.length; j++) {
			var citeref = citerefs[j];
			tags = tags + ", <a href='#" + citeref + "'></a>"
		}
		tx.innerHTML = tags;
	}
	
	txlist = document.getElementsByTagName("citet");
	for (var i = 0; i < txlist.length; i++) {
		var tx = txlist[i];
		var citerefs = tx.textContent.split(",");
		var tags = "(<a href='#" + citerefs[0] + "'>"+citeref+"</a>";
		for (var j = 1; j < citerefs.length; j++) {
			var citeref = citerefs[j];
			tags = tags + "; <a href='#" + citeref + "'>"+citeref+"</a>"
		}
		tags = tags + ")";
		tx.innerHTML = tags;
	}
	
	txlist = document.getElementsByTagName("eqref");
	for (var i = 0; i < txlist.length; i++) {
		var tx = txlist[i];
		tx.innerHTML = "(<a href='#" + tx.textContent + "'></a>)";
	}
	
	txlist = document.getElementsByTagName("dtex");
	for (var i = 0; i < txlist.length; i++) {
		var tx = txlist[i];
		var txtext = "\\displaystyle " + tx.textContent;
		var html = katex.renderToString(txtext, tx, { displayMode: true });
		tx.innerHTML = "<div class='katex-display'>" + html + "<span class=eqnum>(" + (i+1) + ")</span></div>";
		
		if (tx.id.length > 0) {
			var tx2list = document.querySelectorAll("a[href='#" + tx.id + "']")
			for (var j = 0; j < tx2list.length; j++) {
				tx2list[j].innerHTML = "" + (i+1);
			}
		}
		
	}
	
	txlist = document.getElementsByTagName("ttex");
	for (var i = 0; i < txlist.length; i++) {
		var tx = txlist[i];
		var txtext = "\\displaystyle " + tx.textContent;
		var html = katex.renderToString(txtext, tx, { displayMode: true });
		tx.innerHTML = "<span class='katex-display-table'>" + html + "</span>";
		
		if (tx.id.length > 0) {
			var tx2list = document.querySelectorAll("a[href='#" + tx.id + "']")
			for (var j = 0; j < tx2list.length; j++) {
				tx2list[j].innerHTML = "" + (i+1);
			}
		}
		
	}
	
	txlist = document.querySelectorAll(".references li");
	for (var i = 0; i < txlist.length; i++) {
		var tx = txlist[i];
		var tx2list = document.querySelectorAll("citep a[href='#" + tx.id + "']")
		for (var j = 0; j < tx2list.length; j++) {
			tx2list[j].innerHTML = "[" + (i+1) + "]";
			var str = tx.getAttribute("auth") + " (" + tx.getAttribute("year") + ")";
			tx2list[j].innerHTML = str;
		}
		var tx2list = document.querySelectorAll("citet a[href='#" + tx.id + "']")
		for (var j = 0; j < tx2list.length; j++) {
			tx2list[j].innerHTML = "[" + (i+1) + "]";
			var str = tx.getAttribute("auth") + ", " + tx.getAttribute("year");
			tx2list[j].innerHTML = str;
		}
	}
</script>

<!--{% raw %}-->
<!-- The Normal Distribution -->
<!--<div class="equation" data-expr="\displaystyle P(x)=\frac{1}{\sigma\sqrt{2\pi}}e^{-\frac{(x-\mu)^2}{2\sigma ^2}}">
</div>-->
<!--{% endraw }-->

<!--<script type="text/javascript">

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
    
</script>-->
