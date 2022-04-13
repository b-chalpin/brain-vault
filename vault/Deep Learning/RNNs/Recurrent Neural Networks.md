# Recurrent Neural Networks (RNNs)
So far, we have seen data that are all drawn from the some distrbution, or all samples are  independently and identically distributed (i.i.d) in previous models such as the [[Convolutional Neural Network]] or [[Multi-Layer Perceptron]].

What happens when we want to work with data in a sequence where order matters? What do we do when we are not given a sequence, but told to continue it? We use Recurrent Neural Networks (RNNs).

> ..._recurrent neural networks_ (RNNs) are designed to better handle sequential information. RNNs introduce state variables to store past information, together with the current inputs, to determine the current outputs.

[Source](https://d2l.ai/chapter_recurrent-neural-networks/index.html)


### The Problem
Let us denote a variable $x_t$, where we can think of $t$ as the index in the sequence and $t \in \mathbb{Z}^+$. Note that $t$ will typically be discrete and vary over integers. Suppose we want to predict the value of $x_t$ at a timestamp $t$. We will use the equation $x_t \sim P(x_t | x_{t-1}, ..., x_1)$.

Most of what RNNs try to do is estimate $P(x_t | x_{t-1}, ..., x_1)$.


