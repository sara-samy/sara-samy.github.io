---
title: "margin test"
date: 2025-03-26
draft: false
math: true
---
look there.{{< sidenote >}}This is a sidenote.{{< /sidenote >}}
you could also want a margin note.{{< marginnote ind="⊕" >}}This is a margin note. Notice there isn’t a number preceding the note.{{< /marginnote >}}
{{< figure
  src="https://github.com/edwardtufte/tufte-css/raw/gh-pages/img/rhino.png"
  type="margin"
  label="mn-rhino"
  caption=`F.J. Cole, “The History of Albrecht Dürer’s Rhinoceros in Zooological Literature,” _Science, Medicine, and History: Essays on the Evolution of Scientific Thought and Medical Practice_ (London, 1953), ed. E. Ashworth Underwood, 337-356. From page 71 of Edward Tufte’s _Visual Explanations_.`
  ind="⊕"
  alt="Image of a Rhinoceros"
>}}


وَطِب نَفساً إِذا حَكَمَ القَضاءُ
وَلا تَجزَع لِحادِثَةِ اللَيالي
فَما لِحَوادِثِ الدُنيا بَقاء

Lorem ipsum dolor sit amet, consectetur adipiscing elit. In vel malesuada tortor. Duis interdum massa in dignissim volutpat. Sed odio massa, convallis sit amet ultrices iaculis, elementum non magna. Nunc aliquam nulla vel condimentum fermentum. Aliquam dignissim iaculis nulla, sit amet rutrum sapien. Maecenas felis mi, euismod in viverra ac, accumsan a magna. Nam quis mauris mi. Cras auctor laoreet elementum. Nunc lobortis finibus neque, ut semper nisl ornare sit amet. Proin laoreet dapibus risus ac auctor. Fusce scelerisque elementum purus, vel rhoncus magna faucibus vitae. Sed vitae sem finibus, rhoncus neque id, blandit purus. Duis mollis nulla in fermentum vehicula.

Vestibulum tincidunt egestas tempus. Integer congue lacus quis nunc volutpat, id accumsan lorem facilisis. Sed aliquam efficitur $L$ turpis. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Proin ornare maximus eros viverra volutpat. Ut scelerisque in quam nec imperdiet. Donec justo risus, egestas eu lacus sed, volutpat mattis nibh.

Aliquam quis nulla risus. Maecenas at velit vitae diam aliquam aliquam. Nam eleifend in dui a consectetur. Duis lorem turpis, sagittis sit amet nisi et, feugiat suscipit neque. Maecenas aliquam nisi vel pretium egestas. Integer tincidunt mi ac rutrum tristique. Duis non euismod augue. Donec bibendum sapien eget dolor $\int_{M} f \text{d}x$ ultricies, id consectetur mi interdum. Etiam ut magna diam. Nulla facilisi. Ut laoreet faucibus ex, id dignissim ipsum posuere eu. Ut auctor lectus vel justo semper hendrerit. Praesent posuere malesuada lectus, malesuada tempor massa pretium at. Fusce quis tortor eu erat aliquam vulputate. In eget lobortis diam.

$$
0 \leq \lambda_{2} \leq \dots \leq \lambda_{n} \leq n
$$

{{< theorem type="lemma" label="2.3" >}}
For any measurable function $f$, the $L^2$ norm satisfies:
$$ \|f\|_2 = \left( \int |f|^2 d\mu \right)^{1/2} $$
{{< /theorem >}}

{{< proof >}}
By the Cauchy-Schwarz inequality:
$$ \left| \int f \cdot g \right| \leq \|f\|_2 \cdot \|g\|_2 $$
Take $g = \overline{f}$ to obtain the result.
{{< /proof >}}

{{< theorem type="theorem" >}}
Let $G$ be a graph and $L$ Laplacian matrix with eigenvalues $\lambda_{1} \leq \lambda_{2} \leq \dots \leq \lambda_{n}$. Then $\lambda_{1} = 0$, i.e.
$$
0 \leq \lambda_{2} \leq \dots \leq \lambda_{n} \leq n
$$

with $\lambda_{2} > 0$ and $\lambda_{n} = n$ iff $G$ is connected.
If $G$ has $r$ connected components then $\lambda_{1} = \dots = \lambda_{r} = 0$, i.e. the multiplicity of the zero eigenvalue counts the number of connected components of $G$.
{{< /theorem >}}