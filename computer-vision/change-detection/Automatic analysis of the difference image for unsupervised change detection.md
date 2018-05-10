# [Automatic analysis of the difference image for unsupervised change detection](https://ieeexplore.ieee.org/document/843009/)

This paper frames the change detection problem in the form of Bayes' Decision Theory. The authors propose two different learning algorithms, one supervised and the other unsupervised while using Expectation-Maximization (EM) for parameter estimation. The main points are mentioned below:

- The first algorithm assumes the pixel values to be independent. Upon obtaining the difference image using *Change Vector Analysis (CVA)*, the final change detection map is obtained by thresholding the difference image. The threshold is decided using Bayes' Theory. This is an unsupervised method.

- To calculate the posterior values, the apriori probabilities and the likelihood values for each class has to be known. These values are estimated using EM algorithm iteratively, by assuming the likelihood to be a Gaussian.

- The second method makes use of spatial contextual information to improve the final inference using an approach based on Markov Random Fields (MRFs). This requires supervised learning. 

- Given a I x J sized image, there are 2 ^ {I * J} possible labeling configurations for the image and it is not feasible to check each of them to find the one with the minimum cost. So, the conditional distribution of each pixel label is modeled as a MRF using an 8-neighbourhood, with the conditional density being measured using the Gibbs Energy function. The end goal is to reduce an overall energy function based on the sum of the Gibbs energy function and a function representing the statistics of the gray levels under the assumption of conditional independence.

- A big idea to takeaway from this paper is the use of spatial context to make the final prediction.
