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
|All files are submitted   |The submitted repository includes a .circleci folder, a README.md file, a Dockerfile and Makefile, as well as an app.py file, a prediction script, and the necessary scripts to run and upload a microservice on Docker and Kubernetes.  There should also be two output text files: docker_out.txt and kubernetes_out.txt that include the log output after a prediction is made, given some sample input data. | :heavy_check_mark:  |
|.circleci folder is included   | A .circleci folder is included in the Github repository. The directory holds a config.yml that checks the project code for errors. Your project should pass, as indicated by a CircleCI status badge in the repository README.  | :heavy_check_mark: - |

### Code Quality & Enhancement

|Criteria   |Specifications   |   |
|---|---|---|
|Extend app.py to log a prediction value  |TAdd an additional logging statement to app.py that prints as “info” the output prediction for some given input data.   |  :heavy_check_mark:   |
|The project shows the proper use of documentation   |The README file includes a summary of the project, how to run the Python scripts and web app, and an explanation of the files in the repository.   | :heavy_check_mark:  |
|The project passes linting via a Makefile   |Both the Dockerfile and the python file pass linting using pylint and hadolint. This may involve selectively customizing lint overrides in both tools. The lint should be run for both tools via the command make lint. Circleci build server validates step.   | :heavy_check_mark:  |

### Docker Configuration

|Criteria   |Specifications   |   |
|---|---|---|
|Dockerfile is complete  |TThe Dockerfile should create a working directory, install the necessary dependencies, expose port 80, and specify that app.py run at container launch.   |  :heavy_check_mark:   |
|Dockerfile passes linting via a Makefile   |The Dockerfile should pass make lint without errors. Circleci build server validates step.   | :heavy_check_mark:  |
|Log output is saved in docker_out.txt   |While running the docker container, call the prediction script, make_predictions.sh; the log output, which includes the output prediction value, should be included in your submission as a text file, docker_out.txt.   | :heavy_check_mark:  |
|run_docker.sh is complete Test   |Build, list, and run steps are completed in run_docker.sh.   | :heavy_check_mark:  |
|Docker image is uploaded to docker via upload_docker.sh   |The built docker image is uploaded to your own personal Docker ID, as indicated by a complete upload_docker.sh.   | :heavy_check_mark:  |

### Kubernetes Configuration

|Criteria   |Specifications   |   |
|---|---|---|
|run_kubernetes.sh is complete   |This script runs a docker image with kubernetes, lists the kubernetes pod(s), and forwards the container port to a host, using kubectl appropriately.   | :heavy_check_mark:  |
|An output prediction is saved in kubernetes_out.txt  |While running on kubernetes, call make_predictions.sh; the terminal output should be included in your submission as a text file, kubernetes_out.txt.   | :heavy_check_mark:  |
