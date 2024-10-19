---
layout: post
title: "Congratulations! My research project has been accepted in 2024AOCMP Oral Presentation on 12 October 2024"
author: "Peilin Wang"
categories: RP
tags: [RP,documentation]
image: paper5-1.jpg
---

# Dynamic Hyperparameter Integration for Medical Image Registration
<br/>

## Purpose
Deformable image registration algorithms utilize multiple loss functions to effectively guide their training processes. These loss functions serve dual roles: quantifying the smoothness of the deformation vector field and gauging image similarity. The interplay among these loss functions is intricate, heavily influencing outcomes based on their weights, which is exceedingly time-consuming. This study aims to develop a novel hyperparameter integration method that leverages the complex inter-relationship among loss functions, while eliminating the need for fine-tuning their weights at the same time.

## Methods
Drawing inspiration from multi-modality task methodologies, the Dynamic Hyperparameter Integration Registration Algorithm (DyHIMorph) is proposed, which incorporates weights hyperparameters directly into its framework as single modality to provide relationship between weights hyperparameters and deformable vector field (DVF). This innovation enables catching inter-relationships among different loss functions, and dynamic responsiveness to varying hyperparameter configurations, enhancing model robustness and adaptability.

## Results
Preliminary experiments using the open-source OASIS two-dimensional (2D) dataset demonstrate promising outcomes. Integration of DyHIMorph with SynthMorph achieves superior performance, with a Dice score of 0.825 and an SSIM score of 0.915, compared to 0.794 and 0.899 respectively for SynthMorph. DyHIMorph also exhibits enhanced stability and showcases better performance across varying hyperparameter configurations comparing with the SynthMorph with hypernetwork structure, particularly in the range of 0.2 to 0.95 for loss function weights (ranging from 0 to 1).

## Conclusion
These preliminary results highlight the strong performance of DyHIMorph, effectively utilizing the inter-relationships among loss functions and achieving better performance without the need for extensive fine-tuning. This work significantly reduces the time required for hyperparameter optimization. Future work will involve testing DyHIMorph on 3D datasets, which is expected to further decrease the fine-tuning time compared with traditional deep-learning registration algorithms. Additionally, DyHIMorph has the potential to address a broader spectrum of multi-task learning challenges beyond medical image

## AOCMP Introduction
Asia-Oceania Congress on Medical Physics (AOCMP) is Organized annually in various countries in the Asia-Oceania Federation of Organizations for Medical Physics (AFOMP) region to give a scientific platform to share, upgrade, and enhance medical physics knowledge worldwide.

Asia-Oceania Congress on Medical Physics (AOCMP) series were held respectively in Malaysia (Kuala Lumpur 2004 and 2018, Penang 2024), Thailand(Bangkok 2001 and 2016, Chiang Mai 2009 and 2012, Phuket 2020), South Korea(Gyeongju 2002, Seoul 2006), Australia (Sydney 2003, Perth 2019), Japan(Kyoto 2005, Fukuoka 2011), China (Huangshan 2007, Xi’an 2015), Vietnam (Ho Chi Minh City 2008 and 2014), China (Taipei 2010 and 2022), Singapore (Singapore 2013), India (Jaipur 2017)and Bangladesh (Cox’s Bazar 2021).

