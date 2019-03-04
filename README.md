# Block-Based Compressed Sensing of images with Neural Networks

In this project I implemented Block-Based Compressed Sensing of images with Neural Networks based on "A DEEP LEARNING APPROACH TO BLOCK-BASED COMPRESSED SENSING OF IMAGES" paper by Amir Adler⋆, David Boublil†, Michael Elad ⋆, Michael Zibulevsky⋆

## Implementation:
I implemented this project in python3 using keras.

## Process:
I started with the best hyper parameters they found in their research. R=0.25 and T=8 and K=2 (#number of reconstruction layers)

Having R, T, K as fixed numbers, I changed the sensing matrix size to B=8,16,32. I shared the results in separate files. 

Then I picked the best sensing block size and I trained model again with R(compression rate) = 0.1, 0.2, 0.3, 0.4, 0.5. (I didn't share the results)

As expected, when R increased the Average PSNR increased as well.


## Training:
I trained on AWS EC2 p2.xlarge instance.
