# Digit Classification using Neural Networks
In this project, a digit classification model is built using both the TensorFlow library as well as the regular NumPy library. The efficiency 
between both the impementations is compared and the best one is chosen as the final model. The accuracy was found out to be around 96% for the
data set obtained from MNIST.

## Structure
We are using a total of 3 layers. Each layer has multiple neurons and each neuron has multiple weights(no of inputs) and one bias. First layer neurons don't have any weight. The dimensions of bias in a layer are number of neurons in that layer x 1. So for 30 neurons bias dimensions are 30 x 1 in that layer. A list of such numpy arrays gives us overall bias values of neural network. Similarly the dimensions of weights are number of neurons in present layer x number of outputs of previous layer.
A list of all such numpy arrays gives us weights of each layer neurons clubbed together.

## Training
For training we use existing dataset and divide it into mini batches. The dataset is shuffled before choosing mini batches to ensure consistency in curve forming. The training data contains tuples of input data and output label. epochs give us the number of iterations that model works on dataset. eta specifies learning rate to adjust bias and weight values.
This line creates all mini batches
We now calculate gradient of biases and weights and update the weights and biases of every neuron. In the context of neural network training, backpropagation typically computes the derivatives of the cost function with respect to the weights and biases. The gradients are updated for all the data present in a mini batch and sum of all changes is taken into account. These changes are averaged while updating bias and weights of a neuron.

Implementation using Tensorflow library hides all of these details and provides better abstraction.
