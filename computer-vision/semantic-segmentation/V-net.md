# [V-Net: Fully Convolutional Neural Networks for Volumetric Medical Image Segmentation](V-Net: Fully Convolutional Neural Networks for Volumetric Medical Image Segmentation
)

![Vnet](https://camo.githubusercontent.com/d01c3c1d4442e2d48e13e85172f0e5743a6ad096/68747470733a2f2f6c6d622e696e666f726d6174696b2e756e692d66726569627572672e64652f70656f706c652f726f6e6e656265722f752d6e65742f752d6e65742d6172636869746563747572652e706e67)

- Similar architecture to U-Net, but with [residual connections](https://arxiv.org/abs/1512.03385) between the input and output of each stage.
- Downsampling performed by strided convolution instead of MaxPooling.
- Varying number of convolutional layers in each stage.
- PReLU used as the activation.
