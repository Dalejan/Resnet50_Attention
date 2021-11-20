# Attention Modules on Resnet50

## Authors:

- Isabella Torres
- Nicolás Diaz
- Jose David Gómez
- David Quiñonez

## Introduction

The attention in CNN architectures could be defined as the capacity of a network on focusing on important features and discard irrelevant ones, improving this topic on Neural Networks has shown increased performance and results.

The attention can be added to an existing architecture by using modules such as Squeeze and Excitation and CBAM, which are precisely the ones we experimented on this project.

This project shows 3 different ResNet50 implementations to classify the CIFAR10 dataset and how the attention modules can improve it's performance.

## Project structure

- Resnet50 - Original

All the files required to run a jupyter notebook (google colab notebook) that train and test a simplified Resnet50's version without attention modules.

- Resnet50 - CBAM

All the files required to run a jupyter notebook (google colab notebook) that train and test a simplified Resnet50's version with a CBAM (Convolutional Block Attention Module).

- Resnet50 - SE

All the files required to run a jupyter notebook (google colab notebook) that train and test a simplified Resnet50's version with a SE (Squeeze and Excitation Module).

- Grad-CAM

Images generated using Grad-CAM on each model already trained.

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

1. Initially we wanted to review the performance of the original network when detecting features, this was possible using the Gradient-weighted Class Activation Map that shows us, in a visual way, where are the most important features that the network uses to classify an image in a certain class.

2. Then we implemented the Squeeze and Excitation Module and inserted it between strategical layers on the architecture.

3. We also implemented the CBAM in the same way we did with SE.

4. We compared the performance metrics of each architecture variation and also, visually, how good was its attention.

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

- CBAM: Convolutional Block Attention Module - Sanghyun Woo et. al

The results of the authors shows an increase attention with the CBAM module, showing that the model learned the concept of objectness. The heatmap covers not only the object of the class but also the most relevant faeature of this class, whereas the oringal ResNet-50 focuses its attention in apparently irrelevant features.


  <img src="https://github.com/Dalejan/Resnet50_Attention/blob/master/authors_gradcam.jpg">

As we can see, the attention gets better as we intentionally change the attention modules, with better results using CBAM.
The heatmaps have a better location with the CBAM approach

- Original Attention

  <img src="https://github.com/Dalejan/Resnet50_Attention/blob/master/Resnet50_Original/ori.jpg">

- SE Attention

  <img src="https://github.com/Dalejan/Resnet50_Attention/blob/master/Resnet50_SE/se.jpg">

- CBAM Attention

  <img src="https://github.com/Dalejan/Resnet50_Attention/blob/master/Resnet50_CBAM/cbam.jpg">


