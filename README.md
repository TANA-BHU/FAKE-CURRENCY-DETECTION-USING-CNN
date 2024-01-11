
# Fake Note Detection using CNN

This project aims to detect counterfeit currency notes using deep convolutional neural networks (CNNs). It uses a self-generated dataset of genuine and fake Indian currency notes of denominations ₹10,₹20,₹50 ₹200, ₹500, and ₹2000. The project is based on the paper Counterfeit Currency Detection using Deep Convolutional Neural Network by K. S. S. Prasad et al.

## Datset

The 100 photographs in the collection were taken with a smartphone camera and include both real and counterfeit banknotes. Then perform image augmentaion and add 100-150 images from exsisting images. Edge detection, picture segmentation, and filtering techniques are used in the pre-processing of the images. There are 20% training and 80% testing sets in the dataset.

![image](https://github.com/TANA-BHU/FAKE-CURRENCY-DETECTION-USING-CNN/assets/103022959/df4de025-3539-47ea-ba3f-37a64a1d7a48)

## Model 
The model is a four-layer CNN and two fully conntected layers with the following architecture:<br/>

  - inputr layer : The input layer of shape is (64 x 64 x 3), which means that the input image has a height and width of 64 pixels and three color channels (RGB). The activation function used in this layer is ReLU.<br/>
  - The first convolutional layer has 32 filters of size 3 x 3.<br/>
    - The second convolutional layer has 32 filters of size 2 x 2, which means that each filter has a kernel size of 2 pixels in width and height. This layer reduces the spatial dimensions by half compared to the previous layer. The activation function used in this layer is also ReLU.<br/>
  - The third convolutional layer has 64 filters of size 2 x 2, which means that each filter has a kernel size of 2 pixels in width and height. <br/>
  - The fourth convolutional layer has 128 filters of size 2 x 2.<br/>
  - The flatten layer converts the output of all four convolutional layers into a one-dimensional vector with length equal to the number of filters in each convolutional layer multiplied by four. In this case, it becomes a vector with length equal to (32 x 32) + (32 x 32) + (64 x 64) + (128 x 128) = 2048 units.<br/>
  - The dense layer adds two fully connected layers with 256 units each. These are also called hidden or intermediate layers because they are not directly connected to any output units. They perform nonlinear transformations on the input vector using ReLU activation function.<br/>
  - The output layer adds one fully connected unit with 1 unit. This unit produces either a probability value between 0 and 1<br/>

  ## Usage
  To run the project, you need to have Python 3 and the following libraries installed:<br/>
  - TensorFlow <br/>
  - Keras <br/>
  - OpenCV <br/>
  - NumPy <br/>
  - Matplotlib <br/>

  ## Reference <br/>
  Counterfeit Currency Detection using Deep Convolutional Neural Network | IEEE Conference Publication | IEEE Xplore. (n.d.). Ieeexplore.ieee.org. Retrieved January 11, 2024, from https://ieeexplore.ieee.org/document/9105683

‌

