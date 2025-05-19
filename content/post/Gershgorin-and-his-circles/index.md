---
title: Gershgorin and his circles
date: 2025-04-25
show_date: true
draft: false
mathjax: true
featured_image: img/Gershgorin-and-his-circles.png
image_alt: Gershgorin-and-his-circles.png
---

A theorem I love from linear algebra is the _Gershgorin circle theorem_ which relates the spectrum of a $n \times n$ complex matrix to $n$ disks in the complex plane. Given $A \in \mathbb{C}^{n \times n}$ with spectrum{{< sidenote >}}A complex number $\lambda \in \mathbb{C}$ is an eigenvalue of $A$ if and only if there exists $v \in \mathbb{C}^{n}$ with $v \neq 0$ such that
$$
Av = \lambda v
$$or equivalently, $(A - \lambda I_{n})v = 0$. This implies that $A - \lambda I_{n}$ is a singular matrix.{{< /sidenote >}}
$$
\sigma(A) = \\{ \lambda \in \mathbb{C} \ : \ \det(A - \lambda I_{n}) = 0 \\}
$$
we define $r_{i}$ to be the absolute row sum of the $i$-th row of $A$ with the diagonal entry $a_{ii}$ deleted, i.e.
$$
r_{i} := \sum_{j \neq i} \lvert a_{ij} \rvert
$$
The closed disk in the complex plane
$$
D_{i} = \\{ z \in \mathbb{C} \ : \ \\lvert z-a_{ii} \\rvert \leq r_{i} \\}
$$
with center $a_{ii}$ and radius $r_{i}$ is the _$i$-th Gershgorin disk_. The original result of Gershgorin states that the spectrum of $A$ is completely contained in the collection of all such disks.{{< sidenote >}}This collection is called  the _Gershgorin set_ which is closed and bounded in $\mathbb{C}$.{{< /sidenote >}}

{{< theorem type="theorem" label="Gershgorin circle theorem" >}}
Let $A = [a_{ij}]\_{i,j=1,\dots,n} \in \mathbb{C}^{n \times n}$ be a complex square matrix with spectrum $\sigma(A)$. Then, for every eigenvalue $\lambda \in \sigma(A)$ there exists an index $k \in \\{1,\dots, n\\}$ such that
$$
\lvert \lambda - a_{kk} \rvert \leq r_{k}(A)
$$
i.e., $\lambda$ lies in the Gershgorin disk $D_{k}(A)$. Consequently,
$$
\sigma(A) \subseteq \bigcup_{i=1}^{\ \ n} D_{i}(A)
$$
{{< /theorem >}}
{{< details summary="Show Proof." >}}
Let $\lambda$ be an eigenvalue of $A$ with eigenvector $v \in \mathbb{C}^n$. Since $v \neq 0$ we must have
$$
0 < \lvert v_{k} \rvert = \max\\{ \lvert v_{i} \rvert \ : \ i=1,\dots,n \\} = \lVert v \rVert_{1}
$$
for some $k \in \\{1,\dots,n \\}$. Using index notation we can write
$$
\sum_{j=1}^{\ \ \ n} a_{kj} v_{j} = \lambda v_{k}
$$
or equivalently,
$$
(\lambda - a_{kk}) v_{k} = \sum_{j \neq k} a_{kj} v_{j}
$$
Taking the absolute values in the above equation and using the triangle inequality we get
$$
\left\lvert \lambda - a_{kk} \right\rvert \lvert v_{k} \rvert = \left\lvert \sum_{j \neq k} a_{kj} v_{j} \right\rvert \leq \sum_{j \neq k} \lvert a_{kj} v_{j} \rvert \leq \lvert v_{k} \rvert \sum_{j \neq k} \lvert a_{kj} \rvert = \lvert v_{k}  \rvert r_{k}(A)
$$
Dividing by $\lvert v_{k} \rvert$ gives $\lvert \lambda - a_{kk} \rvert \leq r_{k}(A)$.
{{< /details >}}

If we construct a family of matrices where the diagonal entries (which determine the centers of the circles) and the off-diagonal entries (which determine the radii) vary smoothly, we can use Gershgorin's theorem to create some pretty plots!

Below is a plot of the Gershgorin sets of the one-parameter family of matrices $A_{t}$ with diagonal elements{{< sidenote >}}The $k$-th diagonal entry traces a unit circle in the complex plane $t \mapsto e^{2k\pi it}$.{{< /sidenote >}}
$$
a_{kk} = e^{2k\pi it}
$$
and off-diagonal elements that sum to one. This ensures that all circles have the same size and overlap. You can use the slider below to vary $t \in [0, 1]$.

{{< iframe src="/widgets/gersgorin_plot.html" >}}
