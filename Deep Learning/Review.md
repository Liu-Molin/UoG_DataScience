# Deep Learning Review

## Overview

The course is to teach us about modern techniques for machine learning with **high-dimensional image** and **sequence (time-series) data**.

## Foundations of Deep Learning

### Gradients
Working out how to improve the network

#### Overview
- How to change our models
  - Gradient calculations
  - Basic neural nets
  - Backpropagtion algorithm
- Computational graphs & automatic differentiaion
- Loss functions
- Initialisation strategies

### Stochastic Gradient Descent (SGD)
Sample a mini-batch of examples.

**Compared with Gradient Descent**

Most applications of SGD actually use a minibatch of several samples. 
**SGD** simply reduces the size of data,
which makes it faster and with lower RAM comsumed.

**Improvement of SGD**

Momentum will help to accelerate covergence.

$V_{t}=\beta V_{t-1}+(1-\beta) \nabla_{w} L(W, X, y)$

For more about the momentum in Gradient Descent see [Goh, "Why Momentum Really Works", Distill, 2017. <http://doi.org/10.23915/distill.00006>]

### Forward Propagation
@todo

Implement Forward Propagation
### Activation Functions
Without activation functions, the `Neural Network` will only perfom linear mapping from `input` to `output`. Because in that situation, the only mathematical operation during the forward propagation would be `dot-product`.

#### Different kinds of activation functions

**Features**

1. Sigmoid
   - Advantages:
     - Smooth gradient, preventing “jumps” in output values.
     - Output values bound between 0 and 1, normalizing the output of each neuron.
     - Clear predictions—For X above 2 or below -2, tends to bring the Y value (the prediction) to the edge of the curve, very close to 1 or 0. This enables clear predictions.
   - Disadvantages:
     - Vanishing gradient—for very high or very low values of X, there is almost no change to the prediction, causing a vanishing gradient problem. This can result in the network refusing to learn further, or being too slow to reach an accurate prediction.
     - Outputs not zero centered.
     - Computationally expensive
   - Hence, it's especially used for models where we have to predict the probability of anything exsits only between the range of 0 and 1.
2. Tanh
   - Advantages:
     - Zero centered—making it easier to model inputs that have strongly negative, neutral, and strongly positive values.
   - Disadvantages:
     - Like sigmoid function.
   - The tanh function is mainly used classification between two classes.
3. Rectified Linear Unit (ReLU)
   - Advantages:
     - Computationally efficient—allows the network to converge very quickly
     - Non-linear—although it looks like a linear function, ReLU has a derivative function and allows for backpropagation
   - Disadvantages:
     - The Dying ReLU problem—when inputs approach zero, or are negative, the gradient of the function becomes zero, the network cannot perform backpropagation and cannot learn.
4. Leaky ReLU:
   - Advantages:
     - Prevents dying ReLU problem—this variation of ReLU has a small positive slope in the negative area, so it does enable backpropagation, even for negative input values.
     - Otherwise like ReLU.
    - Disadvantages:
      - Results not consistent—leaky ReLU does not provide consistent predictions for negative input values.

### Bias
[Why we need bias?](https://stackoverflow.com/a/42063849/5989507)


Pooling

Convolutional Networks