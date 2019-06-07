# Tensorflow2.0a-python3.6
Dockerfile with tensorflow 2.0a, cuda 10.0 and python 3.6 intended as a base image for machine learning.

Simple image based on the cuda10.0-devl image.
Contrary to the official tensorflow/tensorflow:2.0.0a0-gpu-py3 image comes with python 3.6 to support features such as f-strings.

Them image installs python 3.6 and pip and apt-tools to ease extensability.
Dependencies in the requirements.txt are beeing installed.

## From Dockerhub:
```
pull patientzero/tensorflow2.0a-gpu-py3.6
```

## Build:
```
cd Docker
docker build -t tensorflow2.0a-gpu-py3.6 .
```
