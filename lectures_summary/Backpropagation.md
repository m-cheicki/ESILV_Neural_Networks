# Training Feed-Forward Neural Networks (backpropagation)

How can we figure out what the parameter vector (= weights for all the conections in our neural network) should be ? We have to train our model.

During training, we show a large number of training examples and iteratively modify the weights to minimize the errors we make on the training set.
Moreover, the closer the error `E` is to `theta`, the better our model is.

Our goal will be to select our parameter vector `theta` such as E is as close to `theta` as possible.

## Gradient Descent

Suppose we randomly initialize the weights of our network so we find ourselves somewhere on the horizontal plane.

By evaluating the gradient at our current position, we can find the direction of steepest descent, and we can take a step in that direction. Then we'll find ourselves at a new position that's closer to the minimum than we were before.

We can reevaluate the direction of steepest descent by taking the gradient at this new position and taking a step in this new direction.

### Delta Rule and Learning Rates
