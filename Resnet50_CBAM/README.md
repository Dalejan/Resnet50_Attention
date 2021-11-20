# CBAM - Convolutional Block Attention Module

## Results

- Model Accuracy

  <img src="https://github.com/Dalejan/Resnet50_Attention/blob/master/Resnet50_CBAM/acc.png">

- Model Loss

  <img src="https://github.com/Dalejan/Resnet50_Attention/blob/master/Resnet50_CBAM/loss.png">

## Conclusions

As we can see, the performance still getting just a little bit better compared to the original and the one with SE.

| Loss   | Accuracy | Val_Loss | Val_Accuracy |
| ------ | -------- | -------- | ------------ |
| 0.0161 | 1.0000   | 0.7674   | 0.8360       |

We can infer that this one has a better attention on the bird class because it tottally focus on the head of the animal.

<img src="https://github.com/Dalejan/Resnet50_Attention/blob/master/Resnet50_CBAM/cbam.png">
