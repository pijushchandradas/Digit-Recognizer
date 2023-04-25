#Handwritten Digit Recognition
This is a convolutional neural network (CNN) model for recognizing handwritten digits. The architecture of this model is as follows:

Conv2D layer with input shape of (28,28,1), 32 filters, kernel size of (5,5), padding set to "same", and activation function set to ReLU.
BatchNormalization layer.
Dropout layer with a rate of 0.1.
The above three layers are repeated twice with slightly different parameters.

Another Conv2D layer with 64 filters, kernel size of (3,3), padding set to "valid", and activation function set to ReLU.

Another BatchNormalization layer.

MaxPool2D layer with a pool size of (2,2), strides of (2,2), and padding set to "same".

Another Dropout layer with a rate of 0.1.

Another Conv2D layer with 128 filters, kernel size of (2,2), padding set to "same", and activation function set to ReLU. This layer also includes L2 regularization with a parameter of 0.001.

Another BatchNormalization layer.

MaxPool2D layer with a pool size of (2,2) and padding set to "same".

Another Dropout layer with a rate of 0.2.

Another Conv2D layer with 128 filters, kernel size of (2,2), padding set to "valid", and activation function set to ReLU.

Another BatchNormalization layer.

Another Dropout layer with a rate of 0.2.

Another Conv2D layer with 256 filters, kernel size of (2,2), padding set to "valid", activation function set to ReLU, and L2 regularization with a parameter of 0.001.

Another BatchNormalization layer.

The above two layers are repeated with slightly different parameters.

MaxPool2D layer with a pool size of (2,2), strides of (2,2), and padding set to "same".

Another Dropout layer with a rate of 0.2.

Another Conv2D layer with 512 filters, kernel size of (2,2), padding set to "valid", activation function set to ReLU, and L2 regularization with a parameter of 0.001.

Another BatchNormalization layer.

Flatten layer.

The above four layers are repeated with slightly different parameters.

Dense layer with 10 output nodes and activation function set to softmax.
The model uses L2 regularization and dropout layers to reduce overfitting. The input shape for the model is a grayscale image of size 28x28. The model is trained to classify handwritten digits into one of the ten possible classes (0-9).
