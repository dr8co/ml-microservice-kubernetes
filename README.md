[![CircleCI](https://dl.circleci.com/status-badge/img/gh/dr8co/ml-microservice-kubernetes/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/dr8co/ml-microservice-kubernetes/tree/main)

# Operationalize a Machine Learning Microservice API

!["Boston House Price Prediction"](./media/house_price.png "House Price")

## About

This is the final project for Udacity's Cloud DevOps Engineer Nanodegree.
The project tests one's ability to operationalize a Python flask app,
that serves out predictions (inference) about housing prices through API calls.

## Scenario

You are given a pre-trained `sklearn` model that has been trained to predict housing prices
in Boston according to several features,
such as average rooms in a home and data about highway access, 
teacher-to-pupil ratios, and so on.
The data was initially taken from [Kaggle](https://www.kaggle.com/c/boston-housing)

## Project Goal

The project goal is to operationalize this working, machine learning microservice
using [kubernetes](https://kubernetes.io/), which is an open-source system for
automating the management of containerized applications.

## Tasks

* Test the project code using linting
* Complete a Dockerfile to containerize this application
* Deploy the containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete GitHub repo with CircleCI to indicate that the code has been tested
