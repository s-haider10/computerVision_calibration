# TP1: Camera Calibration

Welcome to my submission for the Camera Calibration practical! In this notebook, I'll be guiding you through the process of camera calibration using both linear and non-linear methods. Below, you'll find detailed explanations, code snippets, and visualizations to help you understand each step of the process.

## Introduction

This practical serves as an introduction to camera calibration. We'll be using a set of corresponding points in both the image and 3D space to calibrate the camera. The goal is to extract intrinsic and extrinsic parameters of the camera, such as the calibration matrix, rotation matrix, and translation vector.

## Getting Started

Before we dive into the code, make sure you have the necessary dependencies installed. You'll need `numpy`, `matplotlib`, and `scipy` to run this notebook.

```bash
pip install numpy matplotlib scipy
```

You can execute the notebook using Jupyter. If you don't have Jupyter installed, you can refer to [this link](http://jupyter.org/install.html) for installation instructions.

## Step-by-Step Guide

### 1. Linear Method

#### 1.a) Building Matrix A
We start by building the matrix `A` that defines the camera calibration equation. This matrix will be used in the linear method to compute the camera matrix.

#### 1.b) Singular Value Decomposition (SVD)
Performing SVD on matrix `A` helps us compute the camera matrix `P`. We'll check the coherence of SVD and ensure that one of the singular values is close to zero.

#### 1.c) Computing Camera Matrix `P`
Using the SVD results, we compute the camera matrix `P` which represents the projection of 3D points onto the 2D image plane.

#### 1.d) Projection Error
We'll write a function to compute the projection error, which measures the mean squared error between the projected 3D points and the actual 2D points.

#### 1.e) Visualization
Visualizing the projected 3D points and the 2D points on the same figure helps us understand the calibration results.

### 2. Camera Parameters

#### 2.a) Extracting Camera Parameters
We'll extract the intrinsic and extrinsic parameters of the camera, including the calibration matrix, rotation matrix, and translation vector, using the results from the linear method.

#### 2.b) Testing with Different Choices of `eps`
Testing the function with different choices of `eps` allows us to determine which option makes more sense based on the object's position relative to the camera.

## Conclusion

By following this notebook, you'll gain a better understanding of camera calibration techniques and how to extract important camera parameters using linear methods. Feel free to experiment with different datasets and parameters to further explore this topic.

Happy coding! 📷✨
