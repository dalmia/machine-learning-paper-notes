# From Image-Level to Pixel-level Labeling with Convolutional Neural Networks

- Goal: Generate pixel-level labels using Image-level labels by using a CNN and applying more weights to pixels that are important for classifying the image by seeing at as an instance of Multi-Instance Learning (MIL) and noting that each image is known to have (or not) atleast one pixel belonging to the class of the object.

- Overfeat is used as the feature extractor which forms the first few layers of the CNN, followed by a few more convolutional layers forming their segmentation network. Training achieved by maximizing the classfication likelihood by adding an Aggregation Layer on top of the segmentation network outputs which puts more weight on the pixels important for classification. This Aggregation layer is removed at test time.

- Segmentation done on *C* classes. Hence, the classification task should have atleast *C* classes where the rest of the classes form the background class. Input- 400x400x3 - Overfeat (frozen) - 29x29x1024 - Segmentation network (first three layerss have ReLU, no activation on the last layer) - 21x21x(C+1).

- Aggregation layer used as we only have image-level labels, which gives us class scores which can be then used for training by maximizing the log-likelihood using gradient descent. This aggregation function (`aggreg`) should be such that the scores of those pixels which are important to classificaition is maximized. Thus, max-pooling might be a good choice, but it would  just update one pixel at a time -> slow. Thus, use a convex approximation of max -> Log Sum Exp (LSE) with parameter *r* controlling the smoothness (high r-> same as averaging, low r -> same as max).

- At inference time, `aggreg` is removed and softmax is applied to get pixel-wise class scores. Efficiently retrieve labels for all pixels by shifting the input image and passing it through the network.

- Reduce false positives by including image-level priors (ILP) and Segmentation Priors (SP). The LSE score of each channel is used as ILP to encourage likely categories and discourage unlikely ones. Final output of ILP is the pixel-wise class score times the ILP.

- Use three types of segmentation priors to further refine the image: `SP-sppxl` using superpixels, `SP-bb` making use of bounding box candidates using a per-class confidence threshold calculated by grid search and `SP-seg` which is a smoothing prior trained with class-independent segmentation labels.  
