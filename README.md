# 🤖 Linear Multivariable Control of an Autonomous Underwater Vehicle (AUV)

> Design and simulation of an **LQR-based optimal control system** for the vertical plane motion of an **Autonomous Underwater Vehicle (AUV)**, improving stability and precision over traditional PID control.

---

## 🌊 Overview

This project was completed as part of the *Linear Multivariable Control* course  
in the **Erasmus Mundus MIR Programme** at Université de Toulon.  

The goal was to design an **optimal control law (LQR)** to regulate an AUV’s vertical motion —  
maintaining depth and pitch stability under hydrodynamic disturbances.  

A MATLAB-based control model was developed to:
- Identify **hydrodynamic parameters** through data fitting,
- Linearize the nonlinear vehicle model around equilibrium,
- Implement and tune an **LQR controller**, and
- Validate its performance through simulation.

---

## 📂 Repository Structure

| Path | Description |
|------|--------------|
| **Codes/ECA_ControlCommand/** | MATLAB simulation files for AUV identification, linearization, and control command generation |
| **Linear_Multivariable_Control_Report.pdf** | Full technical report (15 pages) detailing model derivation, LQR design, and simulation results |
| **README.md** | Project documentation and summary (this file) |

---

## ⚙️ Project Workflow

| Step | Description |
|------|-------------|
| **1. Parameter Identification** | Estimated missing hydrodynamic parameters (e.g., damping coefficients) using least squares (`lsqr`) and constrained optimization (`fmincon`) from recorded mission data. |
| **2. Linearization** | Derived equilibrium points and computed linear state-space matrices **A** and **B** for the vertical plane. |
| **3. LQR Control Design** | Designed an optimal **Linear Quadratic Regulator (LQR)** controller minimizing the cost function `J = ∫(xᵀQx + uᵀRu)dt`. |
| **4. Tuning Q & R** | Tuned Q and R matrices to balance state tracking accuracy and control effort. |
| **5. Simulation & Validation** | Tested depth and pitch control in MATLAB/Simulink to assess steady-state error, overshoot, and response time. |

---

## 🧠 Key Results

| Metric | Achieved Value | Requirement |
|---------|----------------|-------------|
| Depth overshoot | **1.4 m** | < 2 m |
| Steady-state error | **≈ 0** | ≈ 0 |
| Pitch oscillation | **Low / Stable** | Minimal |
| Response time | **≈ 125 s to 10 m depth** | Acceptable |

---

## 📊 Control Insight

- The **LQR controller** achieved precise and smooth depth control with minimal oscillations.  
- **Pitch angle** and **angular velocity** converged steadily to zero after reaching target depth.  
- **Actuator commands** (rear helms & motor RPM) remained stable, ensuring low energy consumption.  
- The approach significantly outperformed traditional PID control in stability and efficiency.  

---

## 🧩 Tools & Techniques

- MATLAB / Simulink  
- Linearization & system identification  
- LQR design (`lqr`, `lqrd`, `fmincon`, `lsqr`)  
- Time-domain analysis (overshoot, settling time, steady-state error)  

---

## 👩‍🔬 Team

**Hyejoo Kwon**, Shahid Ahamed Hasib, Faith Oluwasegun Mustapha,  
Mohamed Magdy Atta, Ahmed Borchani  

📍 Erasmus Mundus Master’s in *Marine & Maritime Intelligent Robotics (MIR)*  
🧑‍🏫 Instructor: *Aurélien Dhaisne*  
📅 Submitted: October 2025  

🔗 [GitHub Repository](https://github.com/S1194789/Linear_Multivariable_Control)
