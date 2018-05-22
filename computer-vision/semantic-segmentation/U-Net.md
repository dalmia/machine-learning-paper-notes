# U-Net: Convolutional Networks for Biomedical Image Segmentation

- Encoder-decoder architecture as proposed in Fully Convolutional Networks for Semantic Segmentation
- Each stage in the encoder part has 2 3x3 conv layers followed by a MaxPooling layer, which performs the downsampling operation.
- Number of filters double in each subsequent stage of the encoder part.
- In the decoder part, transpose convolution is used for upsampling and high-level features of the corresponding stage in the encoder part are concatenated at the beginning of each stage.
- The last layer uses 1x1 convolutions to give the final segmentation map.
- Extensive use of data augmentation, especially random elastic transformations.
