---
title: "Reaction Solvability Analysis of Over-constrained mechanisms using Natural Coordinates"
collection: publications
category: conference-paper
permalink: /publication/2019-12-06-reaction-solvability-natural-inacommm
excerpt: 'This conference paper comes from my MSc work on over-constrained mechanisms'
date: 2019-12-06
venue: '4th International and 19th National Conference on Machines and Mechanisms (iNaCoMM 2019)'
paperurl: 'http://shivams.github.io/files/inacomm19Paper.pdf'
citation: Sharma S., Ghosal A. (2022) Reaction Solvability Analysis Using Natural Coordinates. In: Kumar R., Chauhan V.S., Talha M., Pathak H. (eds) Machines, Mechanism and Robotics. Lecture Notes in Mechanical Engineering. Springer, Singapore. https://doi.org/10.1007/978-981-16-0550-5_94 
---
This paper was presented in an international conference in Machines and Mechanisms in December 2019, and has been published in the proceedings by Springer (2022). It comes out of my Master's dissertation work done in IISc Bangalore during 2013-15 (and defended in 2019).

### Brief Overview of Thesis (for non-Mechanical Engineering readers)

This work provided a new modeling approach to an existing problem in multi-rigid-body dynamics, enabling the problem to be solved symbolically, while earlier work had solved the problem numerically. Solving this problem boiled down to matrix computations (finding rank of the Jacobian matrices), and our approach yielded matrices with linear terms which otherwise would have transcendental terms. This made the symbolic computation much faster.

Another work that was attempted to improve the performance was to use Quaternions and Geometric Algebra for modeling. However, no significant computation gains were visible and it was taking time to learn and adapt the algorithms to the new geometrical techniques, so we suspended this work. Some of the work on Quaternions was put in the Appendix. Finally, we attempted to delve into the symbolic algorithms of Mathematica (our preferred symbolic solver), but this was beyond the scope.

### Detailed Overview of Thesis 

This work deals with a special class of mechanisms, called **over-constrained mechanisms**, where the reactions at the joints can not be calculated uniquely under rigid body assumptions. For such mechanisms, simulation softwares discard the rigid body assumptions, consider the links as flexible by bringing in the material constitutive equations, and solve the problem using Finite Element Analysis (FEA). In recent work, researchers had suggested algorithms to find a subset of reactions in such mechanisms which can be solved uniquely under rigid body assumptions. If our reactions of interest lie in this subset, then FEA can be avoided. This analysis is called Reaction Solvability Analysis (RSA) and the algorithms for RSA boil down to the investigation of the Jacobian matrix of the over-constrained mechanism (hence matrix computations).

Our goal was to implement these numerical algorithms symbolically. This would not only generalize the solutions, but also obviate the need of finding a valid numerical configuration to be fed into the RSA algorithm (by solving computationally expensive loop-closure equations). Applying the existing RSA algorithms naively in a symbolical fashion was computationally expensive as the matrices had transcendental terms and consequently Mathematica's solvers struggled. We proposed a new modeling approach using Natural Coordinates (or Fully Cartesian Coordinates). This made the matrices larger but with only linear terms. Symbolic solvers now performed much better. This work finally formed the central part of this thesis and was presented in an international conference. This RSA methodology was tested on various mechanisms and a comparison was made of their efficiency under different coordinate formulations. The constrained dynamics equations were also derived and from the simulations, the joint reactions for the uniquely solvable joints were obtained as a function of time.

There were other approaches that were attempted but later discarded. First, we explored using different geometrical constructs (e.g. Geometric Algebra, Quaternions, Screw Theory, 6D Vectors etc.) for modeling the mechanisms. No significant gains were visible and there was a learning curve associated. Hence, the work was suspended. Second, we attempted going into the symbolic algorithms of Mathematica itself but this proved to be even more challenging (and also inaccessible) for our lack of expertise. This can be a future problem statement for a computer scientist. 

### Auxiliary Contributions

The algorithm was implemented using Mathematica, and several auxiliary Python codes were written to assist in our work:

* Python program to automatically generate constraint equations to be fed into Mathematica
* Python program to generate the CAD model of a multi-body system
* Python program for forward-kinematics using Quaternions
* Python library for symbolic computation using Quaternions

### Downloads

[Download paper here](../files/inacomm19Paper.pdf)

[Download full thesis here](../files/thesis.pdf)

[Source code of various programs written](https://github.com/shivams/iisc-masters-thesis-codes/)

[Springer Proceedings Link](https://link.springer.com/chapter/10.1007/978-981-16-0550-5_94)

### Trivia (Motivation)

This problem was motivated in 2012/13 when [my undergraduate project on bicycles](/projects/2012-tire-inflation-bicycle/) had me confounded, for I realized that we didn't understand (all these 150 years!) how bicycles are balanced. It was surprising that the "*a-priori*" framework of rigid bodies failed at deducing this understanding. I wanted to test the limits of this *a-priori* framework to test how much we could do using this framework, without going into the "*a-posteriori*" material constitutive equations. In a way, I "*over-constrained*" myself to rigid-body systems!
