---
layout: lesson
title: Linear Approximations and Differentials
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---

### Tangent Lines
Consider a curve $f(x)$. Suppose we already know the value of $f(a)$, but we want to know the value of $f(x)$, with $x$ being quite close to $a$. If we draw the tangent line to $f(x)$ at $x = a$, then this line will be pretty close to $f$ as long as $x$ is close to $a$. We know for sure that it is really easy to plug in values into a linear approximation to get a clean answer, even if it is not possible for the original function! 

<figure class="center">
<p><img src="linear_approximations_and_differentials-Figures/lin_approx.svg" alt="linear approximation" style="width:350px;height:250px;"> </p>
<figcaption class="center">A function $f(x)$ with its linear approximation $L(x)$ about the point $x = a$.</figcaption> </figure>

The tangent line to the curve $f(x)$ at the point $x=a$ can be found by using the form 

$$\frac{y - f(a)}{x-a} = m,$$

where $m = f'(a)$ is the slope of the tangent line at $x=a$. Thus, the formula for the tangent line is 

$$y = f(a) + f'(a)(x-a).$$

Sometimes, people use the letter $L$ for the tangent line because it is also called a "linear approximation"; $L$ for linear. To illustrate how this idea can be applied, let's do some examples!

### Examples

<div class="example">
<p><b>Example:</b> Calculate the tangent line to $f(x) = \sqrt{1+x^3}$ at $x=2$. </p>
<b>Solution:</b> First, we calculate $f(2) = \sqrt{1+8} = 3$. Then, we need to calculate the derivative. The derivative is 
$$f'(x) = \frac{3x^2}{2\sqrt{1+x^3}}.$$
If we plug in $x=2$, we find that 
$$f'(2) = \frac{3(2^2)}{2\sqrt{1+8}} = 2.$$
Thus, the linear approximation is 
$$L(x) = 2 + 2(x-2).$$
</div> <br>

<div class="example">
<p><b>Example:</b> Calculate an approximate value of $\sqrt[3]{8.2}$. </p>
<b>Solution:</b> The first thing that we notice is that 8.2 is quite close to 8. The other thing we notice is that it is easy to evaluate the cube root of 8. It is simply $\sqrt[3]{8} = 2$. This means that we should consider the function $f(x) = \sqrt[3]{x} = x^{1/3}$, and do a linear approximation about $x = 8$. 

The derivative of $f$ is 

$$f'(x) = \frac{1}{3}x^{-2/3}, $$

and if we plug in $x=2$, we find that $f'(x) = \frac{1}{3}\frac{1}{8^{2/3}} = \frac{1}{12}$. Thus, the linear approximation is

$$L(x) = 2 + \frac{1}{12}(x-8).$$

To find an approximate value of $\sqrt[3]{8.2}$, we evaluate $L(8.2)$, which is

$$\begin{eqnarray*}
L(2) &=& 2 + \frac{1}{12}(8.2-8) \\
&=& 2 + \frac{1}{12}\frac{1}{5} \\
&=& \frac{121}{60}
\end{eqnarray*}$$

Using a computer, we can compare our approximation with the actual value. The actual value is $\sqrt[3]{8.2} = 2.01653$, and our approximation is $\frac{121}{60} = 2.01667$. The approximation is not bad, and differs from the actual value by about $0.008%$.
</div> <br>


### Differentials
Closely related to the linear approximations is the idea of differentials. We start with the definition. 

<div class="definition">
<b>Definition:</b> The <i>differential</i> of $y = f(x)$ is
$$dy = f'(x) dx.$$
</div>

What the differential allows us to do is find the small change in a function $y=f(x)$ given a small change in the independent variable $x$. This can be written more intuitively as 

$$\Delta y \approx f'(x) \Delta x.$$

In the figure, we see that $\Delta y$ is the actual change in $y$ when $x$ is increased by $dx$ (or $\Delta x$), but $dy$ is the approximate amount. 

<figure class="center">
<p><img src="linear_approximations_and_differentials-Figures/differential.svg" alt="differential" style="width:350px;height:250px;"> </p>
<figcaption class="center">The differential and actual difference given a change in the independent variable $x$.</figcaption> </figure>

This is a reason why we use the letter $d$ for derivative; the letter $d$ implies a change in something. This is essentially the same idea as for linear approximations, where we had $\Delta y = L(x) - f(x)$, and $\Delta x = x-a$. Now let's do some examples.

### Examples

<div class = "example">
<p><b>Example:</b> Compute the differential of the function $f(x) = e^{\sin x}$. </p>
<b>Solution:</b> The differential is simply
$$dy = \cos x e^{\sin x} dx.$$
</div> <br>

<div class="example">
<p><b>Example:</b> Suppose we have a spherical balloon whose volume is 1 cubic metre. If 0.05 cubic metres of air is let out of it, by how much does its radius change? </p>
<b>Solution:</b> To solve this problem, we identify that the formula relating the volume $V$ of a sphere to its radius $r$ is 
$$V = \frac{4\pi}{3} r^3.$$

Solving for the radius in terms of the volume gives us 

$$r = \left(\frac{3V}{4\pi}\right)^{1/3}.$$

Taking the differential of both sides gives us 

$$dr = \left(\frac{3}{4\pi}\right)^{1/3}\frac{1}{3}\frac{1}{V^{2/3}} dV.$$

If the volume changes by approximately 0.05 cubic metres, then, plugging in $dV = 0.05$ and $V = 1$, we find that 

$$dr = \left(\frac{3}{4\pi}\right)^{1/3}\frac{1}{3}0.05$$

If we change 0.05 to a fraction, our final answer (the amount by which the radius of the sphere changes) is

$$dr = \left(\frac{3}{4\pi}\right)^{1/3}\frac{1}{60}.$$
</div>











