# [Change Detection in Satellite Images Using a Genetic Algorithm Approach](https://ieeexplore.ieee.org/document/5395684/)

The paper highlights the problems used by previous methods used for change detection which rely on parameter estimation techniques to get the apriori values and hence, don't perform well on different types of satellite images. It uses a genetic algorithm to predict the change detection mask by starting with an initial realization of the binary mask and evolving it through generations. The algorithm is mentioned below:

- Generate initial population of K individuals randomly with generation index (iteration number) = 1. The individuals represent different selections among all 2 ^ {I * J} label configurations possible for an I x J image. So, K such configurations are randomly selected. 
- Evaluate the cost (or fitness) value of each individual which is weighted sum of the euclidean distances of each pixel from the mean vector of the class assigned to it for that particular configuration.
- Randomly select two individuals (parents) and use them to generate offsprings.
- Evaluate the cost function of all offsprings.
- Select the most adaptive individual problems using tournament selection and return that individual to the population.
- Generation index is incremented by one and the same process is carried out until the best individual is obtained.


