---
layout: post
title: "Paper Reading: 'UniverSeg: Universal Medical Image Segmentation'"
author: "Peilin Wang"
categories: RI
tags: [RI,documentation]
image: paper-reading-1-1.jpg
---

# [UniverSeg: Universal Medical Image Segmentation] (https://universeg.csail.mit.edu/)
<br/>
## Introduction

This study introduces a novel medical image segmentation model named UniverSeg, designed to effectively segment images encompassing diverse anatomies, image modalities, or labels that extend beyond the boundaries of the training dataset. UniverSeg is rooted in the principles of meta learning and few-shot learning, thereby shifting the paradigm of training deep-learning models from merely 'learning to reflect' to the more sophisticated concept of 'learning to learn'. Concurrently, the architecture of UniverSeg draws inspiration from the UNet model, leveraging its structural attributes to enhance segmentation capabilities. By combining the advancements of meta and few-shot learning with the foundational framework of UNet, UniverSeg represents a pioneering approach in addressing the challenges of versatile medical image segmentation tasks.

KEY WORDS: Meta learning, UNet model.

<br/>
## What is Meta Learning?

Multi-objective genetic algorithms (MOGAs) whose advantages lie in optimizing several objectives simultaneously and obtaining a set of competitive individuals are widely used in physical research nowadays. By estimating more individuals, neural network (NN) has been tentatively combined into MOGAs in recent years to further improve their performance. However, because of the unsatisfied size of training set which is caused by the computationally complex evaluations and limited computing resources, these combinations do not suit such scenarios that have equality constraints or other strict constraints. Here, the dynamically used NN-based MOGA (DNMOGA) is proposed for the first time. 
<br/>
The penalty operation which can be progressively rigorous over generations is used in this algorithm, as part of the fitness function to make individuals fulfill constraints gradually. Moreover, a new way to combine NN and MOGA is proposed, in which NN is included in an operator that coincides with the operators of mutation and crossover to produce a series of individuals, and these individuals will be further evaluated. The numbers of individuals that come from different operators are dynamically redistributed based on the performance of these operators in the previous generation. In addition, accessibility algorithm is introduced to solve the preference of the objectives in this work, without the extra reference points used in other algorithms to lead the nondominated front to approach these points. The flow chart of DNMOGA is shown above.
<br/>
Radio frequency cavity is designed by this algorithm as an example, in which four objectives ($$R/Q_{FM}$$, $$Ra_{FM}$$, abs($$f_{HOM}$$-$$f_{FM}$$), $$R/Q_{HOM}$$) and an equality constraint (abs($$f_{BM}$$-499.65 MHz) <= 0.05 MHz) are considered simultaneously. As a result, DNMOGA considerably improves both the number and competitiveness of the final feasible individuals, and shows the potential to completely replace the manual procession in this question. The nondominated fronts of different algorithms in the last generation are shown here.
![Profile Picture](https://github.com/peilin-wang-git/peilin-wang-git.github.io/raw/main/assets/img/paper1-2.jpg)
Then the individuals that have the similar frequency of the HOM are signaled and picked up from different algorithms. The indicators of these individuals are shown in the table below, in which the advantage of DNMOGA can be discovered. The $$R/Q_{FM}$$ is improved by about 24% and 14% compared with using the NBMOGA and NSGA-II, while the $$Ra_{FM}$$ is increased by approximately 55% and 22% respectively. Besides, only the $$R/Q_{HOM}$$ that comes from the individual of DNOMGA tends to zero, which is beneficial for further analysis of HOM. The geometric parameters of the individual from DNMOGA are shown in the last sub-figure above.

Algorithm             | $$R/Q_{FM}$$ [Ω]      | $$Ra_{FM}$$ [MΩ]      | $$f_{HOM}$$ [MHz]     | $$R/Q_{HOM}$$ [Ω]
:-------------------: | :-------------------: | :-------------------: | :-------------------: | :--------------------:
DNMOGA                | 324.72                | 12.15                 | 826.75                | 8.28E-7
NBMOGA                | 261.09                | 7.82                  | 806.46                | 9.46
NSGA-II               | 284.54                | 9.93                  | 800.56                | 18.58

In general, DNMOGA is instructive for dealing with the complex situations of strict constraints and preference in multi-objective optimization problems in physics.

<br/>
## Read the original

To read the original paper, please [press here](https://www.nature.com/articles/s41598-023-27478-7).


