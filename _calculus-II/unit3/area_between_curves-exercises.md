---
layout: exercises
title: Areas - Exercises
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


\question[$*$] Find the area bounded by the parabolas $y = 6x -x^2$ and $y = x^2 - 2x$.

\begin{solution}[80mm]
First we need to find the points of intersection of the parabolas. Solving the equation
\[6x - x^2 = x^2 - 2x\] 
gives the solutions $x = 0,4$. The area is then given by 
\begin{eqnarray*}
A  &=& \int_0^4 6x - x^2 - (x^2 - 2x)dx \\
&=& \int_0^4 8x - 2x^2dx \\
&=& \left. \left( 4x^2 - \frac{2}{3}x^3 \right) \right|_0^4\\
&=& 4(4)^2 - \frac{2}{3}{(4)^3} \\
&=& 64 - \frac{2}{3} \cdot 64 \\
&=& \frac{64}{3}
\end{eqnarray*}
\end{solution}

%Q19
\question[$**$] Compute the area enclosed by the curves: $y = 25 - x^2$, $256x = 3y^2$, $16y = 9x^2$

\begin{solution}[105mm]
See the following two figures which represent the two areas we need to sum:\\
\includegraphics[scale = 0.5]{(13-1)}
\includegraphics[scale = 0.5]{(13-2)}

First we find out where the curves intersect, which gives us two distinct regions separated at $x = 3$. Thus the area will be the sum of the two shaded regions shown in the figures.
\[A_1 = \int_0^3\left[ \left( \frac{256}{3}x \right)^{1/2} - \frac{9}{16}x^2\right]dx\]
\[A_2 =  \int_3^4 \left[ 25 - x^2 - \frac{9}{16}x^2\right]dx \]
The two integrals are easily evaluated, and the sum of the two is then
\[A_1 + A_2 = \frac{98}{3}\]
\end{solution}


%Q20
\question[$***$] Compute the area enclosed by the curve $y^2 = x^2 - x^4$.
\begin{hint}
This curve is symmetric with respect to the $x$ axis and the $y$ axis. How can you use symmetry to help you calculate the area?
\end{hint}

\begin{solution}[200mm]
See the figure which shows the area we need to compute.\\
\includegraphics[scale = 0.5]{(15)}

First we make some observations as to how one would sketch the graph.
\begin{itemize}
\item First note that this graph is symmetric with respect to both the $x$ axis and $y$ axis, because replacing $x$ by $-x$ or $y$ by $-y$ leaves the relation unchanged. This means we can find the area enclosed in one quadrant, then multiply by 4.
\item There are zeros at $x = 0$ and $x = 1$, which means we can draw an arc between those two points, then reflect it about the $x$ and $y$ axes for the total graph.
\item The graph cannot extend beyond $x = 1$ because otherwise the expression inside square root that is obtained when solving for $y$ would become negative. Solving for $y$, 
\[y = x\sqrt{1-x^2}\]
which holds for the portion in the first quadrant.
\end{itemize}

Integrating this expression from 0 to 1, then multiplying by 4 yields 
\[4\int_0^1 x\sqrt{1 - x^2} dx = 4\left( \frac{-1}{3} \right)\left. \left( 1 - x^2 \right)^{3/2} \right| _0^1 = \frac{4}{3}\]
\end{solution}

%Q21
\question[$***$] Compute the area enclosed by the curve $y^2 = x^4(x+4)$ for the portion of the graph lying to the left of the $y$--axis.

\begin{solution}[205mm]
See the figure which shows the area we need to compute.\\
\includegraphics[scale = 0.5]{(16)}

First we need to determine how this graph is constructed:
\begin{itemize}
\item The graph is symmetric with respect to the $x$ axis because replacing $y$ by $-y$ leaves the relation unchanged.
\item There are zeros at $x = 0$ and $x = -4$
\item The graph does not continue past $x = -4$ because that would make the inside of the square root negative when solving for $y$.
\[y = x^2\sqrt{x+4}\]
\end{itemize}
This means that we draw a curve going through $x = 0$ and $x = -4$ that is also vertically symmetric.
The expression for the area is given by \[2\int_{-4}^0 x^2\sqrt {x + 4} dx \]
First we must find the antiderivative. To evaluate this integral, let  $x + 4 = u^2$ and thus $dx = 2u du$. We then obtain the integral

