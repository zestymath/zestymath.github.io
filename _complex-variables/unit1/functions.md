---
layout: lesson
title: Functions
dept: math
course: calculus-I
unit: unit1
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit I
---

### Introduction

In high school, we learn what functions are, but many people forget the formal definition by the time they reach university. In this lesson, we will review this definition, as well as the definitions of domain, range, and function notation. Additionally, we will introduce some definitions which are likely new to you, such as the codomain, image, and preimage. These terms will not be used too frequently in this course, but are useful to know especially if you study linear algebra in the future. 

### Definitions

<div class="definition">
<b>Definition:</b> Let $A$ and $B$ be sets. We say $f$ is a <i>function from $A$ to $B$</i> if to each element $x$ of $A$, there corresponds one and only one element $f(x)$ of $B$. This is written as $f : A\to B$. 
</div> <br>

This can be represented schematically by the following Figure 

<figure class="center">
<p><img src="functions-Figures/function.svg" alt="Function" style="width:350px;height:250px;"> </p>
<figcaption class="center">A function $f : A \to B$.</figcaption> </figure>

We call $A$ the domain of the function $f$, and $B$ the codomain. It is possible that not every element of $B$ is reached by the function $f$. For example, if we define $f : \R\to\R$ by $f(x) = x^2$, then, although the codomain is $\R$, we never actually reach the negative numbers. This leads us to the following definition.

<div class="definition">
<b>Definition:</b> Let $f:A\to B$ be a function. We define the <i>range</i> of $f$ to be 
$$\text{range}(f) = \{f(x) | x\in A\}.$$
</div> <br>

Closely related to the definition of range are the definitions of image and preimage. 

<div class="definition">
<b>Definition:</b> Suppose we have a function $f:A\to B$, and that $U$ is a subset of $A$. Then, we define 
$$f(U) = \{f(x)\in B | x\in U|\}$$
as the <i>image of $U$ under $f$</i>.
</div> <br>

<div class="definition">
<b>Definition:</b> Suppose we have a function $f:A\to B$, and that $V$ is a subset of $B$. Then, we define 
$$f^{-1}(V) = \{x\in A | f(x)\in V|\}$$ 
as the <i>preimage of $V$ under $f$</i>.
</div> <br>



### Examples

<div class="example">
<p><b>Example:</b> Consider $f : [2,4] \to \R$, where $f(x) = x^2$. 
<ol type = "a">
<li> What is the domain of $f$? </li>
<li> What is the codomain of $f$? </li>
<li> What is the range of $f$? </li>
</ol> </p>
<b>Solution:</b> 
<ol type = "a">
<li> </li>
<li> </li>
<li> </li>
</ol>
</div> <br>

<div class="example">
<p><b>Example:</b> Consider the function $f : \R\to\R$, where $f(x) = x^2$. Find the following sets.
<ol type = "a">
<li> $f([-1,1])$ </li>
<li> $f([0,1])$ </li>
<li> $f((0,\infty))$ </li>
<li> $f^{-1}([0,1])$ </li>
<li> $f^{-1}((0,1])$ </li>
<li> $f^{-1}([-2,-1])$ </li>
<li> $f^{-1}([-1,1])$ </li>
</ol> </p>
<b>Solution:</b> 
<ol type = "a">
<li> </li>
<li> </li>
<li> </li>
<li> </li>
<li> </li>
<li> </li>
<li> </li>
</ol>
</div>
