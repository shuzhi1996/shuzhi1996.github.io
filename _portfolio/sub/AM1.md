---
title: "Topology optimization for LPBF"
permalink: /portfolio/sub/AM1/
---

<style>
.card-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 20px;
}
.card {
  padding-top: 0px;   /* 控制卡片内容距离顶部 */
  border: 1px solid #ddd;
  border-radius: 10px;
  padding: 15px;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.05);
  text-align: center;
}
.card img {
  width: 100%;
  border-radius: 8px;
}
.card h3 {
  margin-top: 5px;  /* 减小标题和卡片顶部的距离 */
  padding-top: 0;   /* 去掉额外内边距 */
}

.card h4 {
  font-size: 16px;
  margin-top: 10px;
}
.card a {
  display: inline-block;
  margin-top: 6px;
  font-weight: bold;
  text-decoration: none;
  color: #0073e6;
}
.card a:hover {
  color: #0056a3;
}
</style>
<div class="research-text3">
This research focuses on developing advanced optimization methodologies for manufacturing processes, integrating computational mechanics, thermal-mechanical coupling, and process planning. Our work is structured into several **sub-directions** that collectively aim to enhance manufacturability, reduce residual stresses, and achieve high-precision fabrication.
</div>

## 1.Research Background
<div class="research-text3">
We investigate heat transfer, mechanical response, and residual stress evolution during additive manufacturing processes. These studies form the theoretical foundation for developing optimization algorithms and predictive simulation tools.
</div>

## 2.LPBF Simulation Solver
### 2.1.Thermal-Elastic-Plastic Solver
Detail coming soon...
### 2.2.Thermal Solver (Overheating Prediction)
Detail coming soon...
### 2.3.Simplified Solver based on Inherent Strain Method 
#### 2.3.1.Solver framework
![Simulation flow chart based on inherited strain method](/images/manufacturing_process/研究1-1.png)  
<p style="margin-top: 5px; font-style: italic; text-align: center;">Simulation flow chart based on inherent strain method.</p>

#### 2.3.2.Simulation process
<div style="display:flex; justify-content:center; gap:10px; margin-top:15px;">
    <img src='/images/manufacturing_process/Picture3.gif' style="width:45%;">
    <img src='/images/manufacturing_process/Picture5.gif' style="width:45%;">
</div>
<p style="margin-top: 5px; font-style: italic; text-align: center;">Simulation process: (left) Fusion process; (right) Cut-off process.</p>

