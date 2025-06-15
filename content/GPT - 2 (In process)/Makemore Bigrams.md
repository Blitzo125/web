---
title: Makemore
draft: true
tags:
---
 
the different language model neural net


bigram
only works with 2 chracters one given and then we predict the next one in the sequence 

what we did 
we first made bigram character level launage mode
using counting
in it we just made a 2d array of the counts of how many time a couple of characters occur eg aa ab ac etc and and made it a 27 by 27 tensor then got probablities for which character is most lickely to come next and then using torch.multinomial which will take the torch tensor of probablities and give out samples and then using those sample and a loop we can make more names

then using neural net
we implemented the same thing using a single layer perceptron with 27 newrons we found which chracter is likely to come next and then used backpropagation to get the desird probablities by changing the weighets of the network 


One-hot encoding is a technique in machine learning that converts categorical data into a numerical format


softmax used as the last activation function of a neural network to normalize the output of a network to a probability distribution over predicted output classes

noise refers to unwanted, random fluctuations or variations in data that can hinder model performance. This "noise" can be caused by errors in data collection, irrelevant features, outliers, or even malicious attacks. Essentially, it's the difference between the actual signal (meaningful information) and what the model is learning from the data.

Activation functions in neural networks determine whether a neuron should be activated or not, based on its input. They essentially decide if a neuron's input is relevant to the prediction process. The function then transforms the summed weighted input into an output that is passed on to the next layer or used as the final output