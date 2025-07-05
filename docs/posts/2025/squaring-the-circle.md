# 99.9…% of Geometers Cannot Solve This Problem!

<link rel="stylesheet" type="text/css" href="https://tikzjax.com/v1/fonts.css">
<script src="https://tikzjax.com/v1/tikzjax.js"></script>

<header>Jul 5, 2025</header>
<br>
<hr>

This article served as the script for [my SoME 4 submission](https://youtu.be/qRfVGjqlkJ8), and it was written in collaboration with Tatiana Elokhin; a Spanish version is also available [here](../../files/2025/squaring-the-circle-spanish.pdf).

<hr>

Let's get straight to the point: consider a circle of radius one, and, using only a ruler and a compass, I want you to construct a square of the same area. Make sure to try as hard as you can... Done? Well, whatever you've done is **wrong**, and it's because this was a trick question -- as you may have inferred from the title --, since I've just presented you with the millenary and impossible problem of "squaring the circle"; this article is precisely about it because, as we'll see, it manages to distill a great extent of the history of mathematics within its statement.

# The dawn of mathematics

Have you ever wondered where numbers come from? I don't mean the metaphysical question of the origin of ideas, of whether theorems are invented or discovered, but something rather more tangible as the history of this discipline. Where does math as a science come from?

Precisely from trying to quantify certain aspects of the daily and commercial life (it suffices to see that geometry literally meant "land measurement"); it's quite convenient to know that one owns exactly \\(124.25\mathrm{m}^2\\) of land in which to plant crops, or that if you have sold 12 bottles of oil at 5 coins each, you've made a total of 60 coins. Thus, primordial mathematics had an entirely pragmatic purpose. This is reflected in the fact that the earliest cultures had formulas or "recipes" they simply followed without caring for an actual proof; for example, the Babylonians estimated the area of a circle as \\(3r^2\\), which officially makes them the first engineers in history (even though they didn't find that \\(e=\\sqrt{g}\\)).

Nonetheless, it was the Greek civilization that provoked a paradigm change (to a great extent, thanks to Thales of Miletus); the cult of reason that was cultivated in the Hellenic region meant rejecting those mechanical procedures built upon sole evidence, and thus the sought for flawless proofs. Think now of all the mathematical knowledge as some sort of tree, where each leaf is a result that depends on many others; if we keep going further down, we'll eventually reach its roots. Because from nothing, nothing comes, some truths will have to be assumed, and for today's main characters those were the ever-so-simple *line* and *circle*, that's why rigorous classic mathematics is confined solely to constructions with ruler and compass, and that's also why the problem of today turns out to be impossible.

# Squaring the circle

You know what the ancient Greeks were very good at? Proportion. If you gave them two distinct figures, and they could -- using their beloved ruler and compass -- turn them into squares, you can bet they would flawlessly compare their two areas.

Now, which figures can be reduced to squares through the aforementioned method? Evidently triangles, and since we can divide any polygon into triangles, any polygon can be transformed into a square employing a ruler and a compass. What if the area is curved? That's not certain at all. Hippocrates shed some light on the matter and gave hope to mathematicians when he squared a lune, but something as fundamental as the circle itself -- recall that it was one of the two basic shapes -- was really getting to them. Thus, squaring the circle became the classic problem par excellence, along with trisecting an angle and doubling a cube, since it being solved would imply measuring with utter precision the area of the most important shape.

<div class="problem">Can a circle be transformed into a square of equal area using only a ruler and a compass?</div>

<br>

It's important to mention that we told a white lie above; Greek rulers weren't as fancy as those we use today either (they didn't have marks indicating certain lengths), but they were more like a straight edge, only useful to trace lines. Let's see now the tools ancient geometers had in their arsenal when dealing with operations:

* Firstly, if they had two segments of lengths \\(a\\) and \\(b\\), they could join them and produce one measuring their sum:

<div align="center">
<script type="text/tikz">
        \begin{tikzpicture}
            \node[circle,fill, inner sep=1pt, white] at (0, 0) {};
            \node[circle,fill, inner sep=1pt, white] at (2.5, 0) {};
            \draw[color=white] (0, 0) -- (2.5, 0);
            \node[color=white] at (1.25, 0.25) {$a$};
            \node[circle,fill, inner sep=1pt, white] at (4, 0) {};
            \node[circle,fill, inner sep=1pt, white] at (5, 0) {};
            \draw[color=white] (4, 0) -- (5, 0);
            \node[color=white] at (4.5, 0.25) {$b$};
            \draw[-Stealth, color=white] (6.5, 0) -- (7.5, 0);
            \node[circle,fill, inner sep=1pt, color=red] at (9, 0) {};
            \node[circle,fill, inner sep=1pt, color=red] at (11.5, 0) {};
            \node[circle,fill, inner sep=1pt, color=red] at (12.5, 0) {};
            \draw[color=red] (9, 0) -- (12.5, 0);
            \node[color=red] at (10.75, 0.25) {$a+b$};
        \end{tikzpicture}
</script>
</div>

* Likewise, if we put the smaller segment at the end of the larger, we can find their difference:

<div align="center">
<script type="text/tikz">
        \begin{tikzpicture}
            \node[circle,fill, inner sep=1pt, white] at (0, 0) {};
            \node[circle,fill, inner sep=1pt, white] at (2.5, 0) {};
            \draw[color=white] (0, 0) -- (2.5, 0);
            \node[color=white] at (1.25, 0.25) {$a$};
            \node[circle,fill, inner sep=1pt, white] at (4, 0) {};
            \node[circle,fill, inner sep=1pt, white] at (5, 0) {};
            \draw[color=white] (4, 0) -- (5, 0);
            \node[color=white] at (4.5, 0.25) {$b$};
            \draw[-Stealth, color=white] (6.5, 0) -- (7.5, 0);
            \draw[color=red] (9, 0) -- (10.5, 0);
            \draw[color=white] (10.5, 0) -- (11.5, 0);
            \node[circle,fill, inner sep=1pt, color=red] at (9, 0) {};
            \node[circle,fill, inner sep=1pt, color=red] at (10.5, 0) {};
            \node[circle,fill, inner sep=1pt, white] at (11.5, 0) {};
            \node[color=red] at (9.75, 0.25) {$a-b$};
        \end{tikzpicture}
</script>
</div>

* Using triangle congruences, we can also construct the product of \\(a\\) and \\(b\\):

<div align="center">
<script type="text/tikz">
\begin{tikzpicture}
            \draw[white] (0, 0) -- (1, 0);
            \draw[white] (1, 0) -- (1, 1.5);
            % \draw (0, 0) -- (1, 1.5);

            \draw[white] (1, 0) -- (2, 0);
            \draw[white] (2, 0) -- (2, 3);
            \draw[red] (0, 0) -- (2, 3);

            \node[color=red] at (1, 2) {$ab$};
            \node[white] at (0.25, 0.75) {$a$};
            \node[white] at (0.65, 0.25) {1};
            \node[white] at (1, -0.25) {$b$};
        \end{tikzpicture}
</script>
</div>

* And, analogously, the quotient \\(a\\) over \\(b\\):

<div align="center">
<script type="text/tikz">
        \begin{tikzpicture}
            \draw[color=white] (0, 0) -- (1, 0);
            \draw[color=white] (1, 0) -- (1, 1.5);
            \draw[red] (0, 0) -- (1, 1.5);

            \draw[color=white] (1, 0) -- (2, 0);
            \draw[color=white] (2, 0) -- (2, 3);
            \draw[color=white] (1, 1.5) -- (2, 3);

            \node[color=white] at (1, 2) {$a$};
            \node[color=red] at (0, 0.75) {$a / b$};
            \node[color=white] at (0.65, 0.25) {1};
            \node[color=white] at (1, -0.25) {$b$};
        \end{tikzpicture}
</script>
</div>

* Finally, by making a circumference of diameter \\(a+1\\) we can find \\(\\sqrt a\\):

<div align="center">
<script type="text/tikz">
        \begin{tikzpicture}
            \draw[color=white] (0, 0) -- (4, 0);
            \draw[color=white] (4, 0) -- (5, 0);
            \node[circle,fill, inner sep=1pt, color=white] at (0, 0) {};
            \node[circle,fill, inner sep=1pt, color=red] at (4, 0) {};
            \node[color=white] at (2, 0.25) {$a$};
            \node[circle,fill, inner sep=1pt, color=white] at (5, 0) {};
            \node[color=white] at (4.5, 0.25) {1};
            \draw[color=white] (5, 0) arc (0:180:2.5);
            \node[circle,fill, inner sep=1pt, color=red] at (4, 2) {};
            \draw[color=red] (4, 0) -- (4, 2);
            \node[color=red] at (3.5, 1) {$\sqrt{a}$};
        \end{tikzpicture}
</script>
</div>

Greek arithmetic was thus reduced to these scarce operations, and all numbers that could be obtained from them are called *constructible*, because they can indeed be constructed with ruler and compass.

Let's go back to our problem, and consider the case when the radius is one (any other is equivalent after scaling down and then rescaling the final solution), that would mean that in order to square that circle we would need a square of side \\(\\sqrt\\pi\\), but since we have no problem at all in taking square roots, squaring the circle is possible if and only if \\(\\pi\\) is a constructible number.

<div class="problem"> Can \(\pi\) be expressed as a combination of sums, subtractions, products, divisions, and square roots applied to integer numbers?</div>

<br>

Thus, we have converted an entirely geometric scenario into an algebraic one, which would have to wait millennia to finally be solved.

# The solution

Jumping straight into a proof would not only be unsatisfactory, but also disrespectful towards the arduous work of the mathematical community through that period; it would obviate, as we've already said, a couple millennia of history.

Not for anything did it become the obsession of uncountable mathematicians, from hobbyists to professionals, some of which to this day keep sending wrong constructions to universities all across the world. It is such the popularity of this problem that is has become a synonym for impossibility and made its way into the pop culture to appear in news, songs, books and even in Dante's *Divine Comedy*:

> What is the geometrician who fixes himself entirely

> on measuring the circle, and does not find, by thinking,

> that principle from which he needs,[...]

The most important discoveries in this field set off with Archimedes' study of the circle and his estimation of the number \\(\\pi\\), but it was undoubtedly the introduction of the coordinate plane by René Descartes the most important insight towards the final solution, because through him mathematicians could then describe geometric figures as algebraic equations. The final bit was authored by Ferdinand von Lindemann, who actually proved a stronger claim.

An algebraic number is one that can be written as the solution of a polynomial equation with integer coefficients; notice that every constructible number is also algebraic, so if it isn't algebraic, it won't be constructible either. What Lindemann really proved was that if a given \\(\\alpha\\) is algebraic, then \\(e^\\alpha\\) isn't, and thus our problem falls as a corollary:

<div class="theorem">A circle can't be squared using only ruler and compass.</div>
<div class="proof">

Let's suppose the circle <em>can</em> be squared, and thus \(\pi\) is constructible and algebraic. The imaginary unit is too, since it is a solution to \(x^2 + 1 = 0\), then evidently \(i\pi\) is algebraic as well. Therefore, by Lindemann's theorem, \(e^{i\pi} = -1\) shouldn't be, but this is a contradiction because \(-1\) is clearly algebraic, hence our assumption was wrong and \(\pi\) is neither algebraic nor constructible.

</div>

Numbers that are not algebraic are called *transcendental*, a name which encapsulates the importance of this problem for the history of this discipline. After all, the enigma that drove mathematicians crazy turned out to be impossible.

# How to actually square the circle

But remember once again the rules of this game, ruler and compass. If we relax them and allow other utensils and procedures, then of course, one can square the circle. To sum up, here's one of such constructions:

We start from a circle of radius \\(r\\), thus area \\(\\pi r^2\\). Let's roll it in such a way that its circumference (\\(2\\pi r\\)) is now a segment, which we'll divide in half and add \\(r\\) afterwards to form the diameter of a semicircle, on which we'll trace a height \\(h\\) in the point connecting \\(\\pi r\\) and \\(r\\) and then form three right triangles:

<div align="center">
<script type="text/tikz">
    \begin{tikzpicture}[scale=1.2073]
        \draw[color=white] (0, 0) -- (3.1416, 0);
        \draw[color=white] (3.1416, 0) -- (4.1416, 0);
        \node[circle,fill, inner sep=1pt] at (0, 0) {};
        \node[circle,fill, inner sep=1pt, color=red] at (3.1416, 0) {};
        \node[color=white] at (1.5708, 0.25) {$\pi r$};
        \node[circle,fill, inner sep=1pt] at (4.1416, 0) {};
        \node[color=white] at (3.6416, 0.25) {$r$};
        \draw[color=white] (4.1416, 0) arc (0:180:2.0708);
        \node[circle,fill, inner sep=1pt, color=red] at (3.1416, 1.7725) {};
        \draw[color=red] (3.1416, 0) -- (3.1416, 1.7724);
        \node[color=red] at (2.6416, 0.8862) {$h$};
        \draw[dashed,color=white] (0, 0) -- (3.1416, 1.7724);
        \draw[dashed,color=white] (3.1416, 1.7724) -- (4.1416, 0);
        \node[fill=white] at (1.5708, 0.9) {$a$};
        \node[fill=white] at (3.5316, 0.8862) {$b$};
    \end{tikzpicture}
</script>
</div>

From here follow the three equations below: \\[\\begin{align*}
\\begin{cases}
    a^2 &= (\\pi r)^2 + h^2\\\\
    b^2 &= r^2 + h^2\\\\
    (\\pi r + r)^2 &= a^2 + b^2
\\end{cases} &\\implies (\\pi r + r)^2 = (\\pi r)^2 + r^2 + 2h^2 \\implies 2h^2 = 2\\pi r^2\\\\ &\\implies \\boxed{h = \\sqrt{\\pi} r.}
\\end{align\*}\\]

And with this, ladies and gentlemen, we've constructed the longitude we were looking for, and creating a square with this segment as side won't be but the cherry on top of a cake mathematics could never taste.

<div align="center">
<script type="text/tikz">
    \begin{tikzpicture}[scale=1.2073]
        \draw[color=white] (0, 0) -- (3.1416, 0);
        \draw[color=white] (3.1416, 0) -- (4.1416, 0);
        \node[circle,fill, inner sep=1pt, color=white] at (0, 0) {};
        \node[circle,fill, inner sep=1pt, color=red] at (3.1416, 0) {};
        \node[color=white] at (1.5708, 0.25) {$\pi r$};
        \node[circle,fill, inner sep=1pt, color=white] at (4.1416, 0) {};
        \node[color=white] at (3.6416, 0.25) {$r$};
        \draw[color=white] (4.1416, 0) arc (0:180:2.0708);
        \node[circle,fill, inner sep=1pt, color=red] at (3.1416, 1.7725) {};
        \draw[color=red] (3.1416, 0) rectangle (3.1416+1.7724,1.7724);
        % \draw[color=red] (3.1416, 0) -- (3.1416, 1.7724);
        \node[color=red] at (2.6416, 0.8862) {$\sqrt{\pi} r$};
    \end{tikzpicture}
</script>
</div>

<br>

# References

<p class="hangingindent">
<em>¿Quién dijo que la cuadratura del círculo era imposible?</em> (Mar. 2015). <a href="https://www.gaussianos.com/quien-dijo-que-la-cuadratura-del-circulo-era-imposible/">https://www.gaussianos.com/quien-dijo-que-la-cuadratura-del-circulo-era-imposible/</a>. (Accessed June 12, 2025).
</p>

<p class="hangingindent">
Bombal Gordón, Fernando (2012). "La cuadratura del círculo: Historia de una obsesión." In: <em>Real Academia de Ciencias Exactas, Físicas y Naturales</em> 105.2, pp. 241–258.
</p>