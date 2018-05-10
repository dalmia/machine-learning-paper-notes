# Learning deep structured network for weakly supervised change detection

The motivation of this paper is to reduce the drastic amount of effort required to annotate images for dense pixel-level annotations. They propose a method to use just the image-level annotation to classify as well as localize changed regions.

- Their algorithm jointly learns the image-level labels as well as the localization of the change using a 2-stream deep network with a Directed Acyclic Graph (DAG) architecture with the initial layers being shared while the final output being split to produce the two different outputs (prediction label and localized changes).
- They introduce a constrained mean-field algorithm that employs a factorizable approximate posterior distribution to impose a global constraint on the changed pixels to suppress the bias towards the background pixels.
- Use a variational EM algorithm to maximize the lower bound of the log likelihood of image-level labels.
- The joint prediction is the MAP estimate of the joint posterior model which is composed of three terms - one being the unary term for image-level y modeled by a CNN, the second being the unary term for pixel-level labels and the third term representing the pairwise energy which enforces the spatial smoothness of pixel-wise labels and capturing the coupling between image-level and pixel-level labels.
