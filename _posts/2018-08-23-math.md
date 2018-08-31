---
title: 'Linear Algebra Essentials to Differential Geometry'
date: 2018-08-23
permalink: /posts/2018/linear-algebra-1/
tags:
  - math
  - linear algebra
---

This is my first notes w.r.t. differential geometry study, from the book "*first steps in differential geometry*", This is only the linear algebra part. Noted: this book is pretty succint in Linear Algebra part, so I'll try to understand it by my own. 

## Dual of a vector space, forms and pullbacks

This section corresponds to chapter 2.8.

### Dual of a vector space, aka. one-form, covector

Given V as a vector, its corresponding dual form is a map from V to R:
$V^* = V\to R$. Further, $$V^*$$ could be regarded as a dot-product.
Then, given $v\in R^2, T\in R^{2*}, T\circ v \in R$.  We
could think of T as another $R^2$ vector, and the computation is dot-product. [This is supported by Theorem 2.9.22 later]

### Connection between one-form $T\in V^*$ and  vector space $V$

* Let $B=\{e_1,...e_n\}$ be a basis for V, then the basis for $$V^*$$ is $$B^*=\{ \epsilon_1,...,\epsilon_n  \}$$, s.t.
  * $\epsilon_i (e_i)=1$ and $\epsilon_i (e_j)=0$ for $j\neq i$ 
* Then, $T=\sum_i T(e_i)\epsilon_i$ 
* Intuition is very easy: let $\epsilon_i = e_i$, and they're all orthonormal basis, while treating one-form mapping as dot-product.

### Pullbacks

Projection ($\Phi$) is a map from v to w, could be regarded as a matrix $\in R^{n\times m}$, while $v\in R^n, w\in R^m$. Then pullback($\Phi^\star$) is a map from $w^\star$ back to $v^\star$, while they're all covectors.  A pullback could be regarded as the transpose of the corresponding projection matrix, namely, $\Phi^\star = \Phi^T$.

Pullback is defined this way:
$$(\Phi^*(T))(v) = T(\Phi(v))$$, where $$T\in W^*$$ and $$v\in V$$.
In the math understanding:

* left: pullback $$T\in w^*$$ to $$\Phi(T)\in v^*$$, then apply "dot-product" to v.
* right: project $v\in V$ to $w\in W$, then apply $$w^*\in W^*$$ to it, and get a real value.

While in the matrix understanding:

* Left = $$(\Phi^*\circ T)^T \circ v$$

* right=$T^T\circ ( \Phi\circ v )$

We could easily observe that they are equal. Noted: every time we apply dot-product, we need to transpose the former vector.

Then, we can understand $$(\Phi_2\circ \Phi_1)^* = \Phi_1^*\circ \Phi_2^*$$, by transpose of matrix multiplication.

### Two-forms (aka. Bilinear Form) and Its Pullbacks

Since one-form ($$V\to R$$) could be regarded as dot-product (with a vector), two-form ($b \in V\times V \to R$) could be regards as a bilinear operation (with a matrix): $b(v,w) = w^TBv$, and $B$ is its corresponding matrix.

Pullbacks of bilinear forms is of type $(W\times W \to R) \to (V\times V \to R)$ , and defined by:   
$$  (T^*B)(v_1,v_2) = B(T(v_1), T(v_2)) $$ where $T\in V\to W$ and $B\in W\times W \to R$.

### Inner product space

Inner product space is just the normal/standard space, where norm, angle are defined. Also, the orthonormal basis of a inner product space $(V,G)$ is the same as that of $V$, where $V$ is vector space, and $G$ is a bilinear form ($V\times V\to G$).

## Linear Symplectic Forms

Linear symplectic form, also known as alternating bilinear form, has a different property with bilinear form:

* Skew-symmetric: for all $v,w\in V$, $\omega(w,v) = -\omega(v,w)$ 

It has an intuition of cross-product.