# Attention Modules on Resnet50

## Authors:

- Isabella Torres
- Nicolás Diaz
- Jose David Gómez
- David Quiñonez

## Introduction

The attention in CNN architectures could be defined as the capacity of a network on focusing on importan features and discard irrelevant ones, improving this topic on Neural Networks has shown increasing performance and results.

The attention can be added to an existing architecture by using modules such as Squeeze and Exitate and CBAM, which are precesily the ones we experiment on this project.

This project shows 3 different ResNet50 implementations to classify the CIFAR10 images and how the attention modules can affect it's performance.

## Project structure

- Resnet50 - Original

All the files required to run a jupyter notbook (google colab notebook) that train and test a simplified Resnet50's version without attention modules.

- Resnet50 - CBAM

All the files required to run a jupyter notbook (google colab notebook) that train and test a simplified Resnet50's version with a CBAM (Convolutional Block Attention Module).

- Resnet50 - SE

All the files required to run a jupyter notbook (google colab notebook) that train and test a simplified Resnet50's version with a SE (Squeeze and Excitation Module).

## The data

[CIFAR10](https://keras.io/api/datasets/cifar10/) dataset is a collection of 50.000 small images (32x32x3) labeled with 10 categories.

| Label | Description |
| ----- | ----------- |
| 0     | airplane    |
| 1     | automobile  |
| 2     | bird        |
| 3     | cat         |
| 4     | deer        |
| 5     | dog         |
| 6     | frog        |
| 7     | horse       |
| 9     | truck       |
| 8     | ship        |

## Analysis Process

1. Initially we decided to check the performance of the original network and how it detects features, this was posible using the Gradient-weighted Class Activation Map that shows us on a visual way were are the more important features that the network uses to classify an image.

2. Then we implemented the Squeeze and Excitation Module and inserted it between strategical layers on the architecture.

3. We also implemented the CBAM in the same way we did with SE.

4. We compared the performance metrics of each architecture variation and also, visually, how good was it attention.

## Comparison results

### Performance metrics

- Original
  | Loss | Accuracy | Val_Loss | Val_Accuracy |
  | ------ | -------- | -------- | ------------ |
  | 0.0213 | 0.9993 | 0.9498 | 0.8202 |

- SE
  | Loss | Accuracy | Val_Loss | Val_Accuracy |
  | ------ | -------- | -------- | ------------ |
  | 0.0162 | 1.0000 | 0.7298 | 0.8451 |

- CBAM
  | Loss | Accuracy | Val_Loss | Val_Accuracy |
  | ------ | -------- | -------- | ------------ |
  | 0.0161 | 1.0000 | 0.7674 | 0.8360 |

### Attention
