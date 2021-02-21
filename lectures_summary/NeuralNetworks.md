# Neural Networks

## The limits of Traditional Computer Programs

Computer programs are design to be very goof at two thingd :

-   Performing arithmetic really fast
-   explicity following a list of instructions

If you want to do stuff that are more interesting you have to define rules.
But this can be really hard as we don't know how our brain does it.

## The Mechanics of Machine Learning

Things we find most natural are learned by examples, not by formula.

For instance, a 2-year-old kid will be able to diffenciate cats and dogs by seeing examples and by beeing corrected by his parents if he has wrong.

Over our lifetime, our model becomes more and more accurate as we assimilate more and more examples.

**Deep learning is a subset of a more general field of artificial intelligence called _machine learning_, the idea of learning from examples.**

To train our model, we give a examples that it evaluates + a small set of instructions to modify the model when it makes mistakes.

We have input `x` in a vector form and the input `theha` as a vector of the model's parameters.
We have to find our `theta` parameters that optimize the accuracy score. There are many possible choices but most of the case, they are closed to each other. If not, we may want to collect more data to narrow these parameters.

To find the optimal value for the parameter vector `theta`, we have to use an _optimizer_.
An **optimizer** aims to maximize the performance of a ML model by iteratively tweaking its parameters until the error is minimized.

But we cannot explain all ML problems with linear models. So we attempt to build models that resemble the structure of human brain.
These algorithms can surpass other kinds of ML algorithms but also rivals the accuracies achieved by humans.

## The Neuron

The foundational unit of the human brain is the **neuron**.
The **neuron** is optimized to receive information from other neurons, process this information in a unique way, and send its result to other cells.

The strength of each connection determines the contribution of the input to the neuron's output. After beeing weighted by the strength of their respective connections, the inputs are summed together in the cell body.

Our artificial neuron takes inputs. Each of them is multiplied by a specific weight. This gives us **weighted inputs**.
These weighted inputs are summed together to produce the **logit** of the neuron. In many cases, this logit can also include a constant _bias_. The obtain logit is passed trough a f function to produce an output that will be given to the next neuron.

## Feed-Forward Neural Networks

A single neuron is not expressive enough to solve complicated problems.

The human cerebral cortex, responsible for human intelligence, is made up of 6 layers.

The bottommost layer = raw data <br>
Information is processed by each layer (hidden layers) and then passed on <br>
The highest layer (the 6th) which gives us the computed output.

We use the steps to define our neural network.

## Important notes to keep in mind

1. Layers of neurons are built like this : bottom layer (raw data) - hidden layers (process information) - top layer (gives an output)

2. Recommendations : hidden layers have fewer neurons than the input layer to force the network to learn compressed representations of the original input.

3. It is not required that every neuron has its output connected to the inputs of all neurons in the next layer.

4. The inputs and outputs are _vectorized_ representations.

## Linear Neurons and Their Limitations

Linear neurons are easy to compute with, but they run into serious limitations. Any feed-forward neural network consisting of only linear neurons can be expressend as a network with no hidden layers.

This is problematic because hidden layers are what enable us to learn important features from input data.

In order to learn complex relationships, we need to use neurons that employ some sort of non-linearity, by using **activation functions**.
