# GRUTrajectoryPredictor: GRU-Based UAV Trajectory Prediction

## Overview
GRUTrajectoryPredictor is a comprehensive repository for predicting UAV trajectories using Gated Recurrent Unit (GRU) neural networks. This repository is organized into three main directories: `Models`, `Notebooks`, and `Images`, each serving a specific purpose in the workflow of training, testing, and visualizing GRU models for UAV trajectory prediction.

![GRU Model Flowchart](images/GRU_arch.png)

## Directory Structure

### 1. Models
This directory contains GRU models trained on different datasets and with varying model complexities. The models are organized into four subdirectories:

- **GRU_With_Mix_Dataset_MaxNorm**: Contains GRU models trained on a mixed dataset with Max Normalization.
- **GRU_With_Mix_Dataset_WhitingNorm**: Houses models trained on a mixed dataset with Whiting Normalization.
- **GRU_With_Simulation_Dataset_MaxNorm**: Includes models trained on a simulation dataset with Max Normalization.
- **GRU_With_Simulation_Dataset_WhitingNorm**: Contains models trained on a simulation dataset with Whiting Normalization.

Each of these subdirectories includes trained GRU models for different levels of model complexity: 64, 128, 256 hidden dimensions, and 2, 3, 5 layers respectively, predicting both position and velocity trajectories.

### 2. Notebooks
The `Notebooks` directory contains two key Python scripts:
- `train.py`: Script for training the GRU models on the respective datasets.
- `test.py`: Utilized for testing the models, requiring the class `TrajectoryPredictor(torch.nn.Module)` to run the model path files located in the `Models` directory.

## Usage
To use the models for trajectory prediction:
1. Train the model using `train.py` in the `Notebooks` directory.
2. Test the trained models using `test.py`, ensuring the `TrajectoryPredictor` class is correctly implemented.


