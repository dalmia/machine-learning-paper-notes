# [RetinaNet: Focal Loss for Dense Object Detection](https://arxiv.org/pdf/1708.02002.pdf)

- The authors propose a novel loss they term the Focal Loss that adds a factor (1 − p) ^ γ to the standard cross entropy criterion. Setting γ > 0 reduces the relative loss for well-classified examples (p > .5), putting more focus on hard, misclassified examples. FL = (1 − p) ^ γ log (p)

- Current state-of-the-art object detectors are based on a two-stage, proposal-driven mechanism. As popularized
in the R-CNN framework [11], the first stage generates a sparse set of candidate object locations and the second stage
classifies each candidate location as one of the foreground classes or as background using a convolutional neural network.

- We present a one stage object detector that, for the first time, matches the state-of-the-art COCO AP of more complex two-stage detectors, such as the Feature Pyramid Network (FPN) [20] or Mask R-CNN [14] variants of Faster R-CNN [28]. To achieve this result, we identify class imbalance during training as the main obstacle impeding one-stage detector from
achieving state-of-the-art accuracy and propose a new loss function that eliminates this barrier.

- The loss function is a dynamically scaled cross entropy loss, where the scaling factor decays to zero as confidence in the correct class increases.

- We design a simple one-stage object detector called RetinaNet, named for its dense sampling of object locations in an input image.

- In contrast, the aim of this work is to understand if one-stage detectors can match or surpass the accuracy of two-stage detectors while running at similar or faster speeds.

