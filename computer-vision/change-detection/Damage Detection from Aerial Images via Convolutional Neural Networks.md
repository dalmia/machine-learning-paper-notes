# [Damage Detection from Aerial Images via Convolutional Neural Networks](https://ieeexplore.ieee.org/document/7986759/)

This paper introduced the ABCD dataset for Aerial images and demonstrated how CNNs can be used with images from different time periods to accurately classify whether an image was washed away or is still surviving.

- Introduced the ABCD dataset
- 3 inputs - pre-tsunami map, pre-tsunami aerial image and post-tsunami aerial image. Using the pre-tsunami map, each building is cropped out from both the pre and post-tsunami aerial images and these two cropped images were used as input to the CNN.
- The CNN architecture used is the Siamese NN with their weights being unshared owing to the fact that the pre- and post-tsunami images would be considerably different.
- Also, proposed the use of multi-stream CNN where the cropped images were used at multiple resolutions as the input to the Siamese Network.
- Instead of the Siamese network, both the 3-channel inputs can be concatenated to form a 6-channel input to a usual CNN for classification.
- Bayesian optimization for Hyperparameter tuning. Data augmentation was used to artificially increase the dataset.
