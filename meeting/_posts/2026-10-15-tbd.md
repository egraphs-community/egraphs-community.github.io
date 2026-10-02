---
layout: meeting
title: "Versioned E-Graphs (and more!)"
speaker: "Jahrim Gabriele Cesario and George Zakhour"
# draft: true # hide from calendar and page
# hide: true # hide from calendar
# video link must normal youtube link
# video: https://www.youtube.com/watch?v=VIDEO_ID
---

E-graphs were first introduced as a data structure for equational reasoning in
theorem provers. Yet proofs often require reasoning beyond plain equalities,
such as disequalities or conditional equalities, where e-graph support is still developing.

In this talk, we present [Versioned E-Graphs](https://dl.acm.org/doi/10.1145/3808249)
for conditional reasoning. Versioned e-graphs efficiently encode multiple equivalence
relations (versions) in a single structure by sharing e-nodes and equalities across versions. We discuss the challenges they raise, such as termination, and how these shape our algorithms.

We then demonstrate their applicability through proof production in our
prototype inductive prover [Vegie](https://github.com/gzakhour/vegie).

We conclude with future extensions that can benefit the theorem-proving
ecosystem, such as richer relations between versions and parallelism, developed as part of our
[Smart E-Graphs](https://prg-grp.github.io/egraphs-extensions-website) project.
```
