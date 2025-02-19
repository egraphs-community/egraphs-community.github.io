---
layout: meeting
title: "Hardware Decompilation: Recovering Abstraction in Digital Circuits"
author: Zach Sisco
---

Zach will present his work on hardware decompilation, leveraging equality saturation.

### Abstract

Hardware description languages (HDLs) are the core drivers for chip development today. Compiling, or "synthesizing", HDL code produces a netlist, a flattened graph of wires and logic gates. After synthesis, a netlist loses all of the high-level abstractions from the HDL code and is considerably larger. Despite this, netlists are the lingua franca for generating and distributing IP blocks for hardware design. To reuse and incorporate these blocks, designers must be able to reason about their implementation, behavior, and relationships to higher-level specifications. All of these tasks are made easier if the IP is represented as HDL code rather than netlists.

To this end, I have established an area of research called hardware decompilation, which lifts a netlist into semantically equivalent HDL code at a higher level abstraction. In this talk, I will introduce what hardware decompilation is and how I have incorporated equality saturation techniques to restructure and optimize netlists into higher-level HDL code. I will present one solution for recovering memory blocks in gate-level netlists, highlighting how equality saturation has helped solve different aspects of the problem.

### Bio

Zachary Sisco is a PhD candidate at the University of California, Santa Barbara, advised by Jonathan Balkind and Ben Hardekopf. He conducts research at the intersection of programming languages and computer architecture, integrating formal methods into open-source languages for chip design to increase developer agility with correctness guarantees. To learn more about his work, please visit his [website](https://zsisco.net/).
