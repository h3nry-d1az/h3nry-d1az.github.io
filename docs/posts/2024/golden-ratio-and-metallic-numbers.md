# The Golden Ratio and the Metallic Numbers

<link rel="stylesheet" type="text/css" href="https://tikzjax.com/v1/fonts.css">
<script src="https://tikzjax.com/v1/tikzjax.js"></script>

<header>Oct 10, 2024</header>
<br>
<hr>

# The golden ratio

The golden number, also called the golden ratio or simply phi (\\(\varphi\\)) -- and sometimes even God's number -- is probably one of the most famous math constants of all time. It probably owes its popularity to its early discovery by the sculptor Phidias back in Ancient Greece, or to the fact that it emerges from the study of something as natural as proportions are, and it could even be a cause of its manifold, beautiful representations and its unexpected apparitions in nature.

Nonetheless, and despite its major transcendence, it is a concept even a child could fathom, and with a relatively straightforward definition:

## Mathematically correct definition
In order to determine *the* golden ratio, we must first understand what *a* golden proportion is per se:

<div class="definition">
    It is said that two lengths are in golden proportion if the ratio between the two combined and the longest equals the ratio between the longest and the shortest. That is, if \(a > b\), then \(\frac{a+b}{a} = \frac{a}{b}\).
</div>
<br>

If you've just gotten dizzy, let me tell you not to worry, because at first glance this statement may seem sort of abstract -- since we have not defined an actual constant, but rather a relationship that can be satisfied by infinite numbers --. Furthermore, it's phrased in more rigorous mathematical terminology, which hides its beautiful geometric intuition; so, to solve these two problems, let's start again and define this concept one more time.

## Geometric definition

Suppose we have two differently-sized rods, which we'll call \\(a\\) to the longest and \\(b\\) to the shortest. Let's now put them together, yielding a new one with length \\(a+b\\), just like it is shown below:

<div align="center" style="color: #bbbbbb;">
<script type="text/tikz">
    \begin{tikzpicture}
        \node[circle,fill, inner sep=1.5pt, color=red] (AB_1) at (-2, 0) {};
        \node[circle,fill, inner sep=1.5pt, color=red] (AB_2) at (-2, -1.62) {};
        \node[circle,fill, inner sep=1.5pt, color=blue] (AB_3) at (-2, -2.62) {};
        \draw[color = red] (AB_1) -- (AB_2);
        \draw[color = blue] (AB_2) -- (AB_3);
        \node at (-1.75, -0.90) {$a$};
        \node at (-1.75, -1.73) {$b$};
        \node at (-1.75, -1.31) {$+$};

        \node[circle,fill, inner sep=1.5pt, color=red] (A_1) at (0, -0.5) {};
        \node[circle,fill, inner sep=1.5pt, color=red] (A_2) at (0, -2.12) {};
        \draw[red] (A_1) -- (A_2);
        \node at (0.25, -1.31) {$a$};

        \node[circle,fill, inner sep=1.5pt, color=blue] (B_1) at (2, -0.81) {};
        \node[circle,fill, inner sep=1.5pt, color=blue] (B_2) at (2, -1.81) {};
        \draw[blue] (B_1) -- (B_2);
        \node at (2.25, -1.31) {$b$};
    \end{tikzpicture}
</script>
</div>
<br>

Notice an interesting property of the previous image, namely that comparing the newly-constructed stick \\(a+b\\) with \\(a\\) is like measuring \\(a\\) against \\(b\\), but in a reduced scale. They are in the same proportion!

Now, it is true that I have selected this detail deliberately, and not all bars satisfy this property, so we'll say that the \\(a,b\\) that do verify it are in *golden proportion*. This is the true motivation behind the earlier definition. It now makes way more sense, doesn't it?

But, as we mentioned in the beginning, the golden ratio is a *constant*, not an infinite group of numbers that meet a property, and its magnitude is precisely the earlier quotient of both lengths. We've now got all the tools we need to find its exact value:

<div class="theorem">
    All the numbers in golden proportion have as ratio \(\frac{1+\sqrt5}{2}\).
