---
layout: exercises
title: Lagrange Remainder Theorem - Exercises
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---

<ol>
<li> <div class="exercise" >Suppose that $g'(x) = \sqrt{x^2+5}$, and that $g(2) = -4$.
<ol type="a">
<li>  Estimate $g(1.95)$ and $g(2.05)$. </li>
<li> Is each approximation an overestimate or an underestimate? </li>
</ol>

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" >
<ol type ="a">
<li> The linear approximation to $g$ at $x = 2$ is given by 
\[L(x) = g(2) + g'(2)(x-2)\]
\[L(x) = -4 + 3(x-2) = 3x-10\]
Plugging in the appropriate values of $x$ we obtain
\[L(1.95) = 3\cdot\frac{39}{20} - 10 = \frac{117}{20} - 10 = \frac{117 - 200}{20} = \frac{-83}{20}\]
\[L(2.05) = 3\cdot\frac{41}{20} - 10 = \frac{123}{20} - 10 = \frac{123 - 200}{20} = \frac{-77}{20}\]
</li>
<li> We compute the remainder $R_1(x)$:
\[R_1(x) = \frac{f''(2)(x-2)^2}{2} = \frac{(x-2)^2}{3} > 0\]
Since the remainder is always positive, since 
\[g(x) = T_1(x) + R_1(x)\] we know that \[g(x) - T_1(x) > 0\] so \[g(x) > T_1(x)\] so the approximations are both underestimates.
</li>
</ol>
</div>
</div>
</div>
</li>

<br>

<li> <div class="exercise"> Use a Maclaurin polynomial for $e^x$ to calculate $1/\sqrt[10]{e}$ correct to five decimal places. What degree of the polynomial is required?

<div class="answerBox">
<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer" >
The error of the approximation of $n$th order has an upper bound given by
\[E_n \leq \left| \frac{f^{(n+1)}(a)(x-a)^{n+1}}{(n+1)!}\right|\]
We note the following:
<ul>
<li> If the approximation is correct to 5 decimal places, this means that the error is strictly less than $10^{-5}$. </li>
<li>  $a =0$, because we will center the approximation at 0. </li>
<li> The value for $x$ will be $x = -\frac{1}{10}$, because $e^{-1/10} = 1/\sqrt[10]{e}$ </li>
</ul>
All derivatives of $e^x$ evaluate to 1 at $x = 0$, so we obtain $$\left| \frac{(1/10)^{n+1}}{(n+1)!}\right| < 10^{-5}$$Plugging in various $n$, we find that the minimum $n$ which satisfies this inequality is $n=3$. 
</div>
</div>
</div>
</li>

<li> <div class="exercise">
Expand $\displaystyle{\frac{1}{\sqrt[4]{1+x}}}$ as a Taylor polynomial. Use this polynomial to estimate $1.1^{-1/4}$ correct to three decimal places.

<div class="answerBox">
<button onclick="myFunction('answer3')" class="answerButton">Show Answer</button>
<div  id="answer3" class="answer" >
We note the following:
<ul>
<li> If the approximation is correct to 3 decimal places, this means that the error is strictly less than $10^{-3}$. </li>
<li>  In this problem, we will expand about $a = 0$ </li>
<li> we are interested in $x = 1/10$. </li>
</ul>
The bound on the error will be 
\[ E_n = \left|\frac{f^{(n+1)}(0)x^{n+1}}{(n+1)!}\right| < 10^{-3}\]
It appears as though $n = 2$ will suffice. Let's compute the third derivative of $\displaystyle{f(x) = \frac{1}{\sqrt[4]{1+x}}}$. We obtain 
\[f'''(x) = \frac{45}{64(1+x)^{13/4}}\]
Evaluating at $x = 0.1$:
\[ f'''(0.1) = \frac{45}{64(1.1)^{13/4}} < \frac{45}{64} < 1\]
Then, $\displaystyle{E_2 < \frac{1}{10^3(6)} < 10^{-3}}$. Thus $n = 2$.
</div>
</div>
</div>
</li>

</ol>
