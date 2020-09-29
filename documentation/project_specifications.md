# Operationalize a Machine Learning Microservice API Project

Udacity Project: Operationalize a machine learning microservice using kubernetes.

## Project Overview

You are given a pre-trained, sklearn model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on the data source site. This project tests your ability to operationalize a Python flask app—in a provided file, app.py—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

## Project Tasks

Project goal is to operationalize this working, machine learning microservice using kubernetes, which is an open-source system for automating the management of containerized applications.

- Test your project code using linting
- Complete a Dockerfile to containerize this application
- Deploy your containerized application using Docker and make a prediction
- Improve the log statements in the source code for this application
- Configure Kubernetes and create a Kubernetes cluster
- Deploy a container using Kubernetes and make a prediction
- Upload a complete Github repo with CircleCI to indicate that your code has been tested

## Starter Repo

https://github.com/udacity/DevOps_Microservices.git


## Rubric

### The Files Submitted

|Criteria   |Meets Specifications   |   |
|---|---|---|
|All files are submitted   |The submitted repository includes a .circleci folder, a README.md file, a Dockerfile and Makefile, as well as an app.py file, a prediction script, and the necessary scripts to run and upload a microservice on Docker and Kubernetes.
There should also be two output text files: docker_out.txt and kubernetes_out.txt that include the log output after a prediction is made, given some sample input data. | :heavy_check_mark:  |
|.circleci folder is included   | A .circleci folder is included in the Github repository. The directory holds a config.yml that checks the project code for errors. Your project should pass, as indicated by a CircleCI status badge in the repository README.  | :heavy_check_mark: - Using AWS System Manager instead  |


|Criteria   |Specifications   |   |
|---|---|---|
|Parameters   |The more the better, but an exaggerated number of parameters can be messy ( say, 10 or more ). 1 or 0 is definitely lacking.   |  :heavy_check_mark:   |
|Resources   |This is the mandatory section of the script, we are looking for a LoadBalancer, Launch Configuration, AutoScaling group a health check, security groups and a Listener and Target Group.   | :heavy_check_mark:  |
|Outputs   |This is optional, but it would be nice to have a URL here with the Load Balancer DNS Name and “http” in front of it .   | :heavy_check_mark:  |
|Working Test   |If the student provides a URL to verify his work is running properly, it will be a page that says “it works! Udagram, Udacity”   | :heavy_check_mark:  |

#### Load Balancer

|Criteria   |Meets Specifications   |   |
|---|---|---|
| Target Group  |The auto-scaling group needs to have a property that associates it with a target group. The Load Balancer will have a Listener rule associated with the same target group   |:heavy_check_mark:   |
|Health Check and Listener   |Port 80 should be used in Security groups, health checks and listeners associated with the load balancer   | :heavy_check_mark:  |

#### Auto-Scaling

|  Criteria |Meets Specifications   |   |
|---|---|---|
|Subnets   |Students should be using PRIV-NET ( private subnets ) for their auto-scaling instances   | :heavy_check_mark:  |
|Machine Specs   |The machine should have 10 GB or more of disk and should be a t3.small or better.   | :heavy_check_mark:  |
|SSH Key   |There shouldn’t be a ‘keyname’ property in the launch config   |:heavy_check_mark:   |


#### Bonus

