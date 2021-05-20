# NTU CZ4041 - Machine-Learning

This repository contains the source codes, the project report, presentation slides, as well as instructions to run the source codes for the CZ4041/CE4041: Machine Learning Course
Project.

## Kaggle Competition (Dog Breed Identification)

### Introduction

Machine Learning algorithms have been used in a multitude of applications to solve complex tasks; one such application of Machine Learning algorithms is in the field of Computer Vision. Computer Vision is defined as a field of study that seeks to develop techniques to help computers “see” and interpret the content of digital images such as photographs and videos.
For our team’s Course Project for CZ4041 Machine Learning, we will be utilizing Machine Learning to solve a Computer Vision task in the form of a Kaggle Competition problem. The Kaggle Competition we have chosen to tackle is the Dog Breed Identification Prediction Competition.

### Problem Statement

The Dog Breed Identification Prediction Kaggle Competition is a multiclass image classification problem which is a subset of the field of Computer Vision. In the competition, the dataset that we will be working on is the Stanford Dogs Dataset which is a strictly canine subset of the ImageNet dataset. The objective of the competition is to allow teams to practice fine-grained image categorization using various Machine Learning algorithms.
We are provided with a training set and a test set of images of dogs. Each image has a filename, that is its unique id. The dataset comprises 120 breeds of dogs. The goal of the competition is to create a classifier capable of determining a dog's breed from a photo. For the training dataset, the labels, or class of dog breed is provided for each image to allow us to use supervised learning methods to train a classifier to identify the various dogs’ breeds from the images. The test set consists of purely images without labels provided and is to be used by our trained classifier to make predictions on and predict the probability of each breed for each image in the test set.
The predicted probabilities of being in each dog breed class for each image are then saved into a CSV file to be uploaded onto the Dog Breed Identification Prediction Kaggle Competition leaderboard for evaluation. The evaluation score and ranked position of our prediction results will be based on the multi-class loss of the submission predictions, with 0.0 being the best possible evaluation score which means that our classifier is able to predict the dog breed for each image in the test set with a high level of confidence and accuracy.
