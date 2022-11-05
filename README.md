# Neural-Architecture-Search-using-Genetic-Algorithm

Task is to create a search algorithm to search in a Neural Architecture
Search (NAS) space for the best performing Convolutional Neural Network
(CNN) architecture on the fashion-mnist data-set. Best performing is de-
fined as having a test accuracy above 75% and the lowest parameter count
model your algorithm can find
CNN Architecture Constraints

## Process:

For this project we have used genetic algorithm. Following are the steps that have been used to solve the problem statement

1. Since we are supposed to optimise the parameters of the given CNN network, a general CNN network is made considering the constraints mentioned.
2. First the parameters are initialized with a range of available choices.
3. The Roulette fitness function is written by taking the weight(importance) of each species and selecting two parents with max fitness value.
4. Crossover has been done in different way. Instead of flipping parameter value one child with one parent, we are randomly deciding which the parent to be flipped.
5. Mutation/flipping has been achieved by changing the gene of children by changing the epoch(adding some integer to existing epoch number). This differentiates the two consecutive children.

## Best Architecture:

The best architecture returned by our searching algorithm is:

1. In normal layers(NC) filter size = 16, kernel size = 6, activation = relu
2. In 2 reduction layers(RC) filter size = 64, kernel size = 3, activation = tanh
3. In dense layers activation = sigmoid

Final genome string we got: NC 16 6 relu;RC 64 3 tanh;RC 64 3 tanh;FL sigmoid

Total number of parameters: 51610 Test set accuracy: 81.84%



For detail problem statement refer to problem statement pdf.

For the implementation refer the report.
