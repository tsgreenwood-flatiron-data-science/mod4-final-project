# mod4-final-project
Image classification problem from datahack contest https://datahack.analyticsvidhya.com/contest/practice-problem-identify-the-apparels/
The code is heavily influenced by https://www.analyticsvidhya.com/blog/2019/01/build-image-classification-model-10-minutes/
Tara Greenwood

Problem Statement
We have total 70,000 images (28 x 28), out of which 60,000 are part of train images with the label of the type of apparel (total classes: 10) and rest 10,000 images are unlabelled (known as test images). The task is to identify the type of apparel for all test images. Here are the description codes for each of the apparel labels.

Label	Description
0	T-shirt/top
1	Trouser
2	Pullover
3	Dress
4	Coat
5	Sandal
6	Shirt
7	Sneaker
8	Bag
9	Ankle boot  

First, we train-test-split the labeled train images. Next, we used TensorFlow.keras to build our deep learning model. We fitted it to the data, compiled it, and measured the cross validation accuracy. After 10 epochs the model displayed over 92% accuracy, so we pickled the model to speed reproducibility. 
The contest has a set of unlabeled images. 
We populated a dataframe with labels from our model, exported it as a csv, and submitted it online to the contest online, receiving a score of 0.9145. Not too bad for a neural network trained in-house!