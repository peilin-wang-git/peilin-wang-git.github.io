---
layout: post
title: "Congratuations! My paper has been published in Scientific Reports on 17 January 2023"
author: "Peilin Wang"
categories: RP
tags: [RP,documentation]
image: paper1-1.jpg
---

# Combining multi-objective genetic algorithm and neural network dynamically for the complex optimization problems in physics
<br/>
## Introduction

This work proposed a new multi-objective optimization algorithm which is call DNMOGA. In this algorithm, neural network was combined dynamically to speed up convergence of the general MOGAs. Remarkably, when We utilized this algorithm to optimize the shape of cavities, the solutions with better preference were obtained comparing with the baseline algorithms.

<br/>
## Abstract

Multi-objective genetic algorithms (MOGAs) whose advantages lie in optimizing several objectives simultaneously and obtaining a set of competitive individuals are widely used in physical research nowadays. By estimating more individuals, neural network (NN) has been tentatively combined into MOGAs in recent years to further improve their performance. However, because of the unsatisfied size of training set which is caused by the computationally complex evaluations and limited computing resources, these combinations do not suit such scenarios that have equality constraints or other strict constraints. Here, the dynamically used NN-based MOGA (DNMOGA) is proposed for the first time. 
<br/>
The penalty operation which can be progressively rigorous over generations is used in this algorithm, as part of the fitness function to make individuals fulfill constraints gradually. Moreover, a new way to combine NN and MOGA is proposed, in which NN is included in an operator that coincides with the operators of mutation and crossover to produce a series of individuals, and these individuals will be further evaluated. The numbers of individuals that come from different operators are dynamically redistributed based on the performance of these operators in the previous generation. In addition, accessibility algorithm is introduced to solve the preference of the objectives in this work, without the extra reference points used in other algorithms to lead the nondominated front to approach these points. The flow chart of DNMOGA is shown above.
<br/>
Radio frequency cavity is designed by this algorithm as an example, in which four objectives ($$R/Q_FM$$, $$Ra_FM$$, $$abs(f_HOM-f_FM)$$, and $$R/Q_HOM$$) and an equality constraint (abs(f_BM-499.65 MHz) <= 0.05 MHz) are considered simultaneously. As a result, DNMOGA considerably improves both the number and competitiveness of the final feasible individuals, and shows the potential to completely replace the manual procession in this question. The nondominated fronts of different algorithms in the last generation are shown here.
<!-- ![Profile Picture](https://github.com/peilin-wang-git/peilin-wang-git.github.io/tree/main/assets/img/paper1-2.jpg)  -->
![Profile Picture](https://github.com/peilin-wang-git/peilin-wang-git.github.io/raw/main/assets/img/paper1-2.jpg)
Then the individuals that have the similar frequency of the HOM are signaled and picked up from different algorithms. The indicators of these individuals are shown in the table below, in which the advantage of DNMOGA can be discovered. The R/Q_FM is improved by about 24% and 14% compared with using the NBMOGA and NSGA-II, while the Ra FM is increased by approximately 55% and 22% respectively. Besides, only the R/Q_HOM that comes from the individual of DNOMGA tends to zero, which is beneficial for further analysis of HOM. The geometric parameters of the individual from DNMOGA are shown in the last sub-figure above.

Algorithm             | R/Q_FM [Ω]            | Ra_FM [MΩ]            | f_HOM [MHz]           | R/QHOM [Ω]
:-------------------: | :-------------------: | :-------------------: | :-------------------: | :--------------------:
DNMOGA                | 324.72                | 12.15                 | 826.75                | 8.28E-7
NBMOGA                | 261.09                | 7.82                  | 806.46                | 9.46
NSGA-II               | 284.54                | 9.93                  | 800.56                | 18.58

In general, DNMOGA is instructive for dealing with the complex situations of strict constraints and preference in multi-objective optimization problems in physics.

<br/>
## Read the original

To read the original paper, please [press here](https://www.nature.com/articles/s41598-023-27478-7).


