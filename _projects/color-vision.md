---
layout: project
title: "Color Vision Deficiency Assistant"
description: "Mobile application helping people with color blindness perceive colors more accurately through customized image recoloration."
image: assets/images/cv-ui01.png
tech_stack: "React Native, Python Flask, OpenCV"
category: "Assistive Technology"
project_type: "Professional Project"
status: "Completed"
date: 2023-09-15
---

## Project Overview

This assistive technology project, developed during my internship at the University of Granada, addresses the challenges faced by people with Congenital Color Vision Deficiency (CVD). Affecting approximately 8% of Caucasian males and 0.5% of females, color blindness limits color discrimination abilities in various contexts.

The application serves dual purposes: helping color blind individuals perceive colors more accurately through customized image recoloration, and allowing people with normal vision to experience what color blindness is like through simulation.

## Technical Implementation

### System Architecture

The application uses a client-server architecture:
- **Frontend**: React Native with Expo framework for cross-platform compatibility
- **Backend**: Python Flask server handling complex image processing algorithms
- **Image Processing Pipeline**: OpenCV-based transformation between RGB and LMS color spaces

<!-- IMAGE: Architecture diagram showing the flow from user input to processed image output -->
[Architecture diagram showing the flow from user input to processed image output]
![architecture](/assets/images/color-vision-flow.png)


### Key Features

1. **Personalized CVD Calibration**: Interactive color grouping experiment to determine the type and severity of color vision deficiency
2. **Image Recoloration**: Advanced algorithms to transform images for better perception by CVD individuals
3. **Simulation Mode**: Allows non-CVD users to experience how images appear to people with different types of color blindness
4. **Camera Integration**: Ability to process both existing and newly captured images

## Color Science Application

The project implements sophisticated color science principles:

- **Color Space Transformation**: Converting between RGB and LMS (Long, Medium, Short wavelength cone response) color spaces
- **Kotera Simulation**: Implementation of the Kotera algorithm for recoloring images to enhance perception for CVD individuals
- **Calibration Testing**: Utilizing Digital NCS (Natural Color System) samples for precise CVD type determination


## Results and Outcomes
[Image: User interface of app designed by Iye Szin]
![User Interface of App 1](/assets/images/cv-ui01.png)
![User Interface of App2](/assets/images/cv-ui02.png)

The application successfully recolors images to enhance color differentiation for users with various types of color blindness. Testing with sample images demonstrated significant improvement in distinguishing previously confusing colors:


[Image: Grid of test results showing original and recolored images]
![Test results](/assets/images/color-vision.png)

## Technical Challenges

Several technical challenges were addressed during development:

1. **Cross-platform Color Management**: Implementing consistent color representation across different mobile devices
2. **Algorithm Translation**: Converting complex MATLAB color transformation algorithms to Python
3. **Real-time Processing**: Optimizing image processing for acceptable performance on mobile devices
4. **Personalization**: Creating adaptive systems that respond to individual variations in color perception

## Future Development

While the core functionality was successfully implemented, several enhancements remain for future development:

1. **Device Screen Calibration**: Enhanced color calibration for more accurate representation
2. **Expanded Testing Framework**: Additional color perception experiments for more precise CVD classification
3. **Real-time Video Processing**: Extending image recoloration to live video streams
4. **Accessibility Improvements**: Further UI refinements for users with additional visual needs

## Technologies Used

- **Frontend**: React Native, Expo
- **Backend**: Python, Flask
- **Image Processing**: OpenCV, NumPy
- **Color Science**: LMS color space transformation, Kotera algorithm
- **Development Environment**: Visual Studio Code, Android Studio Emulator