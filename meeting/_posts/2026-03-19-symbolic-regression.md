---
layout: meeting
title: "Equality Saturation and Symbolic Regression"
speaker: "Prof. Fabrício Olivetti de França"
# hide: true # hide from calendar
# video link must normal youtube link
# video: https://www.youtube.com/watch?v=VIDEO_ID
---

[Fabricio](https://folivetti.github.io/) is a professor of Computer Science at UFABC currently working with the application of e-graphs in symbolic regression together with his colleague Gabriel Kronberger from the University of Applied Sciences Upper Austria.

### Abstract

Equation discovery, also known as symbolic regression, searches for a mathematical expression that describes observational data. This technique is mainly used in regression analysis and, also, to uncover the generating process of observable phenomena in physical sciences.
Symbolic regression methods suffer from an exploration inefficiency since there are many redundant expressions that are hard to detect except by evaluating them.
Equality saturation can be used in this context to store the set of already visited expressions and their equivalent forms helping to avoid redundant evaluation. Besides, the information gathered inside the e-graph can be used to enforce the creation of unique solutions.
In this talk we will show how to apply e-graphs and equality saturation to improve the search efficiency of symbolic regression methods. As a bonus application, we will show a Python library that allows the user to interactively explore the different models visited during the search, as a type of SQL-like database of mathematical expressions.
