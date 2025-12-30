---
title: "Inference Maximizing Point Configurations for Parsimonious Algorithms"
collection: publications
category: conference-paper
permalink: /publication/2025-08-02-adg2025-parsimonious-efficacy-analysis
excerpt: 'This book chapter was written as part of a book being published by the Indian government on environmental instrumentation.'
date: 2025-08-02
venue: 'Automated Deduction in Geometry (ADG) 2025'
citation: 'Sharma, S., & Keyser, J. (2025) "Inference Maximizing Point Configurations for Parsimonious Algorithms", <i>Automated Deduction in Geometry (ADG) 2025</i>.'
---

This work was presented in [Automated Deduction in Geometry (ADG) 2025](https://www.uc.pt/events/adg/2025/accepted-papers-abstracts/) conference in Stuttgart, Germany. 
It came out of a larger body of work that we are currently doing on "_Hybrid Computational Geometry (HCG)_".
This approach combines the two over-arching approaches in Geometry: 
(1) Analytic Geometry (using coordinates and numbers) and 
(2) Synthetic Geometry (axiomatic/deductive without numbers).
HCG can make geometry algorithms more robust by replacing fragile numeric predicates with deductive proofs.
This approach was formalized by Donald Knuth in 1992 as "_Parsimonious Algorithms_" in his monograph called "_Axioms and Hulls_".

This current paper investigates the "_efficacy_" of parsimonious algorithms in real-world settings.
In doing so, we uncovered interesting combinatorial problems in Discrete Geometry linked to Erdős-class problems.
Hence, our efficacy analysis serves an extra purpose: it can offer novel approaches to improve bounds on these Discrete Geometry problems (but we haven't improved on those bounds yet).

+ [Read the paper to find more](../files/adg_2025_paper.pdf)
+ Or watch the [conference presentation video on YouTube](https://www.youtube.com/watch?v=yMTUejf4MxE)
+ Or find the associated code on [GitHub](https://github.com/shivams/parsimonious-efficacy)

We are currently working on a full paper version of this work which will appear in [AMAI special issue of ADG](https://www.uc.pt/events/adg/2025/amai-special-issue/).

## Abstract
Here is the abstract of the paper:
> We present an exploration of inferring orientations for point configurations. We can compute the orientation of every triple of points by a combination of direct calculation and inference from prior computations.  This "parsimonious" approach was suggested by Knuth in 1992, and aims to minimize calculation by maximizing inference.  We wish to investigate the efficacy of this approach by investigating the minimum and maximum number of inferences that are possible for a point set configuration.  To find the configurations which yield maximum inferences, there is no direct formula and hence two constructive approaches are suggested. A basic analysis of sequences that achieve those maximum inferences is also presented and some properties have been proved regarding their existence.