\begin{eqnarray*}
\int x^2\sqrt{x + 4} dx &=& 2\int (u^2 - 4)^2udu \\
&=& 2\int u^5 - 8u^3 + 16u du  \\
&=& 2\left(\frac{u^6}{6} - 2u^4 + 8u^2 \right)\\
&=& \frac{(x + 4)^3}{3} - 4(x + 4)^2 + 16(x + 4) \\
\end{eqnarray*}
Now plugging in the bounds of the original integral to find the area:
\begin{eqnarray*}
2\int_{-4}^0 x^2\sqrt{x + 4} dx &=& 2\left. \left(\frac{(x + 4)^3}{3} - 4(x + 4)^2 + 16(x + 4) \right) \right|_{-4}^0 \\
&=& \frac{128}{3}
\end{eqnarray*}
\end{solution}

\question[$**$] Find the area enclosed between the $x$ axis and the first arch of 
\[y = e^{-ax}\sin(ax)\]

\begin{solution}[205mm]
The function is 0 at $x = 0$, and $x = \pi/a$, and thus the first arch is contained in that interval. The area of the first arch is then given by
\[\int_0^{\pi /a} e^{-ax}\sin (ax)dx\]
First, we find the antiderivative of the integrand. Let $u = ax$ and $du = adx$. 
\begin{eqnarray*}
\int e^{-ax}\sin (ax)dx &=& \frac{1}{a}\int e^{-u}\sin udu \\
&=&\frac{1}{a}\left( -e^{-u}\sin u + \int e^{-u}\cos u du\right) \\
&=& \frac{1}{a} \left(-e^{-u}\sin u - e^{-u}\cos u - \int e^{-u}\sin u du \right) \\
\end{eqnarray*}
Rearranging, 
\begin{eqnarray*}
\frac{1}{a}\int e^{-u}\sin udu  &=& \frac{1}{a}\left( \frac{-1}{2}e^{-u}(\sin u + \cos u) \right) \\
&=& \frac{-e^{-ax}}{2a}(\sin (ax) + \cos (ax))\\
\end{eqnarray*}
Evaluating,
\begin{eqnarray*}
\int_0^{\pi /a} e^{-ax}\sin (ax)dx &=& \left[ \frac{- e^{-ax}}{2a}(\sin (ax) + \cos (ax)) \right]_0^{\pi /a} \\
&=& \frac{-1}{2a}\left[ e^{-\pi}\cos (\pi ) - \cos 0 \right]\\
&=& \frac{e^{-\pi} +1}{2a}
\end{eqnarray*}
\end{solution}


\question[$***$] Let $a > 0$. Find the area enclosed by the loop. \[9ay^2=x(3a-x)^2\]
\begin{hint} Draw a picture, noting that the graph is symmetric with respect to the $x$ axis, and has zeros at $x = 0, 3a$. \end{hint}

\begin{solution}[190mm]
First, to get an idea of what the graph looks like, observe that it is symmetric with respect to the $x$-axis, because replacing $y$ by $-y$ leaves the equation unchanged. Solving for $y$, 
\[y =  \pm \frac{\sqrt{x}|3a - x|}{3\sqrt{a}}\\\]
Note that the function has zeroes at $x = 0$ and $x = 3a$. Thus it will be a closed loop cross the $x$ axis at those two points. The area is then given by 
\begin{eqnarray*}
A &=& 2\int_0^{3a} \frac{\sqrt{x} (3a - x)}{3\sqrt{a}}dx  \\
&=& \frac{2}{3\sqrt{a}}\left.\left( 3a\frac{2}{3}x^{3/2} - \frac{2}{5}x^{5/2} \right)\right|_0^{3a}\\
&=& \frac{2}{3\sqrt{a}}\left( 3a\frac{2}{3}(3a)^{3/2} - \frac{2}{5}(3a)^{5/2} \right) \\
&=& \frac{2}{3}\left( \frac{2}{3}a^2 3^{3/2} - \frac{2}{5}a^2 3^{5/2} \right) \\
&=& \frac{4a^2}{3}\left( \sqrt{3}  - \frac{3^{5/2}}{5} \right)
\end{eqnarray*}
\end{solution}


