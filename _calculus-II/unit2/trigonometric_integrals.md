---
layout: lesson
title: Trigonometric Integrals
dept: math
unit: unit2
course: calculus-II
deptDisplay: Math
unitDisplay: Unit 2
courseDisplay: Calculus II
---

In this section, we will discuss how to evaluate trigonometric integrals, or, integrals involving just trigonometric functions. There are a few broad categories that these integral fit in to; some are easy and some are hard. In this section, $m$ and $n$ will be integers. Note that no matter what $n$ is, $2n+1$ is always an odd integer! Thus, if we want to say "sine raised to an odd power", we could write $\sin^{2n+1}x$. If want to say "sine raised to an even power", we could write $\sin^{2n}x$. 

### Easy Trigonometric Integrals
Let $m$ and $n$ be integers. The following integrals can be solved with the corresponding $u$-substitutions. 

<table style="width:100%">
<tr>
<th>Integral</th>
<th>Substitution</th>
</tr>
<tr>
<td>$$\int \cos^m x \sin^{2n+1} x dx$$ </td>
<td>$$u = \cos x$$</td> 
</tr>
<tr>
<td>$$\int \sin^m x \cos^{2n+1}x dx$$ </td>
<td>$$u =\sin x$$</td> 
</tr>
<tr>
<td>$$\int \tan^m x \sec^{2n}x dx$$ </td>
<td>$$u = \tan x$$</td>
</tr>
<tr>
<td>$$\int \sec^m x \tan^{2n+1}x dx$$ </td>
<td>$$u =\sec x$$</td> 
</tr>
<tr>
<td>$$\int \cot^m x \csc^{2n}x dx$$ </td>
<td>$$u =\cot x$$</td> 
</tr>
<tr>
<td>$$\int \csc^m x \cot^{2n+1}x dx$$ </td>
<td>$$u =\csc x$$</td> 
</tr>
</table>

### Examples for Easy Trigonometric Integrals

<div class="example">
<p><b>Example:</b> Calculate the following integral
$$\int \sin^3 x \cos^3 x dx$$ </p>
<b>Solution:</b> This integral is actually both of the first two forms because the power of the cosine and the power of the sine are both odd. This means that we can choose to make the either the substitution $u = \cos x$ or $u = \sin x$; both will work. Let's choose $u = \sin x$. This makes $du = \cos x dx$. Rewriting our integral as
$$\int \sin^3 x \cos^2 x (\cos xdx),$$
we can use the identity $\cos^2 x = 1-\sin^2 x$ to get 
$$\int \sin^3 x (1-\sin^2 x) (\cos xdx).$$
Now substituting $du = \cos x dx$ and $\sin x = u$, we get 
$$\int \sin^3 x (1-\sin^2 x) (\cos xdx) = \int u^3 (1-u^2)du = \int (u^3 - u^5) du.$$
Lastly, we integrate 
$$\int (u^3 - u^5)du = \frac{u^4}{4} - \frac{u^6}{6}.$$
Thus, substituting back in $u = \sin x$, 
$$\int \sin^3 x \cos^3 x dx = \frac{1}{4}\sin^4 x - \frac{1}{6}\sin^6 x + C$$ 
</div> <br>

<div class="example">
<p><b>Example:</b> Calculate the following integral 
$$\int \sec^4 x \tan^3 x dx $$</p>
<b>Solution:</b> To solve this problem, we notice that this is of the form secant to an even power, and the power of tangent can be anything. Rewriting the integral as 
$$\int \sec^4 x \tan^3 x dx  = \int \sec^2 x \tan^3 x (\sec^2 xdx) = \int (1+\tan^2 x) \tan^3 x (\sec^2 x dx),$$
we make the substitution $u = \tan x$, $du = \sec^2 x dx$. Thus,
$$\int (1+\tan^2 x) \tan^3 x (\sec^2 x dx) = \int (1+u^2)u^3 du = \int(u^3 + u^5) du$$
We can simply integrate this function:
$$ \int(u^3 + u^5) du = \frac{u^4}{4} + \frac{u^6}{6} $$
If we substitute back in $u = \tan x$, then the final answer is 
$$\int \sec^4 x \tan^3 x dx = \frac{1}{4}\tan^4 x + \frac{1}{6}\tan^6 x + C$$
</div> <br>

<div class="example">
<p><b>Example:</b> Calculate the following integral 
$$\int \sec^2 x \tan^3 x dx $$</p>
<b>Solution:</b> This integral has the form of odd power of tangent, and the power of secant can be anything. We rewrite the integral
$$\int \sec^2 x \tan^3 x dx = \int \sec x \tan^2 x(\tan x \sec x dx) = \int \sec x (\sec^2 x - 1)(\tan x \sec x dx)$$
Next, we make the substitution $u = \sec x$, $du = \tan x \sec x dx$. Thus the integral is 
$$\int \sec x (\sec^2 x - 1)(\tan x \sec x dx) = \int u(u^2 - 1) du = \int(u^3 - u)du.$$
This is now easy to integrate, and we get 
$$\int(u^3 - u)du = \frac{u^4}{4} - \frac{u^2}{2}$$
Lastly, substituting back in $u = \sec x$, 
$$\int \sec^2 x \tan^3 x dx = \frac{1}{4}\sec^4 x - \frac{1}{2}\sec^2 x + C$$
</div> <br>

### Hard Trigonometric Integrals
The integrals in this section will often lead to problems involving partial fractions, which we will cover later. The only one which I will show how to calculate in this section is the one with sines and cosines; the others are too difficult at this point and will be postponed until we have learned about partial fractions. These integrals are 

<table style="width:100%">
<tr>
<th>Integral</th>
<th>Strategy</th>
</tr>
<tr>
<td>$$\int \cos^{2m}x \sin^{2n}x dx$$ </td>
<td>Use the identity $\sin^2x + \cos^2 x = 1$ then double angle formula</td> 
</tr>
<tr>
<td>$$\int \sec^{2m+1} x \tan^{2n}x dx$$ </td>
<td>$u =\sin x$</td> 
</tr>
<tr>
<td>$$\int \csc^{2m+1} x \cot^{2n}x dx$$ </td>
<td>$u = \tan x$</td>
</tr>
</table>

### Examples for Hard Trigonometric Integrals

<div class="example">
<p><b>Example:</b> Evaluate the integral
$$\int \sin^2 x \cos^2 x dx$$ </p>
<b>Solution:</b> To solve this problem, we need to apply a trigonometric identity. Let's use $2\sin x \cos x = \sin(2x)$. This gives us 
$$\int \sin^2 x \cos^2 x dx = \int \frac{1}{4}\sin^2(2x) dx$$
Now, we need to use the double angle formula 
$$\sin^2\theta  = \frac{1-\cos(2\theta)}{2},$$
which gives us 
$$\int \frac{1}{4}\sin^2(2x) dx = \frac{1}{4}\int \frac{1-\cos(4x)}{2}dx$$
Finally integrating this gives 
$$\frac{1}{8}\int (1-\cos(4x))dx = \frac{x}{8} - \frac{1}{32}\sin x + C$$
</div>
