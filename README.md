# Block-Based Compressed Sensing of images with Neural Networks

In this research project I implemented Block-Based Compressed Sensing of images with Neural Networks based on "A DEEP LEARNING APPROACH TO BLOCK-BASED COMPRESSED SENSING OF IMAGES" paper by Amir Adler, David Boublil, Michael Elad, Michael Zibulevsky.

You can find the original paper here: https://arxiv.org/pdf/1606.01519.pdf

## Implementation
I implemented this project in python3 using Keras.

The Neural Network looks something like this (The number of nodes in each hidden layer depends on R, B, and T): 
R is compression rate.

B is sensing block size.

T is redundancy factor.


![img](NN.png?raw=true "Train")

## Process
I started with the best hyper parameters they found in their research. R = 0.25, T = 8 and K = 2 (#number of reconstruction layers)

Having R, T, K as fixed numbers, I changed the sensing matrix size to B = 8, 16, 32. I shared the results in separate files. (Loss and PSNR plots, reconstrcuted and original images are shown in the codes)

Then I picked the best sensing block size and I trained model again with R = 0.1, 0.2, 0.3, 0.4, 0.5. (I didn't share the results here) 


As expected, when R increased the Average PSNR increased as well.

Here are the results shown on train and test set:

![img](train_avg-PSNR.png?raw=true "Train")


![img2](test-Avg-PSNR.png?raw=true "Test")

## Training
I trained on AWS EC2 p2.xlarge instance.
