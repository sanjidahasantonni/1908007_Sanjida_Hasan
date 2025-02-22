# Electron Microscopy Image Segmentation Using U-Net:
## Overview
This repository implements a U-Net-based deep learning model for 3D electron microscopy (EM) image segmentation. The U-Net architecture, originally designed for biomedical image analysis, is utilized here to segment high-resolution brain tissue images, helping to distinguish cellular structures with precision.

## Dataset
The dataset used in this project is a high-resolution 3D electron microscopy dataset representing a 5x5x5µm section from the CA1 hippocampus region of the brain. It consists of a 1065x2048x1536 volume with a voxel resolution of 5x5x5nm. The dataset is provided as multipage TIF files, compatible with Fiji for visualization and preprocessing.

## Dataset Link: EPFL CVLab Electron Microscopy Dataset (https://www.epfl.ch/labs/cvlab/data/data-em/)

## U-Net Architecture
The U-Net model follows an encoder-decoder structure specifically designed for precise image segmentation:

Encoder: Extracts hierarchical features using convolutional layers and max pooling.
Decoder: Restores spatial details using upsampling layers and concatenation with encoder features (skip connections).
Skip Connections: Help retain fine-grained spatial details by directly linking encoder and decoder layers.
Implementation Details
The model is built using TensorFlow and Keras, structured with convolution blocks, encoder blocks, and decoder blocks.
Data Augmentation is applied to improve model generalization for segmenting fine cellular structures.
Training Performance: Achieves ~98% accuracy and an IoU score of 71 on a small dataset of 12 images.
The model can be customized by modifying the number of encoder and decoder blocks to test different configurations.
## Results
The trained U-Net model effectively segments microscopic cellular structures, preserving fine details and improving segmentation accuracy. The approach can be extended to various biomedical and EM imaging tasks.
