# The GPU capable builds (Python, NodeJS, C++, etc) depend on the same CUDA runtime as upstream TensorFlow.
# Currently with TensorFlow 1.13 it depends on CUDA 10.0 and CuDNN v7.5.
FROM nvidia/cuda:10.0-devel

RUN apt-get update \
  && apt-get install -y apt-utils \
  && apt-get install -y git locales

RUN apt-get install -y python3.6
RUN apt-get install -y python3-pip
RUN link /usr/bin/python3.6 /usr/local/bin/python

RUN pip3 install --upgrade pip

RUN locale-gen en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US:en
ENV LC_ALL en_US.UTF-8

RUN mkdir -p /tmp
WORKDIR /tmp

ADD requirements.txt /tmp

RUN pip3 install --upgrade --no-cache -r requirements.txt
