# NeuralNetworkPractice

### Please see the ipynb file to see full code running analysis below is the markdown of the file
 
### Hello World of Neural Network
#### MNIST is a set of images of handwritten digits
#### The problem is to classify each greyscale image into the corret category, namely '0', '1'..., '9'
#### There are 60000 training images and 10000 images

Each image is a data point and it is called sample
And each data points typically belong to one or more categories
Each Mnist image belongs to exactly one category or class 0,1,2. etc.
The class of a sample is known as its label

1. load
2. preprocess
3. build network
4. train
5. test

The Mnist dataset is one of several Tensorflow dataset

### 1. Load
#### Data is stored in special multidimensional arrays tensors, There are 60000 greyscale images in the training set, Each image is 28pxl x 28pxl
    - the training set is a data container with 60000 x 28 x 28 elements
    - the training lavels are stored in a 60000 element vector


### 2. Preprocess
The data has to be 'reshaped' to a form that is acceptable to the network

The network will expect samples as vectors (1D arrays) of floating point values


#### The network is also expecting categorically encoded labels
a vector with a single nonzero element corresponding to the category

Each label will be turned in to a 10 element vector with a single 'hot' nonzero entry

for example 7 is encoded as (0,0,0,0,0,0,0,1,0,0)

One - hot encoding



### 3. Build

The second softmax layer outputs a vector whose elements form a probability distribution

    - the numbers are nonnegative and sum to one - a probability distribution
    - outputs are interpreted as probabilities of membership of each class: the probability that the input sample is labeled '0' or '1' or '2' and so on


However the network is not yet ready. We must specify a loss function, an optimiser and one or more training metrics

The loss function quantifies how far off the network prediction is from the target

The optimiser makes parameter adjustments in the training loop and metrics report on progress



### 4. Train

We have to decide:

    - the number of samples processed in a single pass of the training algorithm - the mini-batch size
    - the number of complete passes through the entire training set - the number of epochs



### 5. Test

Remember that the network does not have eyes and a visual cortex. The network only mapped 784 element vector to a 10 component probability factor.
