# Competing Hidden Units

This is a Pytorch implementation of this [Biological Learning Algorithim](https://www.pnas.org/content/116/16/7723) largely based on [the author's code](https://github.com/DimaKrotov/Biological_Learning/blob/master/Unsupervised_learning_algorithm_MNIST.ipynb) but converted to Pytorch for CUDA acceleration

### Basic Idea

Backpropogation, while tremendously efficient for training a neural network, is not biologically plausible. Backpropogation aims to improve the performance of the entire neural network. The neurons in our brain are localized and are unaware of the overall performance of our internal neural networks. The proposed new learning algorithim, and its appromixation method, allow for both speedy learning and mimics the bottom-up, neuron level, learning that exists in our brains.

### Peculiar Properties

Perhaps the most astonishing characteristic this algorithim has is a more visually intuitive understanding of what each neuron is doing and how it changes with each successive epoch. Below is the effect of training a network with one hidden layer of 1,000 nodes for 100 epochs. They are colormaps where white = 0

![one](./one.gif) ![two](./two.gif)

On the left you cannot determine what exactly is going on, this is because the darkest blue is the most negative weight and the darkest red is the largest postivive weight. Normalizing each channel, so that scale of negative values is the same as the scaling of the positive values, shows that each neuron understands a single digit. 
