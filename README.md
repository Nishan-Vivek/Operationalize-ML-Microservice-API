[![Nishan-Vivek](https://circleci.com/gh/Nishan-Vivek/Operationalize-ML-Microservice-API.svg?style=svg)](https://app.circleci.com/pipelines/github/Nishan-Vivek/Operationalize-ML-Microservice-API)


# Operationalize a Machine Learning Microservice API Project

A series of scripts and instructions that deploys a bundled Machine Learning API flask application into a local Kubernetes cluster. 

## Specifications

Specifications as per Udacity course requirements can be found [here](./documentation/project_specifications.md).

## Project Overview

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

Project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:
* Test your project code using linting
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

## Prerequisites & Assumptions

- Github and linked CircleCI accounts
- Workstation with a BASH terminal.
    - This project was tested on an Ubuntu 20.04 workstation.
- Working Docker, Kubectl, Python3.7, hadolint and Minikube Installations on your workstation.
- Knoledge of working with python3 virtual environments

## Usage Instructions

### Download Project Repo

Clone or download the project GIT repo to your workstation. 

***In the Repo***
​

***app.py*** - The flask application to be deployed

***Dockerfile*** - Dockerfile to build application container image

***make_prediction.sh*** - Script to test the running application api

***Makefile*** - Helper makefile scripts to setup app locally

***README.md*** - This document  

***requirements.txt*** Application python dependenices to be used with pip

***run_docker.sh*** Script to build and run the appliaction in a docker container

***run_kubernetes.sh*** Script to deploy the app in a local kubernetest cluster and forward appropate ports

***upload_docker.sh*** Helper script to upload built image to dockerhub

***/.circleci*** CircleCI configuration files to run an automated linting of the application files 

***/documentation*** - Additional documents  

***/model_data*** - Files requried for the flask application

### Running Locally

1. Create and activate a python3.7 virtual environment by running `make setup`
    - All following instructions must be run with the environment activated
2. Install dependenices with `make install`
3. You can lint the applicaiton and docker files with `make lint` at this point if you wish.
4. Run the python application with `python app.py`
5. Verfy the api is listing by visiting localhost:80

### Running in Docker and uploading to dockerhub

1. Update the Dockerfile and `run_docker.sh` with your desired dockerhub tags
2. `run_docker.sh` will build and start the container with the container port forwarded from localhost:8000
3. Generate a prediction by running `make_prediction.sh` in a another terminal window.
4. You can stop the running container by pressing `ctrl-c` in the main terminal window. 
5. Update `upload_docker.sh` to match your dockerhub tag changes with the Dockerfile. Run `upload_docker.sh` to upload your container image to dockerhub.

### Running in kubernetes

1. Start a local kubernetes cluser with minikube
2. Update `run_kubernetes.sh` with your dockerhub tags
3. Deploy the app with `run_kubernetes.sh`
4. Generate a prediction by running `make_prediction.sh` in a another terminal window.
