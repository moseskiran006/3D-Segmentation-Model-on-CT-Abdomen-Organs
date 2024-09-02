# 3D-Segmentation-Model-on-CT-Abdomen-Organs

## Overview

This project focuses on building a 3D segmentation model for abdominal organs, specifically targeting the Liver, Right Kidney, Left Kidney, and Spleen from CT scan images. The model was trained to accurately segment these organs using volumetric data in .nii format. The primary goal is to achieve high segmentation accuracy, measured by the Dice score.

## Ready to Use Google Colab
[`Google Colab File`](https://colab.research.google.com/drive/1lMohor2mtlDMzlA94n_Q4ZKknYCUaDea?usp=sharing)

## Download the dataset linked below
Please ensure you have sufficient storage and bandwidth for the download.
['dataset'](https://drive.google.com/drive/folders/1Or1uBDcfhFPJCA3ASdWVfmVheSDZuiZl?usp=sharing)

## follow the google colab module 

# Model Architecture

The model used in this project is based on the VNet architecture, which is a fully convolutional network specifically designed for 3D medical image segmentation. Key features of the model include:

3D Convolutions: Capture spatial context in all three dimensions.
Residual Blocks: Enable deeper network structures while maintaining efficiency.
Skip Connections: Preserve fine-grained details in segmentation.

## Training Process

The training process involved the following steps:

Data Preprocessing:

Normalization of CT scan intensity values.
Resampling to a consistent voxel size.
Data augmentation techniques such as rotation, scaling, and flipping.

![labeled organs](https://github.com/moseskiran006/3D-Segmentation-Model-on-CT-Abdomen-Organs/blob/main/Screenshot%202024-08-31%20232600.png)

## Training:

Loss Function: Dice Loss
Optimizer: Adam
Learning Rate: 1e-4 with a scheduler
Epochs: 100
Validation:

During training, a validation set was used to monitor model performance and prevent overfitting.

# Validation and Inference

The validation and inference processes were designed to evaluate the model's performance:

Metrics:

Dice Score: The primary metric used to evaluate the segmentation accuracy for each organ.
Hausdorff Distance: Additional metric to measure the similarity between predicted and ground truth boundaries.
Inference:

The trained model was used to predict segmentation masks for unseen CT scans. These predictions were then visualized and compared against ground truth masks.

![3D Visualization](https://github.com/moseskiran006/3D-Segmentation-Model-on-CT-Abdomen-Organs/blob/main/Screenshot%202024-09-02%20224815.png)




