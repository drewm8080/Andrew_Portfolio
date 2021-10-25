## Andrew Moore's Portfolio

## [Posture Classification using Neural Networks](https://github.com/drewm8080/Posture-Classification-Models)

# Mobile Net
We used MobileNet pre-trained on imagenet, froze its convolution layers, and retrained its fully connected layers on our data. Our data set is all the three tranches excluding the null and unknown values, with about 36k images. We trained on 30 thousand images with a 0.5 validation split and tested the model on the remaining 6 thousand. The model was trained on Google Colab. The results are as follows:
![image](https://user-images.githubusercontent.com/71193439/138619973-e78881a8-e6cd-42f7-a098-284adf73b8bc.png)
![image](https://user-images.githubusercontent.com/71193439/138619981-bdc2667f-2ec9-4ca8-817c-860603117072.png)

# Inception-ResNet v2
Similar to MobileNet, we used the same training, validation, and test set. And we froze the convolutional layers pre-trained on imagenet and retrained the fully connected layers. The model was trained on Google Colab. The results are as follows:
![image](https://user-images.githubusercontent.com/71193439/138620013-b4c55d49-31cf-45a3-87a2-a0b3ace888f5.png)

# MobileNet + Edge Detection
We also implemented some preprocessing techniques. We combine the original image and the edge-detected image together into the training set. The following models were trained on the CARC system from USC. We tried MobileNet pre-trained on imagenet, first training on the original images. Then we trained the model on edge-detected images combined with original images to see if there is any improvement.

**Original Images**
![image](https://user-images.githubusercontent.com/71193439/138620992-81221af4-053a-4f39-a964-17f7100b91e6.png)

**Edge-detected + Original Images**
![image](https://user-images.githubusercontent.com/71193439/138621011-b28767b1-4bb3-476d-95f2-da978b14edf8.png)

# Final Results 
![image](https://user-images.githubusercontent.com/71193439/138621056-4ef754ed-4028-4e0b-b27c-ac1df5619873.png)
