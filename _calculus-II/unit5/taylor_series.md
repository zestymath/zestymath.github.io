---
layout: page
title: Taylor Series
dept: math
course: calculus-II
unit: unit5
deptDisplay: Math
courseDisplay: Calculus II
unitDisplay: Unit 5
---

Suppose we are interested in approximating a function $f(x)$ about a certain point $x = a$. Well, a very crude approximation might be $f(x) \approx f(a)$. This is a constant, and it only really works when $x = a$. This isn't a very good approximation if it only works for a single value of $x$. 

As we saw earlier in the course, we could try making a linear approximation to $f$ at $a$. This would look like
 
 $$f(x) \approx f(a) + f'(a)(x-a)$$
 
 Now, our approximation matches the function at $a$, and its derivative also matches the function at $a$. We can still do better. Adding a quadratic term improves the approximation even more!
 
 $$f(x) \approx f(a) + f'(a)(x-a) + \frac{f''(a)(x-a)^2}{2}$$
 
 This sequence of increasingly accurate approximations can be visaulized in the following graph:
 
 (insert picture here)
 
 
 This sequence of increasingly accurate approximations is known as a sequence of Taylor polynomials, which we have covered a little bit before. Here, we develop Taylor series, which allow us to approximate a function over a wide range. It will in fact allow us to establish an equality instead of an approximation:
 
 $$f(x) = \sum_{n = 0}^\infty c_n (x-a)^n.$$
 
 Now we can calculate the coefficients $c_n$. Consider differentiating the equation $k$ times:
 
 $$f^{(k)}(x) = \sum_{n=k-1}^\infty c_n \frac{n!}{(n-k)!} (x-a)^{n-k}$$






