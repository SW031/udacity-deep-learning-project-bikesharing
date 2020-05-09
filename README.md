# Udacity Deep Learning Nanodegree Program

## Project 1: Your First neural network - Predicting Bikesharing patterns
In this project, I'll build a neural network to solve a prediction problem and use it to predict daily bike rental ridership. Building a neural network from scratch provides better understanding of gradient descent, backpropagation, and other concepts that are important to know before moving to higher level tools such as PyTorch.

The data comes from the [UCI Machine Learning Database](https://archive.ics.uci.edu/ml/datasets/Bike+Sharing+Dataset).

## Setup Instructions
Setup instructions taken from [here](https://classroom.udacity.com/nanodegrees/nd101/parts/94643112-2cab-46f8-a5be-1b6e4fa7a211/modules/07d52f20-312f-448d-9980-71d162caa76e/lessons/2ced92c6-f377-4d29-b5aa-8e887f1e4a6f/project).

## Training & Validation Loss Graph
![Training and Validation Loss Graph](https://user-images.githubusercontent.com/53707417/81486126-f4c8df00-9252-11ea-8787-80dd92cb9f94.png)

## Predictions Check Graph
![Predictions Check Graph](https://user-images.githubusercontent.com/53707417/81486148-2e99e580-9253-11ea-8154-4d401c84e2bf.png)

## Conclusions
The current model will be enough for predicting the dataset as the model performs pretty well for the entire data, but analysing the data a bit will lead to some unique characteristics.

It is visible from the results that the december holiday season predictions performed poorly because prior information about such trends was not captured in the data, i.e the dataset that we trained on does not have information on holiday season even for the previous year. So when a new pattern is experienced the model performance is bad. This can be solved by training the model with more data, possibly randomised data so that the model captures such patterns and predicts well. Think of it like you are the manager for the bike sharing service, this is your first year there and you know about the trends from January to October, knowing the data you are most likely to anticipate that the trends from your previous experience will hold. Right? So you would make preparations accordingly, but once december hits, the holiday starts and then people stay at their houses maybe and there is a slump, as this is your first time here you only expected as per your experience. This is the same case with the model. We will have this in mind for the next December. Right? If we notice properly, the holiday season extends over a week, but we find that the days near christmas which are considered as holiday season are marked as non-holidays. So a new feature marking the holiday season will be really helpful along with training over additional holiday season data. 
