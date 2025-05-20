---
layout: project
title: "Pokémon Object Detection with Mask R-CNN"
description: "Implementing transfer learning with a pre-trained Mask R-CNN model to detect custom objects like Pikachu in images."
image: assets/images/mask-01.png
tech_stack: "Python, TensorFlow, Mask R-CNN, OpenCV"
category: "Computer Vision"
project_type: "Personal Project"
status: "Completed"
date: 2023-11-15
---

## Project Overview

This personal project, developed during my time at the Université Paris-Est Créteil, explores the application of Mask R-CNN for custom object detection. I implemented transfer learning techniques with a pre-trained Mask R-CNN model (originally trained on the COCO dataset) to detect and segment custom objects - specifically Pikachu from Pokémon - in images. This work demonstrates how deep learning can be adapted to specialized detection tasks without requiring extensive training data.

## Implementation Details

I utilized a pre-trained Mask R-CNN architecture as the foundation and fine-tuned it to recognize Pikachu from various angles and contexts. The project involved:

- Adapting the Mask R-CNN architecture originally pre-trained on COCO dataset
- Creating a custom dataset with labeled Pikachu images
- Implementing transfer learning to recognize this character not present in the original dataset
- Optimizing detection parameters for higher accuracy

[*Mask R-CNN detection result showing bounding boxes and segmentation*]
![Mask R-CNN Detection Bounding boxes](/assets/images/mask-01.png)
![Mask R-CNN Detection Segmentation](/assets/images/mask-02.png)


## Parameter Optimization

A significant part of this project involved experimenting with various parameters to improve detection performance:

### 1. IoU Thresholds for Region Proposal Network (RPN)
- Adjusted upper threshold (positive samples) and lower threshold (negative samples)
- Found optimal performance with lower bound at 0.3 and upper bound at 0.7
- Values between thresholds were ignored during training to improve robustness

### 2. ROI Box Head Architecture
- Experimented with varying numbers of convolution filters (optimal: 4 filters)
- Tested different configurations of fully connected layers (settled on 2 FC layers)
- Balanced complexity against potential overfitting

### 3. Non-Maximum Suppression (NMS) Optimization
- Fine-tuned pre-NMS and post-NMS proposal numbers
- Default values: 4000 pre-NMS proposals, 1000 post-NMS proposals during training
- NMS suppresses overlapping bounding boxes to retain only the highest confidence detections


## Technical Challenges

The project presented several interesting challenges:

- **Annotation Efficiency**: Creating efficient workflows for annotating custom objects
- **Transfer Learning Optimization**: Finding the right balance between frozen and trainable layers
- **Hyperparameter Tuning**: Systematic experimentation with detection parameters
- **Small Dataset Handling**: Implementing data augmentation to maximize learning from limited examples

## Results and Insights

The fine-tuned model successfully detected Pikachu in various contexts with high precision. Key findings include:

- Transfer learning significantly reduced the amount of training data needed
- Parameter tuning had substantial impact on detection quality
- NMS threshold values greatly influenced the final detection results
- The model generalized well to different poses and backgrounds of the character

## Technologies Used

- **Python** for implementation
- **TensorFlow** and **Keras** for deep learning framework
- **Mask R-CNN** architecture for instance segmentation
- **OpenCV** for image processing and visualization
- **Data augmentation** techniques for training set expansion

## Future Directions

- Expand detection to multiple Pokémon characters
- Implement real-time detection capabilities
- Explore instance segmentation for more detailed character analysis
- Compare performance against newer architectures like YOLO and EfficientDet