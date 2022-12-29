# Predicting Video Advertisement Classification through Text

## Introduction

Here, we will be working on text dataset which holds transcriptions for video of different ads. We preprocess the data into a more usable format and train our Deep learning LSTM model.

This model is based on Neural-Network Architecture and provides very high performance on sequence based datasets as it has a feedback structure helping the model remember sequence of data input and the changes that are happening.

Then we will be creating a Django based project which will be our base website that will be Hosted on Google Cloud.

## Building our Model

LSTM networks were designed specifically to overcome the long-term dependency problem faced by recurrent Neural Networks RNNs(due to the vanishing gradient problem). 

LSTMs have feedback connections which make them different to more traditional feedforward neural networks.

This property enables LSTMs to process entire sequences of data (e.g., Time Series) without treating each point in the sequence independently, but rather, retaining useful information about previous data in the sequence to help with the processing of new data points.

## Creating the Django Project

Django is a free open source web application framework written in Python. It includes advanced functionality like authentication support, management and admin panels, contact forms, comment boxes, files upload support, and more.

By using this framework instead, We just need to configure the components to match our requirements.

## Hosting on Google Cloud

This is the last step in the process of building the project  where we host the newly build website using the Django framework.

We will be using the Google App Engine(GAE) for hosting the website and understand how exactly the virutal servers and the cloud system works.

With this completed, we would be able to access our website and run the model from anywhere across the internet.
