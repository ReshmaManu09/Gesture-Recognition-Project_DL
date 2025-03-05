# Gesture Recognition Project

## Overview

This project focuses on developing a smart TV feature that recognizes five different user gestures using a convolutional neural network (CNN). The gestures are designed to control the TV without a remote, enabling actions such as increasing or decreasing volume, jumping forward or backward, and pausing the video.
Each video is a sequence of 30 frames (or images)

## Features

| Gesture       | Action                          |
|---------------|---------------------------------|
| **Thumbs Up** | Increase volume                  |
| **Thumbs Down** | Decrease volume                  |
| **Left Swipe** | Jump backward 10 seconds         |
| **Right Swipe** | Jump forward 10 seconds          |
| **Stop**      | Pause the movie                  |

## Objectives

- **Generator**: The generator should be able to take a batch of videos as input without any error. Steps like cropping, resizing and normalization should be performed successfully.

- **Model**: Develop a model that is able to train without any errors which will be judged on the total number of parameters (as the inference(prediction) time should be less) and the accuracy achieved. As suggested by Snehansu, start training on a small amount of data and then proceed further.

- **Write up**: This should contain the detailed procedure followed in choosing the final model. The write up should start with the reason for choosing the base model, then highlight the reasons and metrics taken into consideration to modify and experiment to arrive at the final model.

## Models Overview

The project experimented with multiple models to optimize accuracy and reduce overfitting. Below is a summary of the key models tested:

| Model  | Key Adjustments                  | Training Accuracy | Validation Accuracy | Validation Loss | Overfitting | Decision                  |
|--------|----------------------------------|-------------------|---------------------|-----------------|-------------|---------------------------|
| **1**  | Baseline                         | 0.7014            | 0.5950              | 0.9794          | Yes         | Fine-tune architecture     |
| **2**  | Added Batch Normalization        | 0.7192            | 0.6233              | 0.8954          | Yes         | Explore regularization     |
| **3**  | Added Dropout                    | 0.7450            | 0.6600              | 0.8123          | Yes         | Reduce parameters          |
| **4**  | Reduced Parameters               | 0.7380            | 0.6433              | 0.8347          | Yes         | Architecture adjustments   |
| **5**  | Architecture Adjustment          | 0.7617            | 0.6833              | 0.7849          | Yes         | Continue refining          |
| **6**  | Further Parameter Reduction      | 0.7315            | 0.2917              | 4.3904          | Severe      | Overfitting prevention     |
| **7**  | Adjusted Dropout Rate            | 0.7247            | 0.2667              | 2.9665          | Severe      | Discarded                  |
| **8**  | Reduced Learning Rate            | 0.7715            | 0.6967              | 0.8190          | Yes         | Continue tuning            |
| **9**  | Further Learning Rate Tuning     | 0.7735            | 0.7000              | 0.8111          | Yes         | Continue refining          |
| **10** | Minor Architectural Tweaks       | 0.7800            | 0.7050              | 0.8049          | Minimal     | Refine further             |
| **11** | Added Data Augmentation          | 0.7841            | 0.7100              | 0.7980          | Minimal     | Retain augmentation        |
| **12** | Final Learning Rate Adjustment   | 0.8000            | 0.7200              | 0.7981          | Minimal     | Strong candidate           |
| **13** | Final Architecture Refinement    | 0.8125            | 0.7400              | 0.7800          | Minimal     | Chosen as final model      |
| **14** | Slight Variations                | 0.8341            | 0.7200              | 0.8896          | Yes         | Discarded                  |
| **15** | Final Experiment                 | 0.8552            | 0.7400              | 0.8231          | Minimal     | Model 13 preferred         |

## Final Model

**Model 13** was selected as the final model due to its balanced performance, with minimal overfitting and optimal validation accuracy and loss.

Developed by Reshma S G

