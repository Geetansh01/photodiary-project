# Photo Diary Project

## Overview

The **Photo Diary Project** is an automation pipeline designed to align facial images over time. By utilizing deep learning techniques, the project eliminates the tedious task of manual alignment, producing a time-lapse video of aligned faces.

## Motivation

The project aims to develop a pipeline for aligning facial images.

In a previous attempt, a custom dataset of approximately 75 manually annotated images was used, but it was found to be insufficient for achieving satisfactory results.&#x20;

The next iteration relies exclusively on the **BioID dataset** for improved results.

## Features

- **Deep Learning Model**: To predict eye coordinates (left eye row, left eye column, right eye row, right eye column in pixels).
- **Alignment Pipeline**: To Align facial images by applying geometric transformations based on predicted eye coordinates.
- Video Generation: To produce a time-lapse type video of aligned facial images.

## Dataset

- **BioID Dataset**: A publicly available dataset comprising facial images annotated with key facial landmarks, including left and right eye positions.

## Model Details

- **Architecture**: ConvNeXt-Tiny
- **Training**:
  - Fine-tuned on the BioID dataset to predict four coordinates corresponding to the eye positions.
  - Achieved a validation loss of **0.003 MSE** on the dataset.
- **Preprocessing**: Images are normalized for consistent input.

## Technologies Used

- **Programming Language**: Python
- **Libraries**: PyTorch, FastAI, OpenCV

## Results

- **Aligned Video**: A time-lapse type video showcasing aligned facial images over time. ([Video]([https://youtu.be/Y_oVdfEavt4]))



  ## Future Improvements
- Extend the pipeline to handle rotation and scaling for more robust alignment.
- Explore transfer learning with larger pre-trained models for improved accuracy.

