# Obstacle Detection using v-Disparity  
**Master 2 – Autonomous Mobile Systems (M2E3A)**  
Perception – TC2 – G1, Université d'Évry / Université Paris Saclay  
Supervisor: Pr. J-P. Tarel, Université de Gustave Eiffel – Author: Kheir Eddine BELLAHCENE (2023–2024)  

**Full Report:** [Live HTML Report](https://kheiro-bellahcene.github.io/Obstacle-Detection-With-V-Disparity/)  

---

## Overview
This project implements an **obstacle detection pipeline** based on **stereo vision** and **v-disparity analysis**.  
The method estimates the road profile from stereo images, then detects obstacles as deviations from this profile.  

**Main steps:**
1. Compute the disparity map from rectified stereo images.
2. Generate the v-disparity representation.
3. Fit the road profile (`v = a·d + b`) using dominant disparity lines.
4. Identify obstacles based on disparity peaks above the road model.

---

## Conclusion
The v-disparity approach proves to be an effective and relatively simple method for detecting obstacles using stereo vision.  
By modeling the road profile and analyzing deviations in the disparity domain, the system can localize potential hazards without complex 3D reconstruction.  

Its importance lies in transforming a difficult 3D perception problem into a simpler 2D line-detection problem:  
- The road becomes a clear straight line in v-disparity space, making slope estimation easier.  
- Obstacles appear as deviations above this line, enabling robust detection.  
- It is computationally efficient, requiring less processing than full 3D analysis, and adapts to varying road slopes.  

This makes v-disparity highly suitable for real-time perception in autonomous mobile robots and advanced driver-assistance systems.


