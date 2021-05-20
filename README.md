# NTU CZ4041 - Machine-Learning

This repository contains the source codes, the project report, presentation slides, as well as instructions to run the source codes for the CZ4041/CE4041: Machine Learning Course Project.

Youtube video link: 
https://www.youtube.com/watch?v=adQGHavsJMA

## Kaggle Competition (Dog Breed Identification)

![Image of competition page](https://github.com/ShearmanChua/CZ4041---Machine-Learning/blob/main/images/kaggle.jpg)

### Introduction

Machine Learning algorithms have been used in a multitude of applications to solve complex tasks; one such application of Machine Learning algorithms is in the field of Computer Vision. Computer Vision is defined as a field of study that seeks to develop techniques to help computers “see” and interpret the content of digital images such as photographs and videos.
For our team’s Course Project for CZ4041 Machine Learning, we will be utilizing Machine Learning to solve a Computer Vision task in the form of a Kaggle Competition problem. The Kaggle Competition we have chosen to tackle is the Dog Breed Identification Prediction Competition.

### Problem Statement

The Dog Breed Identification Prediction Kaggle Competition is a multiclass image classification problem which is a subset of the field of Computer Vision. In the competition, the dataset that we will be working on is the Stanford Dogs Dataset which is a strictly canine subset of the ImageNet dataset. The objective of the competition is to allow teams to practice fine-grained image categorization using various Machine Learning algorithms.
We are provided with a training set and a test set of images of dogs. Each image has a filename, that is its unique id. The dataset comprises 120 breeds of dogs. The goal of the competition is to create a classifier capable of determining a dog's breed from a photo. For the training dataset, the labels, or class of dog breed is provided for each image to allow us to use supervised learning methods to train a classifier to identify the various dogs’ breeds from the images. The test set consists of purely images without labels provided and is to be used by our trained classifier to make predictions on and predict the probability of each breed for each image in the test set.
The predicted probabilities of being in each dog breed class for each image are then saved into a CSV file to be uploaded onto the Dog Breed Identification Prediction Kaggle Competition leaderboard for evaluation. The evaluation score and ranked position of our prediction results will be based on the multi-class loss of the submission predictions, with 0.0 being the best possible evaluation score which means that our classifier is able to predict the dog breed for each image in the test set with a high level of confidence and accuracy.

### Project Methodologies

Our team mainly focused on developing solutions that utilizes State-of-the-Art (SOTA) Convolutional Neural Network(CNN) models, such as EfficientNets, InceptionResNet, NASNet etc. The reason behind this is that these SOTA CNN models are pre-trained on the ImageNet dataset, and since the Stanford Dogs Dataset used for the Dog Breed Identification Prediction Kaggle Competition is a subset of the ImageNet dataset, by applying the methodology of transfer learning, we will be able to achieve good classification performance by utilizing these models which have weights pre-trained on the ImageNet dataset.

### Results

![Image of results](https://github.com/ShearmanChua/CZ4041---Machine-Learning/blob/main/images/results.jpg)

The best multi-class loss obtained by our team for the Dog Breed Identification Prediction Kaggle Competition is 0.15290, which is obtained using the predictions made by the multi-modal CNN that has the Concatenate() layer for concatenating the feature maps of 5 individual SOTA CNN base models, trained on the original dataset from the Dog Breed Identification Prediction Kaggle Competition with no additional data appended. We are also able to observe that for the score of 0.15290, our team will take the 167th spot on the Leaderboard, out of 1280 places, which is equivalent to the top 13% of the Leaderboard.
