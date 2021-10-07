# Spatial Transformer Networks in PyTorch

## References

DeepMind paper: https://arxiv.org/abs/1506.02025

PyTorch tutorial: https://pytorch.org/tutorials/intermediate/spatial_transformer_tutorial.html

## Description

Spatial transformer networks are a generalization of differentiable attention to any spatial transformation. Spatial transformer networks (STN for short) allow a neural network to learn how to perform spatial transformations on the input image in order to enhance the geometric invariance of the model. For example, it can crop a region of interest, scale and correct the orientation of an image. It can be a useful mechanism because CNNs are not invariant to rotation and scale and more general affine transformations. 

Goals of the project:

1. Investigate if using CoordConv layers instead of standard Conv will help to improve the performance.
2. Compare the performance of the new model in evaluation metric and motivate the choice of metrics.

## Installation

- [Docker](https://docs.docker.com/get-docker)

## Usage

Set up the environment building a docker image from the Dockerfile:
```sh
docker build -t pytorch-stn . 
```

Train the STN:
```sh
 docker run pytorch-stn --stage='train' --epochs=1
```

Test the STN:
```sh
 docker run pytorch-stn --stage='test'
```

## 1. Using CoordConv layers

![alt text](https://github.com/vicsesi/Pytorch-STN/blob/main/imgs/layers.png?raw=true)

## 2. Performance Comparison 

