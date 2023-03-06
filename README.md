[![CircleCI](https://dl.circleci.com/status-badge/img/gh/dr8co/ml-microservice-kubernetes/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/dr8co/ml-microservice-kubernetes/tree/main)

# Operationalize a Machine Learning Microservice API

!["Boston House Price Prediction"](./media/house_price.png "House Price")

<!-- TOC -->
  * [About](#about)
  * [Scenario](#scenario)
  * [Project Goal](#project-goal)
  * [Tasks](#tasks)
  * [Submission Info](#submission-info)
  * [Running the Project](#running-the-project)
    * [Running the app](#running-the-app)
      * [Locally](#locally)
      * [With Docker](#with-docker)
      * [With Kubernetes](#with-kubernetes)
<!-- TOC -->

## About

This is the final project for Udacity's Cloud DevOps Engineer Nanodegree.
The project tests one's ability to operationalize a Python flask app,
that serves out predictions (inference) about housing prices through API calls.

## Scenario

You're given a pre-trained `sklearn` model that has been trained to predict housing prices
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

## Submission Info

This submission satisfies the mentioned requirements.
Here's a brief overview of some files:

* [app.py](./app.py): Flask api server, exposes and endpoint /predict that will predict housing prices in Boston using a pre-trained model.

* [Dockerfile](./Dockerfile): Container building instructions for flask api.

* [run_docker.sh](./run_docker.sh): A script that builds a Docker image of the app.

* [upload_docker.sh](./upload_docker.sh): A script that uploads the built Docker image to DockerHub.

* [run_kubernetes.sh](./run_kubernetes.sh) A script to deploy the containerized app to a k8s cluster.


## Running the Project

This project depends on python3.7, Docker, Make, and Kubernetes (or Minikube, locally.)

### Running the app

#### Locally

```zsh
# Create and activate a virtual python environment
python3.7 -m venv ~/.venv
source ~/.venv/bin/activate

# Install dependencies
make install

# Run app.py
python app.py

# When the api is running and ready to listen for connections
# run a simple test
./make_predictions.sh
```

#### With Docker

```zsh
./run_docker.sh
```

#### With Kubernetes

```zsh
./run_kubernetes.sh
```
