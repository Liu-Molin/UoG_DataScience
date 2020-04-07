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



Pooling

Convolutional Networks