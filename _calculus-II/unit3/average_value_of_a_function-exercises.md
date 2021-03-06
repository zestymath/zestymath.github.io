---
layout: exercises
title: Average Value of a Function - Exercises
dept: math
unit: unit3
course: calculus-II
deptDisplay: Math
unitDisplay: Unit 3
courseDisplay: Calculus II
---


<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" >


\question[$*$] Find the average value of $f(x)$ on the interval $[4,8]$.
\[f(x) = \frac{x}{\sqrt{x^2-15}}\]

\begin{solution}[90mm]
We apply the formula for the average value of a function on an interval.
\begin{eqnarray*}
\overline f  &=& \frac{1}{b - a}\int_a^b f(x)dx \\
&=& \frac{1}{4}\int_4^8 \frac{x}{\sqrt{x^2 - 15}} dx \\
&=& \frac{6}{4} \\
&=& \frac{3}{2}
\end{eqnarray*}
\end{solution}

\question[$*$] Find the average value of $f(x)$ on the interval $[3,4]$.
\[f(x) = \frac{1}{25-x^2}\]

\begin{solution}[90mm]
We apply the formula for the average value of a function on an interval.
\begin{eqnarray*}
\overline f  &=& \frac{1}{b - a}\int_a^b f(x)dx \\
&=& \int_3^4 \frac{1}{25 - x^2}dx\\
&=& \frac{1}{5}\log \left( \frac{3}{2} \right)
\end{eqnarray*}
\end{solution}


\question[$**$] Find the average value of $f(x)$ on the interval $(2,5)$. 
\[f(x) = \frac{1}{\sqrt{|x-3|}}\]

\begin{solution}[110mm]
We apply the formula for the average value of a function on an interval, noting that there is a vertical asymptote at $x = 3$. This means we will have to split up the integral.
\begin{eqnarray*}
\overline f  &=& \frac{1}{b - a}\int_a^b f(x)dx \\
&=& \frac{1}{3}\left(\int_2^3 \frac{dx}{\sqrt{3-x}} + \int_3^5\frac{dx}{\sqrt{x-3}}\right)\\
&=& \frac{1}{3}\left(\lim_{k\to 3^-}\int_2^k \frac{dx}{\sqrt{3-x}} + \lim_{l\to3^+}\int_l^5\frac{dx}{\sqrt{x-3}}\right)\\
&=& \frac{1}{3}\left(\lim_{k\to 3^-}\left.\left(-2\sqrt{3-x}\right)\right|_2^k + \lim_{l\to3^+}\left.\left(2\sqrt{x-3}\right)\right|_l^5\right)\\
&=& \frac{1}{3}\left(\lim_{k\to 3^-}2\left(-\sqrt{3-k} + \sqrt{1}\right)+ \lim_{l\to3^+}2\left(\sqrt{5-3} - \sqrt{l-3}\right)\right)\\
&=& \frac{2}{3}\left(1 + \sqrt{2}\right)\\
\end{eqnarray*}
\end{solution}

\question[$*$] Find the average value of $f(x) = 2^{x}$ on the interval $[1,3]$.

\begin{solution}[70mm]
\begin{eqnarray*}
\overline f  &=& \frac{1}{2}\int_1^3 2^xdx  \\
&=& \frac{1}{2}\left.\left( \frac{2^x}{\log 2} \right)\right|_1^3 \\
&=& \frac{1}{2\log 2}\left( 8 - 2 \right) \\
&=& \frac{3}{\log 2}\end{eqnarray*}
\end{solution}