#### 2.3.3.Results validation
![Comparison with commercial software](/images/manufacturing_process/研究1-3.png)  
<p style="margin-top: 5px; font-style: italic; text-align: center;">Comparison with commercial software shows errors < 5%, demonstrating solver reliability.</p>
[🔗 Related MATLAB Code](https://www.mech.sdu.edu.cn/info/1132/129552.htm)


## 3. Design Optimization based on Inherent Strain Method

<div class="card-grid">

  <!-- 3.1 -->
  <div class="card">
    <h3>3.1. Residual Stress Constrained Structure Topology Optimization</h3>
    <div style="text-align: center;">
      <img src='/images/manufacturing_process/研究1-4.png' style="width: 100%; margin-top: 10px;">
      <p style="font-style: italic; text-align: center;">Comparison and verification with commercial software results.</p>
    </div>
  </div>

  <!-- 3.2 -->
  <div class="card">
    <h3>3.2. Scanning Path Optimization for Residual Distortion Reduction</h3>
    <div class="research-text3">
      <p>
        Since it is quite easy to set or adjust such island scanning path of the laser for the metal AM machine,
        a systemic metal AM-oriented island-type scanning pattern optimization method is therefore proposed in this work.
      </p>
    </div>

<h4>3.2.1. Problem Definition</h4>
    <div style="text-align: center;">
      <div style="display: flex; gap: 0px;">
        <img src='/images/manufacturing_process/图片5.gif' style="width: 30%; margin-top: 10px;">
        <img src='/images/manufacturing_process/图片1.jpg' style="width: 70%; margin-top: 10px;">
      </div>
      <p style="font-style: italic; text-align: center;">The illustration of scanning island.</p>
    </div>

<h4>3.2.2. Modeling</h4>
    <div style="text-align: center;">
      <img src='/images/manufacturing_process/研究1-7.png' style="width: 100%; margin-top: 10px;">
      <p style="font-style: italic; text-align: center;">The anisotropic property of inherent strain and modeling.</p>
    </div>

    <h4>3.2.3. Optimization Framework</h4>
    <div style="text-align: center;">
      <img src='/images/manufacturing_process/研究1-8.png' style="width: 100%; margin-top: 10px;">
      <p style="font-style: italic; text-align: center;">Design framework and case study.</p>
    </div>

<h4>3.2.4. Related Publication</h4>
    <div class="research-text3" style="text-align: justify;">
      <p>
        [1] <strong>Xu, S.</strong>, Huang, J., Liu, J., Ma, Y., & Liu, J. (2022). 
        An Island Scanning Path-Pattern Optimization for Metal Additive Manufacturing Based on Inherent Strain Method. 
        <em>Computer-Aided Design and Applications</em>, 19(4), 812-824. 
        <a href="https://cad-journal.net/files/vol_19/Vol19No4.html" target="_blank">[Paper]</a>
      </p>
      <p>
        [2] <strong>Xu, S.</strong>, Huang, J., Liu, J., & Ma, Y. (2021). 
        Island Scanning Path-Patten Optimization for Residual Distortion Control in Metal Additive Manufacturing.
        <em>Proceedings of CAD’21</em>, Barcelona, Spain, July 5–7, 2021, pp. 66–72. 
        <a href="https://faculty.sustech.edu.cn/wp-content/uploads/2021/10/2022031717455991.pdf" target="_blank">[Paper]</a>
      </p>
    </div>
  </div>

  <!-- 3.3 -->
  <div class="card">
    <h3>3.3. Concurrent Structure and Path Optimization for Residual Distortion Reduction</h3>

<h4>3.3.1. Optimization Framework</h4>
    <div style="text-align: center;">
      <img src='/images/manufacturing_process/研究1-9.png' style="width: 100%; margin-top: 10px;">
      <p style="font-style: italic; text-align: center;">Design framework and case study.</p>
    </div>

<h4>3.3.2. Optimization Results</h4>
    <div style="text-align: center;">
      <img src='/images/manufacturing_process/研究1-10.png' style="width: 100%; margin-top: 10px;">
      <p style="font-style: italic; text-align: center;">Design framework and case study.</p>
    </div>

<h4>3.3.3. Related Publication</h4>
    <div class="research-text3">
      <p>
        <strong>Xu, S.</strong>, Liu, J., Li, X., & Ma, Y. (2023). Concurrent Island scanning pattern and large-scale topology optimization method for laser powder bed fusion processed parts. <em>Finite Elements in Analysis and Design</em>, 225, 104018.<a href="https://www.sciencedirect.com/science/article/pii/S0168874X23001117" target="_blank">[Paper]</a> 
      </p>
    </div>
  </div>

  <!-- 3.4 -->
  <div class="card">
    <h3>3.4. Support Structure Design for LPBF</h3>
    <h4>3.4.1. Optimization results</h4>
    <div style="text-align: center;">
      <img src='/images/manufacturing_process/研究1-6.png' style="width: 90%; margin-top: 10px;">
      <p style="font-style: italic;">Comparison and verification with commercial software results.</p>
    </div>
    <p><a href="https://www.mech.sdu.edu.cn/info/1132/129552.htm" target="_blank">🔗 Related Paper</a></p>
  </div>

<h4>3.4.2. Related Publication</h4>
<div class="research-text3">
  <p>
    <strong>Xu, S.</strong>, Liu, J., Sun, Y., Li, X., & Ma, Y. (2024). 
    Support structure topology optimization considering the residual distortion for laser powder bed fusion metal additive manufacturing. 
    <em>Structural and Multidisciplinary Optimization</em>, 67(10), 1–20. 
    <a href="https://scholar.google.com/citations?view_op=view_citation&hl=zh-CN&user=lC1RMK0AAAAJ&sortby=pubdate&citation_for_view=lC1RMK0AAAAJ:YsMSGLbcyi4C" target="_blank">[Paper]</a>
  </p>
</div>

</div>
