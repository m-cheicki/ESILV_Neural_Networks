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

In addition to the weight paramter defined in our neural network, learning algorithms require a couple of additional parameters called **hyperparameters**.

One of them is the _learning rate_.

In practice, at each step of moving perpendicular to the contour, we need to determine how far we want to walk before recalculating our new direction. This distance needs to depend on the steepness of the surface. Because, the closer we are to the minimum, the shorter we want to step forward. We know we are close to the minimum, because the surface is a lot atter, so we can use the steepness as an indicator of how close we are to the minimum. However, if our error surface is rather mellow, training can potentially take a large amount of time.

Picking the learning rate is a hard problem : if too small, the training process will be too long ; if too big, we will start diverging away from the minimum.

### Gradient Descent with Sigmoid Neurons

Assume we have a neural network with a input set, a linear hidden layer and a sigmoid output layer.
The neuron computes the weighted sum of its inputs, the logit z. Then, it feeds its logit into the input function to compute our final output y.

## Backpropagation Algorithm

When we use a Feed-Forward Neural Network, the information flows forward through the network. The input provides initial information, then propagates up to the hidden layers and finally produces the output.
During training, the propagation continue onward until it produces a cost function.

The Back-Propagation allows the information from the cost to flow backward through the network in order to compute the gradient.
Actually, back-propagation refers only to the method for computing the gradient, while another algorithm, such as stochastic gradient descent, is used to perform learning using this gradient.

When training a network, we repeat the following steps (for n epoches):

-   Perform forward pass.
-   Calculate the delta to be added to each weight via backpropagation.
-   Update the weights.
    The backpropagation focuses on step 2 while proposes an approach for
    computing \delta wi.

Explaination links :

-   [3Blue1Brown](https://www.youtube.com/watch?v=aircAruvnKk&list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi&index=1&ab_channel=3Blue1Brown)
-   [The Coding Train](https://www.youtube.com/watch?v=XJ7HLz9VYz0&list=PLRqwX-V7Uu6aCibgK1PTWWu9by6XFdCfh&ab_channel=TheCodingTrain)
