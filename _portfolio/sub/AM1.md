---
title: "Topology optimization for LPBF"
permalink: /portfolio/sub/AM1/
---
This research focuses on developing advanced optimization methodologies for manufacturing processes, integrating computational mechanics, thermal-mechanical coupling, and process planning. Our work is structured into several **sub-directions** that collectively aim to enhance manufacturability, reduce residual stresses, and achieve high-precision fabrication.

---

## 1.Research Background

We investigate heat transfer, mechanical response, and residual stress evolution during additive and hybrid manufacturing processes. These studies form the theoretical foundation for developing optimization algorithms and predictive simulation tools.


## 2.LPBF Simulation Solver
### 2.1.Thermal-Elastic-Plastic Solver
Detail coming soon...
### 2.2.Thermal Solver (Overheating Prediction)
Detail coming soon...
### 2.3.Simplified Solver based on Inherent Strain Method 
![Simulation flow chart based on inherited strain method](/images/manufacturing_process/研究1-1.png)  
<p style="margin-top: 5px; font-style: italic; text-align: center;">Simulation flow chart based on inherent strain method.</p>

<div style="display:flex; justify-content:center; gap:10px; margin-top:15px;">
    <img src='/images/manufacturing_process/Picture3.gif' style="width:45%;">
    <img src='/images/manufacturing_process/Picture5.gif' style="width:45%;">
</div>

<p style="margin-top: 5px; font-style: italic; text-align: center;">Simulation process: (left) Fusion process; (right) Cut-off process.</p>

![Comparison with commercial software](/images/manufacturing_process/研究1-3.png)  
<p style="margin-top: 5px; font-style: italic; text-align: center;">Comparison with commercial software shows errors < 5%, demonstrating solver reliability.</p>

[🔗 Related MATLAB Code](https://www.mech.sdu.edu.cn/info/1132/129552.htm)

---

## 3.Design Optimization based on Inherent Strain Method
### 3.1.Residual Stress Constrained Structure Topology optimization
<div style="text-align: center;">
    <img src='/images/manufacturing_process/研究1-4.png' style="width: 90%; margin-top: 10px;">
    <p style="font-style: italic;">Comparison and verification with commercial software results.</p>
</div>

[🔗 Related Paper](https://www.mech.sdu.edu.cn/info/1132/129552.htm)

### 3.2.Scanning Path Optimization for Residual Distortion Reduction

![Integration with CAM](/images/manufacturing_process/研究1-4.png)  
*Coupling optimization results with CAM toolpath planning for practical manufacturing execution.*

[🔗 Related Paper](https://www.mech.sdu.edu.cn/info/1132/129552.htm)

### 3.3.Concurrent Structure and Path Optimization for Residual Distortion Reduction
<div style="text-align: center; margin-top: 10px;">
    <a href="https://www.mech.sdu.edu.cn/info/1132/129552.htm" target="_blank">Related Paper Link 1</a><br>
    <a href="https://www.mech.sdu.edu.cn/info/1132/129552.htm" target="_blank">Related Paper Link 2</a>
</div>
[🔗 Related Paper](https://www.mech.sdu.edu.cn/info/1132/129552.htm)

### 3.4.Support Structure Design for LPBF
<div style="text-align: center;">
    <img src='/images/manufacturing_process/研究1-6.png' style="width: 90%; margin-top: 10px;">
    <p style="font-style: italic;">Comparison and verification with commercial software results.</p>
</div>
[🔗 Related Paper](https://www.mech.sdu.edu.cn/info/1132/129552.htm)