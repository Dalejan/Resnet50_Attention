# Resnet50 Architecture

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

And the attention seems to be on ilogical locations.

---

So let's test the same architecture with attention modules (Resnet50_CBAM and Resnet50_SE).
