 Project Title: **Reproduction and Enhancement of [Xu, Chang, et al. "Dynamic coarse-to-fine learning for oriented tiny object detection" CVPR, 2023.]**

## Overview

This repository contains the code and results for reproducing the paper **"Dynamic coarse-to-fine learning for oriented tiny object detection"** and implementing a novel approach for improving the model's performance. The original paper tackles the challenging task of detecting arbitrarily oriented tiny objects, which poses significant difficulties for existing detectors, particularly in label assignment. Despite advancements in adaptive label assignment, extreme geometries and limited features of tiny objects often result in severe mismatch and imbalance issues.

To address these challenges, the paper proposes a dynamic prior along with a coarse-to-fine assigner, termed DCFL. The approach models prior, label assignment, and object representation dynamically, aiming to alleviate mismatch issues and provide appropriate, balanced supervision for diverse instances. The novelty introduced here involves the integration of **Pruning, Quantization, and Huffman Encoding** to reduce the model size while analyzing its effect on accuracy.

## Table of Contents

- [Introduction](#introduction)
- [Results](#results)
  - [Reproduced Results](#reproduced-results)
  - [Novelty and Results](#novelty-and-results)
- [Methodology](#methodology)
  - [Pruning](#pruning)
  - [Quantization](#quantization)
  - [Huffman Encoding](#huffman-encoding)
- [Setup and Installation](#setup-and-installation)
- [Conclusion](#conclusion)
- [References](#references)

## Introduction

The purpose of this project was to reproduce the results presented in the paper **"Dynamic coarse-to-fine learning for oriented tiny object detection"** and explore the effects of network optimization techniques like pruning, quantization, and Huffman encoding on the model’s performance and size.

## Results

### Reproduced Results

Below are the results obtained from the reproduction of the original paper's experiment on the DOTA V1 dataset:

![Reproduced Results](https://github.com/Nikhil-Kumar-Patel/Tiny_Oriented_Object_Detection/blob/main/figures/DOTA-V1.jpg)

- **mAP**: 0.681
- **Recall**: 0.872
- **Precision**: 0.057

### Novelty and Results

After applying pruning, quantization, and Huffman encoding, the results are as follows:

![Novelty Results](https://github.com/Nikhil-Kumar-Patel/Tiny_Oriented_Object_Detection/blob/main/figures/Pruning.jpg)

- **mAP**: 0.550
- **Recall**: 0.750
- **Precision**: 0.033

The application of these techniques significantly reduced the model size, as shown in the diagram below, albeit with some reduction in precision and mAP.

![Novelty Process](https://github.com/Nikhil-Kumar-Patel/Tiny_Oriented_Object_Detection/blob/main/figures/Novelty.jpg)

## Methodology

### Pruning

Pruning involves removing less significant weights from the network, thereby reducing the network's complexity and size. This step aims to maintain accuracy while compressing the model.

### Quantization

Quantization reduces the number of bits required to represent each weight, which leads to a smaller model with reduced computational requirements.

### Huffman Encoding

Huffman encoding is used for lossless compression of the quantized weights, further minimizing the storage size of the model without affecting its accuracy.

## Setup and Installation

To reproduce the results and apply the novelty, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/Nikhil-Kumar-Patel/Tiny_Oriented_Object_Detection.git
   ```
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```


## Conclusion

This project successfully reproduces the original results and demonstrates the impact of model optimization techniques such as pruning, quantization, and Huffman encoding. While these methods effectively reduce the model size, they also lead to a trade-off in precision and mAP.

## References

1. **Dynamic coarse-to-fine learning for oriented tiny object detection** - [link to the paper](https://arxiv.org/pdf/2304.08876)
