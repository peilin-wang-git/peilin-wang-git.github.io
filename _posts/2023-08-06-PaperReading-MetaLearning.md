---
layout: post
title: "Paper Reading: UniverSeg Universal Medical Image Segmentation"
author: "Peilin Wang"
categories: RI
tags: [RI,documentation]
image: paper-reading-1-1.jpg
---

# [UniverSeg: Universal Medical Image Segmentation](https://universeg.csail.mit.edu/)

## Introduction

This study introduces a novel medical image segmentation model named UniverSeg, designed to effectively segment images encompassing diverse anatomies, image modalities, or labels that extend beyond the boundaries of the training dataset. UniverSeg is rooted in the principles of meta learning / few-shot learning, thereby shifting the paradigm of training deep-learning models from merely 'learning to reflect' to the more sophisticated concept of 'learning to learn'. Concurrently, the architecture of UniverSeg draws inspiration from the UNet model, leveraging its structural attributes to enhance segmentation capabilities. By combining the advancements of meta and few-shot learning with the foundational framework of UNet, UniverSeg represents a pioneering approach in addressing the challenges of versatile medical image segmentation tasks.

`KEY WORDS: Meta learning / few-shot learning, UNet model.`

## What is [meta learning / few-shot learning](https://www.youtube.com/watch?v=UkQ2FVpDxHg&list=PLvOO0btloRnuGl5OJM37a8c6auebn-rH2&index=1&t=3s)?
Comparing with the general training tasks, few-shot learning has two obvious characteratics. 

Firstly, few-shot learning shifts the destination of training deep-learning models from merely 'learning to reflect' to the more sophisticated concept of 'learning to learn'. These words sound abstracted, and need to be further explained. 

Specifically, let's say there are many animals with different labels, few-shot learning cannot recognize the animals in new images nor take them into the existing calsses, but is able to understand the relationship between the new images and some images with different labels. Thus, the training process of few-shot learning naturally need a supporting set and quray set. These two sets can be seen as the subsets in training set, validation set and test set, and the images can be violated into supporting set and quray set randomly in different epoch. Supporting set has many images with different label, and quray set usually has only one image with pending class. Few-shot learning compares the features of images between quray set and supporting set, and predict the class of quray set as one of the labels in supporting set, as shown below.
![Profile Picture](https://github.com/peilin-wang-git/peilin-wang-git.github.io/raw/main/assets/img/paper-reading-1-2.jpg)

In the training process, few-shot learning try to learn the relation between different images, which means the labels in validation set or test set are different from the labels in training set. This is why few-shot learning learns to learn. Besides, according to the number of images with same label in quary set, few-shot learning can be further violates as one-shot learning, two-shot learning, as so on. According to the number of labels in each quary set, few-shot learning can be further violates as one-k learning, two-k learning, as so on.
![Profile Picture](https://github.com/peilin-wang-git/peilin-wang-git.github.io/raw/main/assets/img/paper-reading-1-3.jpg)

Secondly, the task of few-shot learning decides taht a little size of training set is supposed to be trained in few-shot learning.

## What is UNet?

## The main thought of UniverSeg

## Original

To read the original paper, please [press here](https://universeg.csail.mit.edu/).


