---
layout: exercises
title: Definition of the Derivative
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---

<ol>
<li> <div class="exercise"> Suppose $f(x)$ is differentiable at $x = a$. Find the value of the limit in terms of $f'(a)$:
\[\lim_{x\to a}\frac{f(x) - f(a)}{\sqrt{x} - \sqrt{a}}\]

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" >

First, notice that the limit is very similar to the definition of the derivative. Multiply both numerator and denominator by $\sqrt{x}+\sqrt{a}$ to obtain the form of the definition of the derivative.

\begin{eqnarray*}
\lim_{x\to a}\frac{f(x) - f(a)}{\sqrt{x} - \sqrt{a}} \cdot \frac{\sqrt{x}+\sqrt{a}}{\sqrt{x}+\sqrt{a}} &=& \lim_{x\to a}\frac{f(x) - f(a)}{x - a} \cdot (\sqrt{x}+\sqrt{a})\\
\end{eqnarray*}
Next, use the property of the limits to separate the limit into two.
\begin{eqnarray*}
\lim_{x\to a}\frac{f(x) - f(a)}{x - a} \cdot (\sqrt{x}+\sqrt{a}) &=& \lim_{x\to a}\frac{f(x) - f(a)}{x - a} \cdot \lim_{x\to a}(\sqrt{x}+\sqrt{a})\\
&=& f'(a) \cdot \lim_{x\to a}(\sqrt{x}+\sqrt{a})\\
&=& f'(a) \cdot 2\sqrt{a}\\
\end{eqnarray*}
</div> 
</div>

</div>
</li> 


<li>  <div class="exercise"> Compute the derivative of $\displaystyle{y = \sqrt{5x + 1}}$ using the definition of the derivative. 

<div class="answerBox">
<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>

<div  id="answer2" class="answer">
\begin{eqnarray*}
y' &=& \lim_{h \to 0} \frac{\sqrt{5(x+h) + 1} - \sqrt{5x + 1}}{h}\\
&=& \lim_{h \to 0} \frac{(\sqrt{5(x+h) + 1} - \sqrt{5x + 1})(\sqrt{5(x+h) + 1} + \sqrt{5x + 1})}{h(\sqrt{5(x+h) + 1} + \sqrt{5x + 1})}\\
&=& \lim_{h \to 0} \frac{5x + 5h + 1 - 5x - 1}{h(\sqrt{5(x+h) + 1} + \sqrt{5x + 1})}\\
&=& \lim_{h \to 0} \frac{5h}{h(\sqrt{5(x+h) + 1} + \sqrt{5x + 1})}\\
&=& \lim _{h \to 0} \frac{5}{\sqrt{5(x+h) + 1} + \sqrt{5x + 1}}\\
&=& \frac{5}{2 \sqrt{5x+1}}
\end{eqnarray*}
</div> 
</div>
</div>
</li>

<li> <div class="exercise"> Compute $f'(x)$ using the definition of the derivative if 
$$f(x)=\frac{\sqrt{x+1}}{x}.$$

<div class="answerBox">
<button onclick="myFunction('answer3')" class="answerButton">Show Answer</button>
<div  id="answer3" class="answer">
\begin{eqnarray*}
f'(x) &=& \lim_{h \to 0} \frac{f(x+h)-f(x)}{h}\\
&=&\lim_{h \to 0} \frac{\frac{\sqrt{x+h+1}}{x+h} - \frac{\sqrt{x+1}}{x}}{h}\\
&=&\lim_{h \to 0} \frac{x\sqrt{x+h+1} - (x+h)\sqrt{x+1}}{xh(x+h)}\\
&=&\lim_{h \to 0}  \frac{x\sqrt{x+h+1} - (x+h)\sqrt{x+1}}{xh(x+h)} \cdot \frac{x\sqrt{x+h+1} + (x+h)\sqrt{x+1}}{x\sqrt{x+h+1} + (x+h)\sqrt{x+1}}\\
&=&\lim_{h \to 0} \frac{x^2(x+h+1)-(x+h)^2(x+1)}{xh(x+h)(x\sqrt{x+h+1} + (x+h)\sqrt{x+1})}\\
&=&\lim_{h \to 0}  \frac{x^3+x^2h+x^2-(x^2+2xh+h^2)(x+1)}{xh(x+h)(x\sqrt{x+h+1} + (x+h)\sqrt{x+1})}\\
&=&\lim_{h \to 0} \frac{x^3+x^2h+x^2-(x^3+2x^2h+xh^2+x^2+2xh+h^2)}{xh(x+h)(x\sqrt{x+h+1} - (x+h)\sqrt{x+1})} \\
&=&\lim_{h \to 0}  \frac{-x^2h-xh^2-2xh-h^2}{xh(x+h)(x\sqrt{x+h+1} + (x+h)\sqrt{x+1})}\\
&=&\lim_{h \to 0}  \frac{-x^2-xh-2x-h}{x(x+h)(x\sqrt{x+h+1} + (x+h)\sqrt{x+1})}\\
&=& \frac{-x^2-2x}{x^2(x\sqrt{x+1} + x\sqrt{x+1})}\\
&=& \frac{-x-2}{x(x\sqrt{x+1} + x\sqrt{x+1})}\\
f'(x) &=& \frac{-x-2}{2x^2\sqrt{x+1}}\\
\end{eqnarray*}
</div> 
</div>
</div>
</li>


