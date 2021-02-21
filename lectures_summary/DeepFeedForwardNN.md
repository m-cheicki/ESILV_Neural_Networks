# Deep Feed Forward Neural Networks

Deep Feed Forward Networks are also called **Feed Forward Neural Networks** or **Multi Layer Perceptrons (MLP)**.

**A feed forward network defines a mapping of a function `y = f(x;theta)` and learns the value of the parameters `theta `**

The term **deep learning** comes from the depth of nested functions. The last layer is called the **output layer**.

Most neural networks use an affine transformation controlled by learned parameters, followed by a fixed non-linear function called **activation function**.

## Feed Forward Neural Networks

Bottom layer = pulls input data
Top layer = computes outputs
Hidden layers = middle layers (between top and bottom layers)

For now, we are studying NN with connections that only traverse from a lower layer to a higher layer. There are no connections between neurons in the same layer, and there are no connections that transmit data from a higher to lower layer.

### Output units

There are three activation functions :

-   ReLU : Rectified Linear Unit <br>
    applied to outputs of a linear transformation => non-linear trnasformation. The function remains very close to linear. It uses `f(z) = max(0, z)` <br/>
    **Hockey-stick-shaped response**

-   Sigmoid function<br>
    if logit very small = 0 <br>
    if logit very large = 1 <br>
    else the neuron assumes an **S-shaped response** <br>
    Range is `[0;1]`

-   Tanh function <br>
    Similar to Sigmoid but Zero-centered because range is `[-1;1]`

### The softmax layer

Unlike in other kinds of layers, the output of a neuron in a softmax layer depends on the outputs of all the other neurons in tis layer. <br>
This is because we require the **sum of all the outputs to be equal to 1**

A strong prediction would have a single entry in the vector close to 1, while the remaining entries were close to 0.

A weak prediction would have multiple possible labels taht are more or less equally likely.
