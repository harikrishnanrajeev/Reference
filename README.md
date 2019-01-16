# Reference
Collating links , articles , git hubs for reference

1) https://storage.googleapis.com/openimages/web/index.html
(Open Images Dataset V4 - 15,440,132 boxes on 600 categories - 30,113,078 image-level labels on 19,794 categories)

2) CNN References and Links

    2.1) http://setosa.io/ev/image-kernels/  (To understand how convolutions work)
     
    2.2) https://docs.gimp.org/2.6/en/index.html
     https://docs.gimp.org/2.6/en/plug-in-convmatrix.html    (convolution matrix)
     https://docs.gimp.org/2.6/en/plug-in-dog.html   (Gaussian filter)
     
    2.3) https://medium.com/impactai/cnns-from-different-viewpoints-fab7f52d159c
    
    2.4) http://neuralnetworksanddeeplearning.com/chap1.html
    
    2.5) https://classroom.udacity.com/courses/ud188    
   

3) Good to Read

    3.1) https://medium.com/@cody.marie.wild/machine-learning-writing-month-17b80b88f1dd

4) Mathematics

    4.1) https://pimbook.org/
    4.2) https://explained.ai/matrix-calculus/index.html
    
5) Bayesian

    5.1) http://bayesiandeeplearning.org/
    
6) Object detecion:

    6.1) https://medium.com/ilenze-com/object-detection-using-deep-learning-for-advanced-users-part-1-183bbbb08b19
        (Three part series which will elaborate on Object Detection in images using CNN)
    
    6.2) https://github.com/simonm3/maskr  (nice details of Mask-RCNN repo's keras and pytorch)
 
 7) Notes
    Dropout:
    . Type of regularization
. Its a training scheme that masks neurons at every step
. Based on paper by Nitish Srivastawa , Jeff Hinton et all - "Drop out: A simple way to prevent neural networks from overfitting"
. Dropout throws away activations with a probability p. (p=0.5 is common)
. Drop out of input is unusual but possible. Usually we use dropout for hidden neurons
. Too much dropout results in underfitting
. During Test time, dropout is turned off , because we want to be as accurate as possible
. Why we only applied dropout to fully-connected layers and all and not to convolutions layers ?
	Dropout is usually not applied to convolutional layers. It is not needed because convolutional layers have considerable 
	inbuilt resistance to overfitting
	The reason is that shared weights mean that convolutional filters are forced to learn from across the entired image.
	This makes them less likely to pick on local idiosyncracies in the training data. And so there is less need to apply other regularizers 
	, such as dropout.
	In the original dropout papaer, it was mentioned that adding dropout to convolutional layers brings down the error rate. But current SoTA architectures
	do not have dropout in the convolutional part of the architecture. 
. Why do we need both batchnorm and dropout , both does regularization ?.
	One great thing about dropout is that it has a parameter which indicates how much to dropout.
	
. Dropblock - https://github.com/miguelvr/dropblock
. Dropfilter - https://arxiv.org/abs/1810.09849

. Embeding dropout - It drops out some activations of the embedding matrix. 
. Dropout uses Bernoulli random variables , in which you are either using an activation (mulyiply by 1) or dropping it completely (muliply by 0) 
