# [Unsupervised Change Detection in Satellite Images Using Principal Component Analysis and k -Means Clustering](https://ieeexplore.ieee.org/abstract/document/5196726/)

Given images at two different times, X1 and X2, the goal is to detect the change that has occured over the course of time. Most change detection algorithms work on the difference image *Xd*, which itself can be computed in various ways. The authors use the absolute difference between X1 and X2 to calculate Xd. The algorithm proposed is as follows:

- Divide the image into M non-overlapping blocks of size h x h and flatten it to get a vector for each block. Suppose each image is of size H x W, then M = ⌊H x W / h x h⌋.
- Get the mean of those vectors.
- Get the covariance matrix by subtracting the mean from each of the block vectors and perform the eigen decomposition to obtain the eigenspace consisting of S eigenvectors where S < h * h.
- For each pixel, take its h x h neighborhood and transform it to the eigenspace.
- Obtain the mean vectors in the eigenspace representing the clusters for the two classes - `changed` and `unchanged` - using k-means.
- Classify each pixel as `changed` or `unchanged` depending on whichever class's mean vector has the minimum distance from that pixel vector.
