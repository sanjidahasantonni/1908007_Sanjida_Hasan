Spectrogram Denoising Using U-Net
Overview
This repository contains the implementation of a U-Net-based deep learning model for spectrogram denoising. The U-Net architecture, originally designed for biomedical image segmentation, is adapted here for improving spectrogram quality by reducing noise while preserving key audio features.

Dataset
The dataset used for this project is a high-resolution 3D electron microscopy dataset representing a 5x5x5µm section from the CA1 hippocampus region of the brain. The dataset corresponds to a 1065x2048x1536 volume, with a voxel resolution of 5x5x5nm. It is provided as multipage TIF files compatible with Fiji.

📌 Dataset Link: EPFL CVLab Electron Microscopy Dataset

U-Net Architecture
The U-Net model follows an encoder-decoder structure:

Encoder: Extracts features through convolutional layers and max-pooling operations.
Decoder: Restores spatial details using upsampling layers and skip connections.
Skip Connections: Help retain spatial information by directly connecting encoder layers to corresponding decoder layers.
Implementation Details
The model is built using TensorFlow and Keras, with core components including convolution blocks, encoder blocks, and decoder blocks.
Data Augmentation techniques are applied to improve model generalization.
Training Performance: Achieves ~98% accuracy and an IoU score of 71 on a small dataset of 12 images.
Includes options for modifying the number of encoder and decoder blocks to experiment with architecture variations.
Results
The trained U-Net model effectively reduces noise in spectrograms while preserving the structural details. Users can modify hyperparameters and network depth to explore different trade-offs between denoising performance and computational efficiency.
