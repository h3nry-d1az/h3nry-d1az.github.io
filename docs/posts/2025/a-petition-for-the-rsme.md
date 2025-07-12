# A Petition for the RSME

<header>Jul 12, 2025</header>
<br>
<hr>

For the past couple of years, I've been an avid enthusiast of the [problem of the month](https://www.rsme.es/category/el-problema-del-mes/) section run by the *Real Sociedad Matemática Española* (RSME), and believe it or not, it has truly given me some of the most satisfying "eureka" moments I have ever experienced in my entire life. In some way, it has brought me the motivation to do math on my own -- because being featured as a solver is a really appealing reward --, to enjoy the problem-solving experience for its own sake, and sometimes pretty much the only thing to look forward to. I can undoubtedly say that I've matured mathematically with it, and it's something I'll always be grateful for.

The project started aiming to keep people thinking back during the lockdown, but this present year things have gone downhill: problems have been delayed every single month, until in April the last one to date was published, with remarkably already well-known questions and a very sloppy appearance overall (notice the URL references March instead of April and the year is not present). It is such a pity -- which I suspect may be a consequence of a possible lack of funding or personnel, or even a decrease in participants -- because this section meant a lot to many people like me.

# One of my favorite problems

Today, I'd like to share by far my favorite from this year and one of my top-3 ever by far. It corresponds to the senior one in the [February issue](https://www.rsme.es/2025/02/el-problema-del-mes-febrero-2025/), and I like it because it's short but clever, looks nasty and intimidating but rapidly transforms into a harmless expression; no official solution for it was published either, so here's my little contribution to the community. Without further ado, here's its statement translated into English:

<div class="problem">
Prove that if a line intersects the curve \(y=\sqrt[3]{x^2}\) at three points with abscissas \(x_1\), \(x_2\), and \(x_3\), then \(\displaystyle \sqrt[3]{\frac{x_2 x_3}{{x_1}^2}}+\sqrt[3]{\frac{x_3 x_1}{{x_2}^2}}+\sqrt[3]{\frac{x_1 x_2}{{x_3}^2}}\) is constant.
</div>

<br>
Before jumping straight into its solution, we need to take a look at a result widely known in math olympiads, not so obvious at first glance. Vieta's formulas relate a polynomial's coefficients to its roots, and can be deduced really quickly.

By the fundamental theorem of algebra (FTA), we can factor out any polynomial \\(p\\) as \\[\begin{align\*}
p(x)&=a_n(x-x_1)(x-x_2)\\cdots(x-x_n)\\\\
&=a_n x^n - a_n(x_1 + \\ldots + x_n)x^{n-1} + a_n(x_1x_2 + \\ldots + x_1x_n)x^{n-2} + \\ldots + a_nx_1\\cdots x_n,
\end{align\*} \tag{1}\\] where \\(n\\) is the degree of \\(p\\), \\(x_i\\) its \\(i\\)th root, and \\(a_n\\) the coefficient of \\(x^n\\). Recall also that any polynomial can by definition be expressed as \\[p(x)=a_n x^n + a_{n-1} x^{n-1} + \\ldots + a_1 x + a_0 \tag{2};\\] so combining equations \\((1)\\) and \\((2)\\) we reach the conclussion that \\[\\sum_{1\\leq i_1 < i_2 < \\ldots < i_k \\leq n} \\left(\\prod_{j=1}^k x_{i_j}\\right) = (-1)^k \\frac{a_{n-k}}{a_n}.\\]

It's much easier to understand if you do the same procedure -- expand out the FTA form and identify each coefficient -- on a concrete polynomial, but that's it: everything you need to know to understand the solution.

<div class="solution">
Because lines can be described by the equation \(y=ax+b\), we face the equality \(\sqrt[3]{x^2}=ax+b\), which we can reorganize by cubing both sides: \[\begin{align*}
    \sqrt[3]{x^2}=ax+b &\implies x^2 = (ax+b)^3 = a^3 x^3 + 3 a^2 b x^2 + 3 a b^2 x + b^3\\
    &\implies a^3 x^3 + (3 a^2 b -1) x^2 + 3 a b^2 x + b^3 = 0.
\end{align*}\] Now, invoking Vieta's formulas for third-degree polynomials we deduce that, if \(x_1\), \(x_2\) y \(x_3\) are solutions, then \[x_1x_2x_3 = -\frac{b^3}{a^3}\qquad\text{and}\qquad x_1x_2 + x_2x_3 + x_3x_1 = \frac{3ab^2}{a^3} = \frac{3b^2}{a^2}.\] Overall, the given expression starts to cancel out, and simplifies down to \[\begin{align*}
    \sqrt[3]{\frac{x_2 x_3}{{x_1}^2}}+\sqrt[3]{\frac{x_3 x_1}{{x_2}^2}}+\sqrt[3]{\frac{x_1 x_2}{{x_3}^2}} &= -\sqrt[3]{\frac{b^3}{a^3{x_1}^3}}-\sqrt[3]{\frac{b^3}{a^3{x_2}^3}}-\sqrt[3]{\frac{b^3}{a^3{x_3}^3}}\\
    &= -\frac{b}{a} \left(\frac{1}{{x_1}}+\frac{1}{{x_2}}+\frac{1}{{x_3}}\right) = -\frac{b}{a} \cdot \frac{x_1x_2 + x_2x_3 + x_3x_1}{x_1x_2x_3}\\
    &= -\frac{b}{a}\cdot \frac{3b^2/a^2}{-b^3/a^3} = \boxed{3},
\end{align*}\] which is indeed a constant, as we wanted to prove.

</div>

# Final thoughts

I've made this post, not as hatred towards the RSME for abandoning this section, but rather to encourage people to try out their problems and send their solutions, maybe if a large enough amount does so, we'll get the problem of the month back.

My petition is for the RSME to consider how beloved the POTM is, and to do their best to keep it going; if someone is needed to maintain this section, I volunteer to do so, despite not being a math major.