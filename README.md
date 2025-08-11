# 🚗🔍 Obstacle Detection using **V-Disparity**
**Master 2 – Autonomous Mobile Systems (M2E3A)**  
Perception – TC2 – G1  
Université d'Évry / Université Paris-Saclay  
**Supervisor:** Pr. J-P. Tarel (Université Gustave Eiffel)  
**Author:** Kheir Eddine BELLAHCENE — 2023–2024  

📄 **Full Interactive Report:** [🔗 Live HTML Report](https://kheiro-bellahcene.github.io/Obstacle-Detection-With-V-Disparity/)  

---

## 🌟 Overview
This project presents a **stereo vision–based pipeline** for **real-time obstacle detection**, leveraging the **v-disparity representation** to simplify road scene analysis.  
The core idea: instead of directly handling noisy 3D reconstructions, we transform the problem into a **2D line detection** task in the disparity domain — cleaner, faster, and more robust.

---

### **Workflow**
1. **Stereo Disparity Computation**  
   Generate a disparity map from rectified stereo image pairs.
2. **V-Disparity Map Construction**  
   Convert the disparity map into a vertical profile histogram (v-disparity).
3. **Road Profile Estimation**  
   Detect and fit the dominant line corresponding to the road:  
   `v = a·d + b`
4. **Obstacle Detection**  
   Identify disparity peaks **above** the fitted road profile — these are potential hazards.

---

## 📌 Key Insight
> The road appears as a **straight, dominant line** in v-disparity space,  
> while **obstacles stand out** as deviations above it.

---

## ✅ Advantages of V-Disparity Approach
- **Simplicity:** Turns complex 3D geometry into a 2D line-fitting problem.
- **Robustness:** Works under varying slopes and road shapes.
- **Efficiency:** Less computationally heavy than full 3D reconstruction.
- **Real-Time Potential:** Well-suited for **autonomous mobile robots** and **ADAS** systems.

---

## 🏁 Conclusion
The v-disparity method offers an **elegant compromise** between accuracy and speed in road obstacle detection.  
By abstracting away unnecessary complexity, it allows autonomous systems to **focus on actionable hazards** without overloading processing resources — a key requirement for safety-critical applications.



