 Project Title: **Reproduction and Enhancement of [Xu, Chang, et al. "Dynamic coarse-to-fine learning for oriented tiny object detection" CVPR, 2023.]**

## Overview

This repository contains the code and results for reproducing the paper **"[Xu, Chang, et al. "Dynamic coarse-to-fine learning for oriented tiny object detection" CVPR, 2023.]"** and implementing a novel approach for improving the model's performance. The paper was focused on [briefly describe the original paper's objective]. The novelty introduced here involves the integration of **Pruning, Quantization, and Huffman Encoding** to reduce the model size while analyzing its effect on accuracy.

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
- [Usage](#usage)
- [Conclusion](#conclusion)
- [References](#references)

## Introduction

The purpose of this project was to reproduce the results presented in the paper **"[Original Paper Title]"** and explore the effects of network optimization techniques like pruning, quantization, and Huffman encoding on the model’s performance and size.

## Results

### Reproduced Results

Below are the results obtained from the reproduction of the original paper's experiment on the DOTA V1 dataset:

![Reproduced Results](path_to_the_image)

- **mAP**: 0.681
- **Recall**: 0.872
- **Precision**: 0.057

### Novelty and Results

After applying pruning, quantization, and Huffman encoding, the results are as follows:

![Novelty Results](path_to_the_image)

- **mAP**: 0.550
- **Recall**: 0.750
- **Precision**: 0.033

The application of these techniques significantly reduced the model size, as shown in the diagram below, albeit with some reduction in precision and mAP.

![Novelty Process](path_to_the_image)

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
   git clone [[repository_url]](https://github.com/Nikhil-Kumar-Patel/Tiny_Oriented_Object_Detection.git)
   ```
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Download the dataset and place it in the designated folder:
   ```bash
   wget [dataset_url]
   ```
4. Run the training or inference scripts:
   ```bash
   python train.py --config config.yaml
   ```

## Usage

To test the novelty:

```bash
python prune_quantize_encode.py --config config.yaml
```

## Conclusion

This project successfully reproduces the original results and demonstrates the impact of model optimization techniques such as pruning, quantization, and Huffman encoding. While these methods effectively reduce the model size, they also lead to a trade-off in precision and mAP.

## References

1. **[Dynamic coarse-to-fine learning for oriented tiny object detection]** - [[link to the paper](https://arxiv.org/pdf/2304.08876)]
2. **Other References** - [https://github.com/ChaselTsui/mmrotate-dcfl]
