---
title: "Reaction Solvability Analysis using Natural Coordinates"
collection: publications
category: conference
permalink: /publication/2019-12-06-reaction-solvability-natural-inacommm
excerpt: 'This conference paper comes from my MSc work on over-constrained mechanisms'
date: 2019-12-06
venue: '4th International and 19th National Conference on Machines and Mechanisms (iNaCoMM 2019)'
paperurl: 'http://shivams.github.io/files/inacomm19Paper.pdf'
citation: 'Sharma, Shivam & Ghosal, Ashitava (2019) &quot;Reaction Solvability Analysis using Natural Coordinates&quot;, <i>4th International and 19th National Conference on Machines and Mechanisms (iNaCoMM 2019)</i>, IIT Mandi, 5-7 December. Association for Machines and Mechanisms.'
---
This paper was presented in an international conference in Machines and Mechanisms. It comes out of my Master's dissertation work submitted in IISc Bangalore in 2017 (and defended in 2019).

### Downloads

[Download paper here](../files/inacomm19Paper.pdf)

[Download full thesis here](../files/thesis.pdf)

[Source code of various programs written](https://github.com/shivams/iisc-masters-thesis-codes/)

### Overview of Thesis

This work was a theoretical work in multi-rigid-body dynamics and provided a new modeling approach to an existing
problem in this field, enabling the problem to be solved symbolically, while earlier work had solved the problem numerically. Solving this problem boiled down to doing matrix computations (finding rank of the Jacobian matrices), and our approach yielded matrices with linear terms which otherwise would have transcendental terms. This made the symbolic computation much faster. This work was presented in an international conference in our field in December 2019 and will soon be published in the proceedings. The algorithm was implemented using Mathematica, and several auxiliary Python codes were written to assist in our work:

* Python program to automatically generate constraint equations to be fed into Mathematica
* Python program to generate the CAD model of a multi-body system
* Python program for forward-kinematics using Quaternions
* Python library for symbolic computation using Quaternions

Another work that was attempted to improve the performance was to use Quaternions and Geometric Algebra for modeling. We had explored many other geometrical techniques like Screw Theory and 6D vectors. However, no significant computation gains were visible and it was taking time to adapt the algorithms to the new geometry, so we suspended this work. Some of the work on Quaternions was put in the Appendix.