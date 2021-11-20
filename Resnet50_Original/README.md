# Resnet50 Architecture

The ResNet architecture is based on residual connections throughout the layers, this type of connections helps with the problem of vanishing gradient that does not allow the training of the lower layers of the model.

## Results

- Model Accuracy

  <img src="https://github.com/Dalejan/Resnet50_Attention/blob/master/Resnet50_Original/acc.png">

- Model Loss

  <img src="https://github.com/Dalejan/Resnet50_Attention/blob/master/Resnet50_Original/loss.png">

## Conclusions

As we can see, the performance of the network is not quite good.

| Loss   | Accuracy | Val_Loss | Val_Accuracy |
| ------ | -------- | -------- | ------------ |
| 0.0213 | 0.9993   | 0.9498   | 0.8202       |

And the attention seems to be unfocused.

<img src="https://github.com/Dalejan/Resnet50_Attention/blob/master/Resnet50_Original/ori.jpg">

So let's test the same architecture with attention modules (Resnet50_CBAM and Resnet50_SE).
