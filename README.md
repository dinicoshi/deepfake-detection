# DeepFake Detection

The goal of this project is to identify deepfake manipulations in videos and distinguish them from real
videos.

# Introduction

This project leverages a video-based dataset to build models that analyse and predict whether a given video is deepfake-manipulated or real. It uses two diffrent models - a CNN/RNN approach and a CNN/Transformers approach, to build the prediction models.

# Project Structure

```
project
├── preprocessing.ipynb
├── README.md
├── xception_convlstm2d.ipynb
└── xception_transformers.ipynb
```

# Key Components

- **preprocessing.ipynb**: Handles frame-level feature extraction using Xception and reshapes video features into uniform sequences.
- **xception_convlstm2d.ipynb:** Main notebook implementing the ConvLSTM2D model for temporal analysis of deepfake videos, including model training and evaluation.
- **xception_transformers.ipynb**: Implements a Transformer-based model for sequence classification of video features, using positional embeddings and attention layers.

# Models Used

The project implements two deep learning models to predict the presence of deepfake manipulation and compare performance:

- XceptionNet with ConvLSTM2D model
- XceptionNet with Transformers

You can download the trained dataset from: https://drive.google.com/drive/folders/1eqQV0FmYc37JbHDgoIZlc3tyQ-UaerUk?usp=drive_link

# Results

| Model | AUC Score |
| --- | --- |
| ConvLSTM2D | 0.7778 |
| Transformer | 0.8441 |