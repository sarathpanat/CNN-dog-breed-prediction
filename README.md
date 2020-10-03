# CNN-dog-breed-prediction

So,this is an ML application on dog breed prediction. Here if we input an image of human, it will show that the image contains a human and it shows the breed which has resemple to human face and if you input a dog image it will predict the dog breed, I mean the dog out of 133  different breed that we used for training.

#Dog-breed-classifier.ipnb(Iam explaining about this file down below that I have coded for the above solution)
Dataset

10901 Human images
8351 Dog images - 133 different dog breed
Human Detection

Opencv - Haar feature-based cascade classifier
Dog Detection

Pre-trained VGG-16 model along with weights on ImageNet
CNN - Scratch

5 Convo layers with Relu activation
kernal size(3*3) with padding
3 MaxPooling layers
Flattened output will be fed to a Fully Connected Layer which then uses ReLU activation function
Dropout of 0.2 to avoid overfitting
Loss function : Cross Entropy ,Optimiser : adam optimiser with lr=0.001 ,Epoch: 30
Result : Test loss = 3.124 , Accuracy : 24%

CNN - Transfer Learning

VGG-16
Add last layer as linear layer with 133 output nodes
Loss function : Cross Entropy ,Optimiser : adam optimiser with lr=0.001 ,Epoch: 30
Result : Test loss = 1.028751 , Accuracy = 71%

So,after solving the problem with an accuracy of 71%, I just tried 3 ways to improve accuracy.
1.Using different pre-trained models
2.Increasing epoch size
3.Increased epoch size and used exponantial learning rate instead of constant.

#CCN-vgg19.ipynb
-Trained with 50 epoch - 74% accuracy
#CNN-inception_v3
-Trained with 30 epoch - 81%accuracy
-Trained with 100 epoch - 83%accuracy
-Trained with 100 epoch and  learning rate = exponential
  lrate = initial_lrate * exp(-k*t)
  initial_lrate = 0.1
  k = 0.1
accuracy of 84%
#CNN-resnet18
-Trained with 30 epoch - 82% accuracy

So,I have improved the accuracy by 13% by using inception with exponantial learning rate.
