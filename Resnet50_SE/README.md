# Squeeze and Excitation

The [Squeeze and Excitation](https://arxiv.org/abs/1709.01507) Attention Module aims to highligth the channel features by using average pooling on them.
This module can be inserted between convolutional layers since it goes from a feature map and solves the highlighed features on it.

<img src="https://miro.medium.com/max/1120/1*bmObF5Tibc58iE9iOu327w.png">

## Results

- Model Accuracy

  <img src="https://github.com/Dalejan/Resnet50_Attention/blob/master/Resnet50_SE/acc.png">

- Model Loss

  <img src="https://github.com/Dalejan/Resnet50_Attention/blob/master/Resnet50_SE/loss.png">

As we can see, the performance of the network is not quite good, but it's slightly better than the original one.

| Loss   | Accuracy | Val_Loss | Val_Accuracy |
| ------ | -------- | -------- | ------------ |
| 0.0162 | 1.0000   | 0.7298   | 0.8451       |
