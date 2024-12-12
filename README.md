# Very Low Exposure Simulator

## Overview
The Very Low Exposure Simulator uses Monte Carlo simulation to generate and analyze very low-exposure images. This project is designed to investigate how extremely low light levels affect image resolution and signal-to-noise ratio (SNR), offering a computational framework for studying photon distribution in imaging under limited lighting conditions.

## Features
- **Bulk Processing**: Handles bulk processing of input luminance distribution images.
- **Monte Carlo Simulation**: Simulates low-light conditions using stochastic photon distribution.
- **Image Preprocessing**: Normalizes images and adjusts parameters for low-light simulation.
- **Customizable Parameters**: Supports adjustable photon counts and image resolutions for simulation.
- **YOLOv9 Integration**: Implements YOLOv9 for object detection on simulated low-exposure images.

## Motivation
- To simulate low-exposure images.
- To understand the effect of low exposure on image resolution and SNR.
- To explore the capabilities of neural networks under low-light conditions.

## Objectives
- Generate low-exposure images from luminance distributions using Monte Carlo simulation.
- Estimate the minimal illumination required for object detection in autonomous driving scenarios.
- Analyze the effect of photon distribution on resolution and SNR.

## Methodology
### 1. Define Parameters
- **Array Size**: Set the initial image size (e.g., 64x64) and update based on actual dimensions.
- **Photon Count**: Adjust the number of photons for simulation accuracy and computation time.

### 2. Image Preprocessing
- **Normalize Image**: Convert pixel intensity values to a [0, 1] range.
- **Adjust Array Size**: Match array size to image dimensions.

### 3. Monte Carlo Simulation
- **Initialize Simulation**: Create a zero-initialized array for the simulated image.
- **Simulation Loop**:
  - Randomly sample pixel coordinates.
  - Retrieve pixel intensity as photon detection probability.
  - Simulate photon detection using random number generation.

### 4. Postprocessing and Visualization
- Generate low-exposure images with noise reflecting low-light conditions.
- Display original and simulated images side-by-side.

### 5. Results Analysis
- Compare resolution and SNR under varying photon counts and lighting conditions.
- Use F-Stop, ISO, and exposure time settings to analyze the effect on quanta per pixel.

## Results
The simulator provides detailed results based on:
- Photon counts ranging from 10,000 to 100,000,000.
- Impact of ISO settings and exposure times on SNR and resolution.
- Visualization of low-light image characteristics.

## Requirements
- Python (latest version)
- Required libraries:
  - NumPy
  - OpenCV
  - Matplotlib
  - YOLOv5 (pre-trained weights for object detection)