</div>
<div class="proof">
    As we stated above, this value is commonly represented as \(\varphi\) in honor of the aforementioned Phidias, and I won't be making an exception here. Replacing then \(\varphi\) for \(a/b\) in the first definition and simplifying we reach the following equality:
    $$
    \begin{align*}
        \frac{a}{b}&=\frac{a+b}{a}\implies\frac{a}{b}=1+\frac{b}{a}\\
        &\implies \varphi = 1 + \varphi^{-1}\\
        &\implies \varphi^2 = \varphi + 1\\
        &\implies \varphi^2 - \varphi - 1 = 0
    \end{align*}
    $$

    Which is a classic quadratic equation that any high school student could solve, so it will suffice to employ Bhaskara's formula:
    $$
    \begin{align*}
        \varphi &= \frac{-(-1)\pm\sqrt{(-1)^2-4\cdot(1)\cdot(-1)}}{2\cdot(1)} = \frac{1 \pm \sqrt{5}}{2}
    \end{align*}
    $$

    Nevertheless, \(\varphi\) must be positive, since we are dealing with a ratio of positive numbers, therefore we can discard the second solution:
    $$\varphi = \frac{1+\sqrt5}{2}$$

    The other remaining value is called the <em>conjugate</em> of \(\varphi\), because it has the sign of the second summand inverted. It is usually denoted by \(\tilde\varphi\) and, in a enthralling manner, it holds that \(\tilde\varphi = -\frac{1}{\varphi} = 1-\varphi\).
</div>

