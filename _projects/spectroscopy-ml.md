---
layout: project
title: "Data Science in Spectroscopy"
description: "Interdisciplinary research combining computational methods and petrology. Developing machine learning models for spectroscopic data analysis."
image:
tech_stack: "Python, TensorFlow, Spectral Libraries (RRUFF)"
category: "Interdisciplinary Research"
status: "In Progress"
project_type: "Professional Project"
date: 2025-03-31
github_link: "https://github.com/iyeszin/rocks_evaluation"
---

## Project Overview

This ongoing research project sits at the intersection of geology, computer science, and materials analysis. I'm developing machine learning approaches to analyze spectroscopic data from mineral samples, with applications in both academic research and industrial materials characterization.

## Research Context
This project was conducted as part of my doctoral research at Montanuniversität Leoben, in collaboration with the Chair of Waste Processing Technology and Waste Management, and Chair of Subsurface Engineering. I conceptualized and led the implementation of machine learning approaches for spectroscopic data analysis.

## Key Contributions
- Built a system that automatically identifies minerals from their light signatures (Raman spectroscopy), eliminating hours of manual analysis
- Created a smart weighing system that determines rock types based on which minerals are present and in what amounts
- Designed machine learning models that work hand-in-hand with geologists' knowledge rather than replacing it
- Developed an end-to-end automated pipeline that connects the dots from raw spectral data to final rock classification, making complex analysis accessible to non-specialists

## Current Focus
- Developing and validating our classification algorithm using synthetic mineral compositions
- Building interpretable models that provide insights on compositional information
- Planning the transition from synthetic to real-world rock samples

## Data Challenges and Approach
### Why This Data Is Unique
Unlike many machine learning projects that use easily accessible data (like images or text), spectroscopic mineral data presents special challenges:

- **Expensive Equipment**: Raman spectroscopy requires specialized instruments costing hundreds of thousands of dollars
- **Expert Operation**: Only trained technicians can properly prepare samples and operate the equipment
- **Limited Access**: Few facilities have both the equipment and expertise to generate quality data
- **Time-Intensive**: Each sample analysis can take hours to complete properly

### Our Solution
To overcome these barriers, we've:
- Started with synthetic mineral compositions to prove our algorithm works
- Created a framework that maximizes learning from limited data
- Designed our pipeline to be adaptable when real-world samples become available
- Focused on methods that incorporate geological domain knowledge to compensate for data limitations

### Future Direction
Our next phase aims to built pilot plant to collect data and to validate our approach on real rock samples.