<li> <div class="exercise"> For the given function $f(x)$, determine if 
<ol type = "a">
<li>  $f(x)$ is continuous at $x = 2$, and </li>
<li> if $f(x)$ is differentiable at $x = 2$. </li>
</ol>
\[f(x) = \frac{|x-2|-7}{x+4}\]

<div class="answerBox">
<button onclick="myFunction('answer4')" class="answerButton">Show Answer</button>
<div  id="answer4" class="answer">
A function is continuous if 

$$f(a)=\lim_{x\to a}f(x)$$

We can rewrite $f(x)$ in piecewise notation as
$$f(x) = \begin{cases}
\frac{x-9}{x+4}& , x \geq 2 \\
\frac{-5-x}{x+4} &, x < 2
\end{cases}$$

<ol>
<li> Right hand side limit:
\begin{eqnarray*}
\lim_{x\to2^+}f(x)&=&\lim_{x\to2^+}\frac{x-9}{x+4}\\
&=&\frac{-7}{6}
\end{eqnarray*}
</li>
<li>  Left hand side limit:
$$\begin{eqnarray*}
\lim_{x\to2^-}f(x)&=&\lim_{x\to2^-}\frac{-5-x}{x+4}\\
&=&\frac{-7}{6}
\end{eqnarray*}$$
</li>
</ol>

The lateral limits are equal to each other and to $f(2)$, therefore $f(x)$ is continuous at $x = 2$.

A function is differentiable if the limit

$$\lim_{x\to a}\frac{f(x)-f(a)}{x-a}$$

exists and $f$ is continuous at $a$. We already know that $f$ is continuous at $x = a$. Here, $a=2$ and $f(2)=\frac{-7}{6}$.

<ol>
<li> Differentiability from the right:
\begin{eqnarray*}
\lim_{x\to2^+}\frac{\frac{x-9}{x+4}-(-\frac{7}{6})}{x-2^+}&=& \lim_{x\to2^+}\frac{\frac{6}{6}\cdot\frac{x-9}{x+4}+\frac{x+4}{x+4}\cdot\frac{7}{6}}{x-2}\\
&=&\lim_{x\to2^+}\frac{\frac{6x-54}{6x+24}+\frac{7x+28}{6x+24}}{x-2}\\
&=&\lim_{x\to2^+}\frac{\frac{13x-26}{6x+24}}{x-2}\\
&=&\lim_{x\to2^+}\frac{13x-26}{(6x+24)(x-2)}\\
&=&\lim_{x\to2^+}\frac{13(x-2)}{(6x+24)(x-2)}\\
&=&\lim_{x\to2^+}\frac{13}{6x+24}\\
&=&\frac{13}{36}
\end{eqnarray*}
</li>
<li> Differentiability from the left:
\begin{eqnarray*}
\lim_{x\to2^-}\frac{\frac{-5-x}{x+4}-(-\frac{7}{6})}{x-2}
&=& \lim_{x\to2^-}\frac{\frac{6}{6}\cdot\frac{-5-x}{x+4}+\frac{x+4}{x+4}\cdot\frac{7}{6}}{x-2}\\
&=&\lim_{x\to2^-}\frac{\frac{-30-6x}{6x+24}+\frac{7x+28}{6x+24}}{x-2} \\
&=&\lim_{x\to2^-}\frac{\frac{x-2}{6x+24}}{x-2}\\
&=&\lim_{x\to2^-}\frac{1}{6x+24}\\
&=&\frac{1}{36}
\end{eqnarray*}
</li>
</ol>

Since $\frac{13}{36} \not=\frac{1}{36}$ the slopes are unequal and the function is not differentiable at $x = 2$.

</div>
</div>
</div>
</li>

</ol>
