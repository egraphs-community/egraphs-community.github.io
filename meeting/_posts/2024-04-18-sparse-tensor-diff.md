---
layout: meeting
title: Sparse Tensor Algebra Compilation using Equality Saturation
speaker: Amir Shaikhha
---

[Amir Shaikhha](https://amirsh.github.io/)
 will present their recent work (from [CGO 2024](https://conf.researchr.org/info/cgo-2024/accepted-papers))
 on [A Tensor Algebra Compiler for Sparse Differentiation](https://arxiv.org/pdf/2303.07030.pdf).

## Abstract:
Tensor programs often need to process large tensors (vectors, matrices, or higher-order tensors) that require a specialized storage format for their memory layout. Several such layouts have been proposed in the literature, such as the Coordinate Format, the Compressed Sparse Row format, and many others, that were especially designed to optimally store tensors with specific sparsity properties. However, existing tensor processing systems require specialized extensions in order to take advantage of every new storage format. In this paper, we describe a system that allows users to define flexible storage formats in a declarative tensor query language similar to the language used by the tensor program. The programmer only needs to write storage mappings, which describe, in a declarative way, how the tensors are laid out in main memory. Then, we describe a cost-based optimizer that optimizes the tensor program for the specific memory layout. Additionally, our design enables automatic differentiation (AD) of sparse tensors; state-of-the-art tensor frameworks only support the AD computation for dense tensors, which results in substantial memory and computational overheads. We demonstrate empirically significant performance improvements compared to state-of-the-art tensor processing systems.

## Bio:
Amir Shaikhha is an Assistant Professor (Lecturer) in the School of Informatics at the University of Edinburgh. His research focuses on the design and implementation of data-analytics systems by using techniques from databases, programming languages, compilers, and machine learning communities. Prior to that, he was a Departmental Lecturer at Oxford. He earned his Ph.D. from EPFL in 2018, for which he was awarded a Google Ph.D. Fellowship in structured data analysis, as well as a Ph.D. thesis distinction award. He has won the Best Paper Award at GPCE 2017 and the Most Reproducible Paper Award at SIGMOD 2017. He (co-)chaired the program committees of DBPL 2021, Scala 2022, and GPCE 2023.
