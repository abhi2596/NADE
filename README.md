# Neural Auto Regressive Model for categorical distribution

NADE is an autoregressive model which uses a neural network to model the conditional distribution. 

In our case, the input is a pixel with a categorical distribution that takes values from 0 to 9. In the NADE paper, an algorithm is given for binary distribution and real valued distribution. But in our case the input is categorical. So the algorithm for categorical is close to binary the only difference is the use of softmax in the last layer. For training, we used NLL loss and passed the input as a target. For generating samples we have passed a learned noise input which gives the value of the first pixel we have used this pixel as the input to generate the next pixel in the way the generation of samples is done in a sequential manner. Hence though NADE is a good model to learn the distribution of dataset generating samples from it takes time as it follows a sequential pattern.


Architecture of NADE:
<img width="496" alt="NADE_architecture" src="https://user-images.githubusercontent.com/80634226/194641247-8094b9be-b90a-4b69-a7ce-c674a60ee8ef.png">

Training and Testing loss graph:

![NADE_graph](https://user-images.githubusercontent.com/80634226/194641772-f0bd0239-f8d5-4d65-a9e8-afc28144e608.png)


The model was trained on Fashion Mnist dataset. Dataset was preprocessed such that each pixel takes a value from 0-9 rather than 0-255.

Below are some of the samples generated after training the model. 

![NADE_sample1](https://user-images.githubusercontent.com/80634226/194641421-4ac07dbf-f7fd-433e-930e-71003bb9b42a.png)
![NADE_sample2](https://user-images.githubusercontent.com/80634226/194641446-4b0ba55b-ff63-4d78-b3a6-2ddd8306106b.png)

Paper on which the implementation and architecture are based on https://arxiv.org/pdf/1605.02226.pdf


