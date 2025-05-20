---
layout: project
title: "Sign Language Robot: ROS2-based Human-Robot Interaction Framework"
description: "Designed and implemented a comprehensive system enabling robots to recognize and produce sign language, enhancing accessibility for deaf and hard of hearing individuals."
image: assets/images/sl-model.png
tech_stack: "Python, ROS2, TensorFlow, Computer Vision, MediaPipe, Robotics"
category: "Assistive Technology"
project_type: "Professional Project"
status: "Completed"
date: 2023-05-15
---

## Project Overview

This project addresses the critical need for innovative accessibility solutions for the deaf and hard of hearing community. Working at the University of Granada, I developed a comprehensive ROS2-based framework enabling human-robot interaction through sign language, creating a bidirectional communication system that can both recognize human signs and produce sign language gestures with a robotic hand.

The system aims to answer a fundamental research question: How can the integration of sign language into human-robot interaction enhance accessibility and inclusivity for individuals who are deaf or hard of hearing?

![Training and inference phase](/assets/images/sl-system.png)


## Technical Implementation

### System Architecture

The framework consists of three primary components working in seamless integration:

1. **Sign Language Recognition**: Computer vision system using deep learning to detect and classify hand gestures
2. **ROS2 Communication Framework**: Message-passing architecture connecting all system components
3. **Robotic Hand Control**: Precise motor control to form accurate sign language gestures

The complete ROS2 architecture includes:
- Camera node for gesture capture
- Inference node for sign recognition
- Chat agent for processing recognized signs
- Position controller for robotic hand articulation
- Service interfaces for system integration

![ROS2 Architecture Diagram](/assets/images/sl-ros.png)
*ROS2 architecture showing communication flow between system components*

### Sign Recognition

I implemented two approaches to sign language recognition:

1. **Static Sign Recognition**: CNN-based model trained on the Sign Language MNIST dataset achieving 100% top-1 accuracy on test data
   - Preprocessing pipeline for image normalization
   - Custom model architecture with convolutional layers, batch normalization, and dropout
   - Full confusion matrix validation

2. **Dynamic Sign Recognition**: Advanced system using 543 body landmarks (face, hands, pose) to recognize word-level signs
   - Transformer and GRU architectures for temporal sequence modeling
   - Landmark reduction and frame interpolation for efficient processing
   - Achieved 76.98% accuracy on the public dataset leaderboard

![Sign Recognition Results](/assets/images/sl-setup.gif)

### Robotic Hand Control

I developed a complete control system for the robotic hand:

- Created a user-friendly GUI for trajectory control and testing
- Implemented precise motor control for 8 actuators managing 19 degrees of freedom
- Designed a trajectory database mapping recognized signs to motor positions
- Achieved system latency of only ±0.003 seconds


## Challenges and Limitations

While the recognition models achieved high accuracy in controlled testing environments, the real-world implementation on the robotic system revealed several important challenges:

1. **Hardware Constraints**: The physical limitations of the robotic hand significantly impacted sign reproduction:
   - Ring and little fingers shared the same control mechanism, limiting independent movement
   - Inability to cross fingers for certain signs
   - Limited finger span compared to human hands
   - Constraints in achieving precise thumb positions required for some signs

2. **Recognition-to-Execution Gap**: The high accuracy of the recognition algorithms in testing environments did not directly translate to successful execution in the full robotic system due to:
   - Environmental variations (lighting, background, etc.)
   - Differences between training data and real-world inputs
   - Real-time processing requirements

3. **ROS2 Integration Challenges**: 
   - ROS2 incompatibility with Gazebo simulation limited testing options
   - Only the left robotic hand was fully supported in the ROS2 implementation

![Unsuccessful Trajectories](/assets/images/sl-limitation.png)
*Examples of signs that proved challenging for the robotic hand due to physical limitations*

These challenges provided valuable insights into the gap between algorithmic performance and practical robotics implementation - an important learning outcome of the project.

## Impact and Applications

Despite the implementation challenges, this project demonstrated:
- The viability of computer vision approaches for sign language recognition
- The potential for ROS2-based frameworks in assistive technology
- Clear identification of hardware requirements for effective sign language robots

The research highlighted both the promise and current limitations of robotic sign language interpretation, providing a foundation for future improvements in the field.

## Future Directions

Based on the challenges encountered, future development should focus on:
- Improved robotic hand designs with greater dexterity and independent finger control
- Bridging the gap between algorithmic and real-world performance through domain adaptation
- Enhancing the system with facial expression capabilities for complete grammatical context
- Development of hardware specifically designed for sign language reproduction

## Technologies Used

- **Computer Vision**: MediaPipe, OpenCV
- **Machine Learning**: TensorFlow, CNN, Transformer, GRU
- **Robotics**: ROS2, Motor Control
- **Development**: Python, C++

## Key Learnings

This project provided valuable insights into:
- The complexities of translating computer vision models to practical robotic applications
- Hardware design requirements for effective sign language reproduction
- The importance of considering physical constraints when designing assistive technology
- Effective implementation of ROS2 for complex human-robot interaction systems