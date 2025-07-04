---
layout: post
title: "Congratulations! My research project has been accepted in 2025ESTRO Digital Poster Discussion on 2 May 2025"
author: "Peilin Wang"
categories: RI
tags: [RI,documentation]
image: paper6-1.jpg
---

# A Digital paperAnatomy-Based Vertebra-Guided Affine Registration Network (VerGAReg)
<br/>

## Purpose
To develop an automatic affine registration method tailored for abdominal MRI-guided radiation therapy, addressing the limitations of manual registration and the underperformance of existing deep-learning algorithms caused by deformable respiratory motion.

## International Collaborative Research Fellowship (ICRF) 
We propose VerGAReg, a vertebra-guided affine registration network with two main modules: a deep learning-based key point extraction module and a parameter fitting module. The key point extraction uses dual-channel architecture with a cross-stitch mechanism for weight sharing. The first channel performs vertebral segmentation, with each block feeding into the corresponding block of the second channel to aggregate and analyze semantic information, ultimately extracting key points from the entire image. The parameter fitting module utilizes the least squares method to compute affine transformation parameters.

For training data, we use the XCAT digital phantom to generate accurate, comprehensive anatomical labels with respiratory motion and augment these labels to various contrasts and qualities. Additionally, we employ Focal Loss to guide vertebra segmentation and Dice Loss for anatomical alignment in the affine registration procedure.

## Results
VerGAReg was trained over 5000 iterations using 106 augmented images. A two-stage evaluation process was conducted. In the first stage, 300 T1-weighted 4D-MRI images were generated and converted to T2- and PD-weighted images to simulate consistent anatomy and respiratory features across modalities. These modalities were paired, and alignment errors were measured across three respiratory motion ranges, evaluating performance using the statistical metric normalized mutual information (NMI) and several vertebral stability metrics. VerGAReg consistently outperformed the total-body alignment (TBA) method, the vertebra affine alignment (VAA) method without segmentation guidance, and the iterative method ANTs in nearly all the metrics concerned.
In the second stage, VerGAReg was evaluated on real patient 3D-4D MRI pairs from 32 patients at Beijing Cancer Hospital. VerGAReg achieved a vertebral stability local cross-correlation (LCC) of 0.363 ± 0.106, surpassing TBA (0.274 ± 0.060) and VAA (0.271 ± 0.051). For the NMI metric, VerGAReg achieved 0.258 ± 0.061, compared to 0.217 ± 0.046 for TBA and 0.212 ± 0.045 for VAA. A specific case is shown in Fig. 2(g), in which VerGAReg performs best in position and direction of affine parameters.

## Conclusion
We developed VerGAReg, a digital anatomy-based vertebra-guided affine registration network that demonstrates superior performance in abdominal imaging. VerGAReg can serve as an effective preliminary step for automatic affine registration in abdominal applications.
