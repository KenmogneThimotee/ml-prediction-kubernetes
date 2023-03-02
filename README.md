Circle ci build status : [![KenmogneThimotee](https://circleci.com/gh/KenmogneThimotee/ml-prediction-kubernetes.svg?style=svg)](https://app.circleci.com/pipelines/github/KenmogneThimotee/ml-prediction-kubernetes?branch=master)


## Project Overview

In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API. 

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

---

## Setup the Environment

* Create a virtualenv with Python 3.7 and activate it. Refer to this link for help on specifying the Python version in the virtualenv. 
```bash
python3 -m pip install --user virtualenv
# You should have Python 3.7 available in your host. 
# Check the Python path using `which python3`
# Use a command similar to this one:
python3 -m virtualenv --python=<path-to-Python3.7> .devops
source .devops/bin/activate
```
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl

### File descriptions

-   .circleci/config.yml
    Is the circleci workflow that build, test and lint the project
-   output_txt_files/docker_out.txt
    Is the  log statements of a successfully docker running prediction
-   output_txt_files/kubernetes_out.txt
    Is the  log statements of a successfully kubernetes running prediction
-   app.py
    Is the flask web app that make prediction
-   Dockefile
    Instructions to create the docker image
-   make_predictions.sh
    Bash file that make prediction
-   Makefile
    The makefile that contains instructions to install dependencies, test and lint
-   README.md
    The readme of the project
-   requirements.txt
    The list of all the python package dependencies
-   run_docker.sh
    The bash file that build and run the the project as a docker container
-   run_kubernetes.sh
    The bash file that create a pod and run it in a kubernetes cluster
-   upload_docker.sh
    The bash file that upload the docker image to the docker hub


