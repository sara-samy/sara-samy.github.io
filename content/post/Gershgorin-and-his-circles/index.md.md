---
title: Gershgorin and his circles
date: 2025-04-25
draft: false
math: true
---

A very nice theorem I love from linear algebra is the _Gershgorin circle theorem_ which relates the spectrum of a $(n \times n)$-complex matrix to $n$ disks in the complex plane. Given $A \in \mathbb{C}^{n \times n}$ with spectrum{{< sidenote >}}A complex number $\lambda \in \mathbb{C}$ is an eigenvalue of $A$ if and only if there exists $v \in \mathbb{C}^{n}$ with $v \neq 0$ such that 
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
Let $A \in \mathbb{C}^{n \times n}$ Then
$$
\sigma(A) \subseteq \bigcup_{i=1}^{\ \ n} D_{i}(A)
$$
{{< /theorem >}}
{{< iframe src="/widgets/gersgorin_plot.html" >}}