To conclude this section, below are listed [a hundred significant figures](http://www.numberworld.org/digits/GoldenRatio/) of this curious constant:

<div align="center">
<span style="font-size: 22pt;">1.</span><span style="font-size: 20pt;">6</span><span style="font-size: 18pt;">1</span><span style="font-size: 16pt;">8</span>0339887&nbsp;&nbsp;&nbsp;4989484820&nbsp;&nbsp;&nbsp;4586834365&nbsp;&nbsp;&nbsp;6381177203&nbsp;&nbsp;&nbsp;0917980576
    &nbsp;&nbsp;&nbsp;2862135448&nbsp;&nbsp;&nbsp;6227052604&nbsp;&nbsp;&nbsp;6281890244&nbsp;&nbsp;&nbsp;9707207204&nbsp;&nbsp;&nbsp;1893911374&hellip;
</div>
<br>
<br>

# The metallic numbers
But, why stop here? Sure the golden ratio is such an interesting concept, but will it be the only value with similar characteristics? The solution to this unknown are the "metallic numbers", whose structure we'll study next, and whose name alludes to the *gold* in *golden ratio*.

## The golden ratio, revisited
Recall the geometric definition for a golden proportion we came up with, and let's put the rods \\(a+b\\) and \\(a\\) perpendicularly, forming a rectangle like the following:
<div align="center" style="color: #bbbbbb;">
<script type="text/tikz">
    \begin{tikzpicture}
        \node[circle,fill, inner sep=1.5pt, color=red] (A_1) at (0, 0) {};
        \node[circle,fill, inner sep=1.5pt, color=red] (A_2) at (0, -2) {};
        \node[circle,fill, inner sep=1.5pt, color=red] (AB_1) at (2, -2) {};
        \node (AB_null) at (2, 0) {};
        \node[circle,fill, inner sep=1.5pt, color=blue] (AB_2) at (3.24, -2) {};
        \node (AB_2_null) at (3.24, 0) {};
        \draw[color = red, fill=red!35] (A_1.center) -- (A_2.center) -- (AB_1.center) -- (AB_null.center) -- cycle;
        \draw[color = blue, fill=blue!35] (AB_1.center) -- (AB_2.center) -- (AB_2_null.center) -- (AB_null.center) -- cycle;
        \node at (1, -2.39) {$a$};
        \node at (2.62, -2.35) {$b$};
        \node at (2, -2.35) {$+$};
        \node at (-0.35, -1) {$a$};
    \end{tikzpicture}
</script>
</div>
<br>

Let's now detach the blue rectangle from the former and see what happens:
<div align="center" style="color: #bbbbbb;">
<script type="text/tikz">
    \begin{tikzpicture}
            \node[circle,fill, inner sep=1.5pt, color=red] (A_1) at (0, 0) {};
            \node[circle,fill, inner sep=1.5pt, color=red] (A_2) at (0, -2) {};
            \node[circle,fill, inner sep=1.5pt, color=red] (AB_1) at (2, -2) {};
            \node (AB_null) at (2, 0) {};
            \node[circle,fill, inner sep=1.5pt, color=blue] (AB_2) at (3.24, -2) {};
            \node (AB_2_null) at (3.24, 0) {};
            \draw[color = red, fill=red!35] (A_1.center) -- (A_2.center) -- (AB_1.center) -- (AB_null.center) -- cycle;
            \draw[color = blue, fill=blue!35] (AB_1.center) -- (AB_2.center) -- (AB_2_null.center) -- (AB_null.center) -- cycle;
            \node at (1, -2.39) {$a$};
            \node at (2.62, -2.35) {$b$};
            \node at (2, -2.35) {$+$};
            \node at (-0.35, -1) {$a$};

            \node at (4.24, -1) {$\longrightarrow$};
            \node[circle,fill, inner sep=1.5pt, color=blue] (B_1) at (5.59, -0.38) {};
            \node[circle,fill, inner sep=1.5pt, color=blue] (B_2) at (5.59, -1.62) {};
            \node (B_4) at (7.59, -0.38) {};
            \node[circle,fill, inner sep=1.5pt, color=blue] (B_3) at (7.59, -1.62) {};
            \draw[color = blue, fill=blue!35] (B_1.center) -- (B_2.center) -- (B_3.center) -- (B_4.center) -- cycle;
            \node at (5.24, -1) {$b$};
            \node at (6.59, -1.97) {$a$};
        \end{tikzpicture}
</script>
</div>
<br>

Like the lengths from our old definition, the new rectangle is equal to the previous one, but deescalated; that is, they are both *proportional* to one another.

This new property is equivalent to the earlier definition and, perhaps, even more visual. Furthermore, it'll be our starting point to generalize the golden ratio.

Just as a curiosity, the DIN A*x* paper formats are based upon a similar idea, but in that case, the proportion is \\(\sqrt2\\), because cutting in half a DIN A3 produces two DIN A4, a DIN A4 two DIN A5, and so forth. Can you show why this is the ratio? (Hint: use the proof for the theorem we have just discussed.)

## Definition of the metallic numbers
Allow me to go back to the previous rectangle and tweak it slightly. What if I wanted a rectangle with this same property, but more stretched? At first glance, one may wonder: “Why would I want something like this?” but this shape would have numerous applications, combining the robustness of the former with dimensions more suitable for certain situations.

By our previous theorem, something *exactly* equal is impossible, yet we can apply a little trick to obtain what we're looking for:
<div align="center" style="color: #bbbbbb;">
<script type="text/tikz">
    \begin{tikzpicture}
            \node[circle,fill, inner sep=1.5pt, color=red] (A_1) at (0, 0) {};
            \node[circle,fill, inner sep=1.5pt, color=red] (A_2) at (0, -2.41) {};
            \node[circle,fill, inner sep=1.5pt, color=red] (AB_1) at (4.82, -2.41) {};
            \node (AB_null) at (4.82, 0) {};
            \node[circle,fill, inner sep=1.5pt, color=blue] (AB_2) at (5.82, -2.41) {};
            \node (AB_2_null) at (5.82, 0) {};
            \draw[color = red, fill=red!35] (A_1.center) -- (A_2.center) -- (AB_1.center) -- (AB_null.center) -- cycle;
            \draw[color = blue, fill=blue!35] (AB_1.center) -- (AB_2.center) -- (AB_2_null.center) -- (AB_null.center) -- cycle;
            \node at (2.41, -2.76) {$2a$};
            \node at (5.32, -2.76) {$b$};
            \node at (4.82, -2.76) {$+$};
            \node at (-0.35, -1.205) {$a$};
        \end{tikzpicture}
</script>
</div>
<br>

Multiplying the \\(a\\) of the longer segment by a constant yields something along those lines. And the number two here isn't special at all, it could very well be a 3, a 4, or *generalizing*, any given \\(n\\)!

However, we stumble upon a small problem, being that varying the longitude of the segments changes our proportion too, so the golden ratio would take a new value in this case, although it would receive the name of *golden ratio*, but rather we shall call it a *metallic number*. In general, the metallic number resulting from multiplying \\(a\\) by \\(n\\) will be called the nth metallic number.

## Finding the nth metallic number
Before proceeding with the computations, let's introduce some notation to summarize with more precision and rigor the geometric concept we've been developing until now:

<div class="definition">
    The nth metallic number, denoted \(\mu_n\), is defined as the quotient \(\frac{a}{b}\), where the values \(a\) and \(b\) verify the following relationship:
    $$\frac{a}{b}=\frac{na+b}{a}$$
</div>
<br>

I've chosen the Greek letter \\(\mu_n\\) to represent this collection, since metal in Ancient Greek is μέταλλον, and these were the discoverers of this idea; although it is worth pointing out that it can be seen represented as \\(A(n)\\), and virtually as other variations of which I'm unaware.

Regardless, armed with the previous definition and the proof of the first theorem, we can once and for all find a general expression for \\(\mu_n\\):

<div class="theorem">
    The nth metallic number has as value $$\mu_n = \frac{n+\sqrt{n^2+4}}{2}.$$
</div>
<div class="proof">
    Recalling the definition of a metallic number, we have that:
    $$
    \begin{align*}
            \frac{a}{b}&=\frac{na+b}{a}\implies\frac{a}{b}=n+\frac{b}{a}\\
            &\implies \mu_n = n + {\mu_n}^{-1}\\
            &\implies {\mu_n}^2 = n{\mu_n} + 1\\
            &\implies {\mu_n}^2 - n{\mu_n} - 1 = 0
        \end{align*}
    $$

    Which is yet another quadratic equation with an easy solution:
    $$
    \begin{align*}
            \mu_n &= \frac{-(-n)\pm\sqrt{(-n)^2-4\cdot(1)\cdot(-1)}}{2\cdot(1)}\\
            &= \frac{n\pm\sqrt{n^2+4}}{2}
        \end{align*}
    $$

    And since all \(\mu_n\) have to be greater than zero -- because they denote the ratio of two positive quantities --, we can discard with no fear the negative roots:
    $$\mu_n = \frac{n+\sqrt{n^2+4}}{2}$$
    As it was to be proven.
</div>

The first five metallic numbers already have a name (and even symbol), being [the following](https://mathworld.wolfram.com/SilverRatio.html):
<div align="center">
<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;11
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-axxb{background-color:#c0c0c0;border-color:inherit;color:#000000;font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-c3ow{border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-2yfi{background-color:#c0c0c0;border-color:inherit;color:#000000;text-align:center;vertical-align:top}
</style>
<table class="tg"><thead>
  <tr>
    <th class="tg-2yfi">\(n\)</th>
    <th class="tg-axxb">Metal</th>
    <th class="tg-axxb">Symbol</th>
    <th class="tg-axxb">Exact value</th>
    <th class="tg-axxb">Approximated value</th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-c3ow">1</td>
    <td class="tg-c3ow">Gold</td>
    <td class="tg-c3ow">\(\varphi\)</td>
    <td class="tg-c3ow">\(\frac{1+\sqrt5}{2}\)</td>
    <td class="tg-c3ow">1.618033989&hellip;</td>
  </tr>
  <tr>
    <td class="tg-c3ow">2</td>
    <td class="tg-c3ow">Silver</td>
    <td class="tg-c3ow">\(\delta_S\)</td>
    <td class="tg-c3ow">\(1+\sqrt2\)</td>
    <td class="tg-c3ow">2.414213562&hellip;</td>
  </tr>
  <tr>
    <td class="tg-c3ow">3</td>
    <td class="tg-c3ow">Bronze</td>
    <td class="tg-c3ow">\(\delta_{\text{Br}}\)</td>
    <td class="tg-c3ow">\(\frac{3+\sqrt{13}}{2}\)</td>
    <td class="tg-c3ow">3.302775638&hellip;</td>
  </tr>
  <tr>
    <td class="tg-c3ow">4</td>
    <td class="tg-c3ow">Copper</td>
    <td class="tg-c3ow">\(\delta_{\text{Cu}}\)</td>
    <td class="tg-c3ow">\(2+\sqrt5\)</td>
    <td class="tg-c3ow">4.236067978&hellip;</td>
  </tr>
  <tr>
    <td class="tg-c3ow">5</td>
    <td class="tg-c3ow">Nickel</td>
    <td class="tg-c3ow">\(\delta_{\text{Ni}}\)</td>
    <td class="tg-c3ow">\(\frac{5+\sqrt{29}}{2}\)</td>
    <td class="tg-c3ow">5.192582404&hellip;</td>
  </tr>
</tbody></table>
</div>
<br>

Nonetheless, the remaining infinite ones have neither an official, recognized nickname, nor an associated symbol, so I can take for example \\(\mu_{14}=7+5\sqrt{2}\\), and hereby name it *Henry's number*, giving it the symbol \\(\mathfrak h\\). And, of course, *you* can do this same thing as well.

## Abstraction in mathematics
There's a quote from the great mathematician J. Henri Poincaré which, from my perspective, brings together exceptionally the main idea of this essay:
> "Mathematics is the art of giving the same name to different things."

And it is true that the spirit of a mathematician isn't fulfilled with discovering an interesting property, but craves to explore the limits of their finding, thus expanding it in such a way that what was earlier thought as a whole, now it isn't but a special case of a more robust theory, which englobes entities formerly unrelated but now connected.

This process receives the name of *abstraction* or *generalization* and, although in principle can appear confusing and useless, it is one of the more powerful tools mathematicians have at their disposal and, more importantly, the fire that fuels their work.