---
layout: post
title: "Paper Reading: Medical Large Model (1)"
author: "Peilin Wang"
categories: RI
tags: [RI,documentation]
image: paper-reading-1-1.jpg
---

# [UniverSeg: Universal Medical Image Segmentation](https://universeg.csail.mit.edu/)

## Introduction

This study introduces a novel large medical image segmentation model named UniverSeg, designed to effectively segment images encompassing diverse anatomies, image modalities, or labels that extend beyond the boundaries of the training dataset. UniverSeg is rooted in the principles of meta learning / few-shot learning, thereby shifting the paradigm of training deep-learning models from merely 'learning to reflect' to the more sophisticated concept of 'learning to learn'. Concurrently, the architecture of UniverSeg draws inspiration from the UNet model, leveraging its structural attributes to enhance segmentation capabilities. By combining the advancements of meta learning / few-shot learning with the foundational framework of UNet, UniverSeg represents a pioneering approach in addressing the challenges of versatile medical image segmentation tasks.

This study possibly stands as a pioneering effort in utilizing a large model for medical image segmentation. The amalgamation of few-shot learning and the established UNet architecture adds substantial value to this research. This synergy not only expands the horizons of medical image segmentation but also brings forth a new approach that holds significant implications. The integration of these two distinct methodologies contributes to the meaningfulness of this work, showcasing innovative thinking in the domain of medical image analysis.

**KEY WORDS: Meta learning / few-shot learning, UNet model, large model.**

## What is [meta learning / few-shot learning](https://www.youtube.com/watch?v=UkQ2FVpDxHg&list=PLvOO0btloRnuGl5OJM37a8c6auebn-rH2&index=1&t=3s)?
Comparing with the general training tasks, few-shot learning has some obvious characteratics. 

Firstly, few-shot learning shifts the destination of training deep-learning models from merely 'learning to reflect' to the more sophisticated concept of 'learning to learn'. These words sound abstracted, and I'd like to further explain it. 

Specifically, let's say there are many animals with different labels, few-shot learning cannot recognize the animals in new images without reference nor take them into the existing calsses, but is able to understand the relationship between the new images and some reference images. Thus, the training process of few-shot learning naturally need a supporting set and quray set. Supporting set has many reference images with different labels, and quray set usually has only one image with pending class. These two sets can be seen as the subsets in training set, validation set and test set, and the images in these three sets can be violated into supporting set and quray set randomly in every epoch.  Few-shot learning compares the features of images between quray set and supporting set, and predict the class of quray set as one of the labels in supporting set, as shown below.
![Profile Picture](https://github.com/peilin-wang-git/peilin-wang-git.github.io/raw/main/assets/img/paper-reading-1-2.jpg)

In the training process, few-shot learning try to learn the relationship between different images, but not the relationship between images and existing labels, which means the labels in validation set or test set are different from the labels in training set. This is why few-shot learning can learn to learn. Besides, according to the number of images with same label in quary set, few-shot learning can be further violates as one-shot learning, two-shot learning, as so on. According to the number of labels in each quary set, few-shot learning can be further violates as one-k learning, two-k learning, as so on.
![Profile Picture](https://github.com/peilin-wang-git/peilin-wang-git.github.io/raw/main/assets/img/paper-reading-1-3.jpg)

In addition, the paradigm of few-shot learning couses that a small size of training set is supposed to be trained in few-shot learning. Take the common dataset [Omniglot](https://github.com/brendenlake/omniglot) as an example, there are 1623 labels, but each label only has 20 images, which is extremely difficult for general model to have a satisfied performance.

Finally, the training operation and related code can be obtained from [here](https://zhuanlan.zhihu.com/p/156830039).

## What is [UNet](https://link.springer.com/chapter/10.1007/978-3-319-24574-4_28)?
UNet is a grown  encoder-decoder structure with residual connections, which has good performance for medical images processing. Many blogs as well as websites have talk about it for many times.

## The main thought of UniverSeg
In contrast to typical tasks in few-shot learning that predominantly focus on classification, UniverSeg is designed to address a considerably more intricate challenge: segmenting images containing diverse anatomical structures. 

In order to transfer information between queary set and supporting set, CrossBlock is proposed. In Fig. 1(b), how this block works is shown, as well as the equations in the original paper are corelated to the submodels in block. Besides, predictions from an ensemble of K independently sampled support sets are combined in this paper to reduce the dependence to the choice of the supporting set. Moreover,some people have tried to further describe this model in the retrospectives of augmentation, training, as well as designment, I think they have done very [well](https://blog.csdn.net/qq_40943760/article/details/130493000). Note that all the compirations in this paper are among the UniverSeg and several other few-shot learning models, and UniverSeg has not performed better than the individual fully-trained networks (such as nnUNet) yet.

The main loop of UniverSeg has been shown below. 
![Profile Picture](https://github.com/peilin-wang-git/peilin-wang-git.github.io/raw/main/assets/img/paper-reading-1-4.jpg)
All the methods of augmentation have been shown below.
![Profile Picture](https://github.com/peilin-wang-git/peilin-wang-git.github.io/raw/main/assets/img/paper-reading-1-5.jpg)
The datasets collected and used in this paper has been shown below.
![Profile Picture](https://github.com/peilin-wang-git/peilin-wang-git.github.io/raw/main/assets/img/paper-reading-1-6.jpg)

## Original
To read the original paper, please [press here](https://universeg.csail.mit.edu/).


