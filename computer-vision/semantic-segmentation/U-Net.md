# [U-Net: Convolutional Networks for Biomedical Image Segmentation](https://camo.githubusercontent.com/d3691bd39b74d10164610b8b9cb9376f70b40da4/687474703a2f2f6d6174746d6163792e696f2f766e65742e7079746f7263682f696d616765732f6469616772616d2e706e67)

![Unet](https://camo.githubusercontent.com/d01c3c1d4442e2d48e13e85172f0e5743a6ad096/68747470733a2f2f6c6d622e696e666f726d6174696b2e756e692d66726569627572672e64652f70656f706c652f726f6e6e656265722f752d6e65742f752d6e65742d6172636869746563747572652e706e67)

- Encoder-decoder architecture as proposed in Fully Convolutional Networks for Semantic Segmentation
- Each stage in the encoder part has 2 3x3 conv layers followed by a MaxPooling layer, which performs the downsampling operation.
- Number of filters double in each subsequent stage of the encoder part.
- In the decoder part, transpose convolution is used for upsampling and high-level features of the corresponding stage in the encoder part are concatenated at the beginning of each stage.
- The last layer uses 1x1 convolutions to give the final segmentation map.
- Extensive use of data augmentation, especially random elastic transformations.
