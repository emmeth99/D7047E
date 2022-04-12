# Exercise 2

Test Accuracy of the different models


| Model      | Test Accuracy |
| ----------- | ----------- |
| AlexNet + Fine Tuning                                   |  35.5%     |
| AlexNet + Feature Extraction                            |  71.5%     |
| MNIST-trained ResNet on MNIST data                      |  98.2%     |
| MNIST-trained ResNet on SVHN data                       |  14.8%     |
| MNIST-trained ResNet on SVHN data + Feature Extraction  |  26.6%     |


The difference between the two AlexNet runs is that in the fine tuning run, we allow all parameters of the network to be changed during training. While in the feature extraction run we only allow the parameters of the last layer to be changed. The feature extraction apporoach makes use of the pretrained networks initial weights and makes training much faster. The fine tuning run also makes use of the pretrained networks initial weights, but makes changes to all of them to better fit the data.

In our runs the feature extraction model was much faster and had much better accuracy than the fine tuning model. The difference in speed comes from the fact that feature extraction has much less paramaters to train, and we think that the increased accuracy comes from not touching the already good weights in the earlier layers, wheras we suspect that the fine tuning models lower accuracy comes from uneccesarily changing weights in the earlier layers.
