---
layout: post
title: "Congratulations! My research project has been accepted in 2025ISMRM Digital Poster Discussion on 17 May 2025"
author: "Peilin Wang"
categories: RI
tags: [RI,documentation]
image: paper7-1.jpg
---

# RAUQ-4DRecon：A Robust Anatomy-based Ultra-Quality 4D MR reconstruction workflow
<br/>

## Purpose
Current deep-learning and prior-image-based reconstruction methods lack generalizability, limiting the scalability and clinical adoption of four-dimensional MRI (4D-MRI).

## Goal 
To develop a generalizable deep-learning-based 4D-MRI reconstruction workflow.

## Approach
We propose RAUQ-4DRecon, a workflow trained on XCAT-generated data with diverse contrasts and physiological parameters. Key innovations in the deep-learning workflow include a segmentation-guided vertebra affine alignment network and a deformable motion estimation hypernetwork to capture and transfer respiratory motion of commercial low-quality time-resolved 4D-MRI to high-quality 3D-MRI.

## Results
RAUQ-4DRecon outperformed VoxelMorph and pTV across all metrics concerned in XCAT validation. Comparing with DDEM workflow in external-validation real-patient data, RAUQ-4DRecon increased NMI metric from 0.328±0.085 to 0.382±0.071, LCC for vertebra stability also increased from 0.275±0.082 to 0.347±0.061.
