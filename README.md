# ImageClassifier

Inspiration and branched from the tutorial, [A Beginner’s Tutorial on Building an AI Image Classifier using PyTorch](https://towardsdatascience.com/a-beginners-tutorial-on-building-an-ai-image-classifier-using-pytorch-6f85cb69cba7).

Table of contents
=================

<!--ts-->
   * [Introduction](#Introduction)
   * [Features](#Features)
   * [Python Libraries](#Python-Libraries)
<!--te-->

# Introduction

Image classification refers to a process in computer vision that can classify an image according to its visual content. For example, an image classification algorithm may be designed to tell if an image contains a human figure or not. The goal of this project was to train a model to identify images. To add humor and sponteneity, the model would identify whether an image displayed was one of Shrek or one of puppies.

The original inspiration behind this project was to train AI to classify images for [this project](https://github.com/bingxuanying/GrainStorageProject2019) without spending the time to build a model for scratch. Hence, transfer learning became very important here. Transfer learning in training models makes use of the knowledge gained while solving one problem and applying it to a different but related problem. In this project, the [densenet161](https://pytorch.org/hub/pytorch_vision_densenet/) was taken, and retrained to identify Shrek and puppies.

# Features

The model, when fed a testing set images guesses whether an image in that of Shrek or Donkey.

```
# Process Image
image = process_image("root/image1234.jpg")
# Give image to model to predict output
top_prob, top_class = predict(image, model)
# Show the image
show_image(image)
# Print the results
print("The model is ", top_prob*100, "% certain that the image has a predicted class of ", top_class  )
```

# Python Libraries

## PyTorch

[PyTorch](https://pytorch.org/tutorials/beginner/blitz/tensor_tutorial.html) is a Python-based scientific computing package targeted at two sets of audiences:

* A replacement for NumPy to use the power of GPUs
* A deep learning research platform that provides maximum flexibility and speed

## Matplotlib

[Matplotlib](https://matplotlib.org/) is a comprehensive library for creating static, animated, and interactive visualizations in Python.

## NumPy

[NumPy](https://numpy.org/) is the fundamental package for scientific computing with Python. It contains among other things:

* A powerful N-dimensional array object
* Sophisticated (broadcasting) functions
* Tools for integrating C/C++ and Fortran code
* Useful linear algebra, Fourier transform, and random number capabilities

## Python Imaging Library

The Python Imaging Library adds image processing capabilities to a Python interpreter.

This library provides extensive file format support, an efficient internal representation, and fairly powerful image processing capabilities.

The core image library is designed for fast access to data stored in a few basic pixel formats. It should provide a solid foundation for a general image processing tool.
