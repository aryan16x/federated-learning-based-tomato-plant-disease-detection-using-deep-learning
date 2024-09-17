# Federated Learning Based Tomato Plant Disease Detection Using Deep Learning: A Collaborative Approach

## Project Overview
This project implements a federated learning approach for tomato plant disease detection using deep learning techniques. It aims to provide a collaborative and privacy-preserving method for identifying diseases in tomato plants across distributed datasets.

## Team Details

### Mentor
- Prof. Aruguma Arun R.

### Team Members
1. Vansh Bennalakar [21BCT0277]
2. Aryan Gadhiya [21BCT0208]

## Features
- Federated learning implementation for distributed data processing
- Deep learning models for accurate disease detection
- Privacy-preserving approach to handle sensitive agricultural data

## Data Transformation Process

The data transformation process balances the dataset between two clients while ensuring data diversity. Here are the key steps:

1. **Dataset Selection**: The process focuses on three categories of tomato plant diseases:
   - Tomato Late Blight
   - Late Mold
   - Bacterial Spot

2. **Client Data Balancing**:
   - **Client 1 (Downsampling)**: If Client 1 has more images than the target size, random images are removed to reach the target.
   - **Client 2 (Upsampling)**: If Client 2 has fewer images than the target size, new images are generated through augmentation.

3. **Image Augmentation** (for Client 2 upsampling):
   - Random rotations and flips
   - Gaussian noise, blur, and median blur
   - Motion blur, optical distortion, and piecewise affine transformations
   - Shift, scale, and rotate transformations
   - CLAHE, sharpening, embossing, and brightness/contrast adjustments
   - Hue, saturation, and value modifications

4. **Output**: Balanced datasets for both clients, with Client 2 having augmented images to match Client 1's quantity.

This process ensures that both clients have similar amounts of data while introducing variety in Client 2's dataset through augmentation.
