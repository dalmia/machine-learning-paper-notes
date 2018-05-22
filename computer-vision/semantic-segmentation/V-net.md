# [V-Net: Fully Convolutional Neural Networks for Volumetric Medical Image Segmentation](V-Net: Fully Convolutional Neural Networks for Volumetric Medical Image Segmentation)

![Vnet](https://camo.githubusercontent.com/d3691bd39b74d10164610b8b9cb9376f70b40da4/687474703a2f2f6d6174746d6163792e696f2f766e65742e7079746f7263682f696d616765732f6469616772616d2e706e67)

- Similar architecture to U-Net, but with [residual connections](https://arxiv.org/abs/1512.03385) between the input and output of each stage.
- Downsampling performed by strided convolution instead of MaxPooling.
- Varying number of convolutional layers in each stage.
- PReLU used as the activation.
