---
title: "Topology Optimization for LPBF"
permalink: /portfolio/sub/AM1/
---

<style>
.portfolio-detail {
  max-width: 1040px;
  margin: 0 auto;
}

.portfolio-detail .research-text3 {
  color: #3e4650;
  line-height: 1.75;
  text-align: justify;
}

.portfolio-detail .status-note {
  margin: 8px 0 20px;
  padding: 10px 14px;
  border-left: 3px solid #9aa6b2;
  color: #65707b;
  background: #f7f9fa;
  font-style: italic;
}

.portfolio-detail .card-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 22px;
}

.portfolio-detail .card {
  padding: 18px;
  border: 1px solid #dfe4e8;
  border-radius: 12px;
  background: #fff;
  box-shadow: 0 4px 14px rgba(31, 43, 55, 0.06);
}

.portfolio-detail .card h3,
.portfolio-detail .card h4 {
  margin-top: 8px;
}

.portfolio-detail img {
  display: block;
  max-width: 100%;
  height: auto;
  margin-right: auto;
  margin-left: auto;
  object-fit: contain;
}

.portfolio-detail .figure {
  margin: 18px auto 24px;
  text-align: center;
}

.portfolio-detail .figure-row {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 12px;
  margin-top: 15px;
}

.portfolio-detail .figure-caption {
  margin: 8px auto 0;
  color: #67717c;
  font-size: 13px;
  font-style: italic;
  line-height: 1.5;
  text-align: center;
}

.portfolio-detail .project-link {
  display: inline-block;
  margin: 4px 0 24px;
  padding: 9px 15px;
  border-radius: 999px;
  color: #fff;
  background: #1769aa;
  font-weight: 700;
  text-decoration: none;
}

.portfolio-detail .project-link:hover {
  background: #125586;
  text-decoration: none;
}

@media screen and (max-width: 640px) {
  .portfolio-detail .card-grid {
    grid-template-columns: 1fr;
  }

  .portfolio-detail .figure-row {
    flex-direction: column;
  }

  .portfolio-detail .figure-row img {
    width: 100% !important;
  }
}
</style>

<div class="portfolio-detail">
<div class="research-text3">
This research focuses on developing advanced optimization methodologies for manufacturing processes, integrating computational mechanics, thermal-mechanical coupling, and process planning. Our work is structured into several **sub-directions** that collectively aim to enhance manufacturability, reduce residual stresses, and achieve high-precision fabrication.
</div>

## 1. Research Background
<div class="research-text3">
We investigate heat transfer, mechanical response, and residual stress evolution during additive manufacturing processes. These studies form the theoretical foundation for developing optimization algorithms and predictive simulation tools.
</div>

## 2. LPBF Simulation Solver
### 2.1. Thermal-Elastic-Plastic Solver
<p class="status-note">Detailed documentation is being prepared.</p>
### 2.2. Thermal Solver (Overheating Prediction)
<p class="status-note">Detailed documentation is being prepared.</p>
### 2.3. Simplified Solver Based on the Inherent Strain Method 
#### 2.3.1. Solver Framework
![Simulation flow chart based on inherent strain method](/images/manufacturing_process/研究1-1.png)  
<p class="figure-caption">Simulation flow chart based on inherent strain method.</p>

#### 2.3.2. Simulation Process
<div class="figure-row">
    <img src='/images/manufacturing_process/Picture3.gif' style="width:45%;">
    <img src='/images/manufacturing_process/Picture5.gif' style="width:45%;">
</div>
<p class="figure-caption">Simulation process: (left) Fusion process; (right) Cut-off process.</p>

#### 2.3.3. Results Validation
![Comparison with commercial software](/images/manufacturing_process/研究1-3.png)  
<p class="figure-caption">Comparison with commercial software shows errors below 5%, demonstrating solver reliability.</p>
[🔗 Related MATLAB Code](https://www.mech.sdu.edu.cn/info/1132/129552.htm)


## 3. Design Optimization Based on the Inherent Strain Method

<div class="card-grid">

  <!-- 3.1 -->
  <div class="card">
    <h3>3.1. Residual Stress Constrained Structure Topology Optimization</h3>
    <div style="text-align: center;">
      <img src='/images/manufacturing_process/研究1-4.png' style="width: 100%; margin-top: 10px;">
      <p class="figure-caption">Residual-stress-constrained topology optimization results.</p>
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
      <p class="figure-caption">The illustration of scanning island.</p>
    </div>

<h4>3.2.2. Modeling</h4>
    <div style="text-align: center;">
      <img src='/images/manufacturing_process/研究1-7.png' style="width: 100%; margin-top: 10px;">
      <p class="figure-caption">The anisotropic property of inherent strain and modeling.</p>
    </div>

<h4>3.2.3. Optimization Framework</h4>
<div style="text-align: center;">
      <img src='/images/manufacturing_process/研究1-8.png' style="width: 100%; margin-top: 10px;">
      <p class="figure-caption">Optimization framework for island scanning-pattern design.</p>
    </div>
    
<div style="text-align: center;">
      <img src='/images/manufacturing_process/GIF55.gif' style="width: 90%; margin-top: 10px;">
      <p class="figure-caption">Evolution of the optimized island scanning pattern.</p>
    </div>

<div style="text-align: center;">
      <img src='/images/manufacturing_process/GIF66.gif' style="width: 80%; margin-top: 10px;">
      <p class="figure-caption">Residual-distortion response during the optimization process.</p>
    </div>

<h4>3.2.4. Related Publication</h4>
    <div class="research-text3" style="text-align: justify;">
      <p>
        [1] <strong>Xu, S.</strong>, Huang, J., Liu, J., Ma, Y., & Liu, J. (2022). 
        An Island Scanning Path-Pattern Optimization for Metal Additive Manufacturing Based on Inherent Strain Method. 
        <em>Computer-Aided Design and Applications</em>, 19(4), 812-824. 
        <a href="https://cad-journal.net/files/vol_19/Vol19No4.html" target="_blank" rel="noopener noreferrer">[Paper]</a>
      </p>
      <p>
        [2] <strong>Xu, S.</strong>, Huang, J., Liu, J., & Ma, Y. (2021). 
        Island Scanning Path-Pattern Optimization for Residual Distortion Control in Metal Additive Manufacturing.
        <em>Proceedings of CAD’21</em>, Barcelona, Spain, July 5–7, 2021, pp. 66–72. 
        <a href="https://faculty.sustech.edu.cn/wp-content/uploads/2021/10/2022031717455991.pdf" target="_blank" rel="noopener noreferrer">[Paper]</a>
      </p>
    </div>
  </div>

  <!-- 3.3 -->
  <div class="card">
    <h3>3.3. Concurrent Structure and Path Optimization for Residual Distortion Reduction</h3>

<h4>3.3.1. Optimization Framework</h4>
    <div style="text-align: center;">
      <img src='/images/manufacturing_process/研究1-9.png' style="width: 100%; margin-top: 10px;">
      <p class="figure-caption">Concurrent optimization framework for structure and scanning pattern.</p>
    </div>

<h4>3.3.2. Optimization Results</h4>
    <div style="text-align: center;">
      <img src='/images/manufacturing_process/研究1-10.png' style="width: 100%; margin-top: 10px;">
      <p class="figure-caption">Optimized structure, scanning pattern, and residual-distortion results.</p>
    </div>

<h4>3.3.3. Related Publication</h4>
    <div class="research-text3">
      <p>
        <strong>Xu, S.</strong>, Liu, J., Li, X., & Ma, Y. (2023). Concurrent Island scanning pattern and large-scale topology optimization method for laser powder bed fusion processed parts. <em>Finite Elements in Analysis and Design</em>, 225, 104018. <a href="https://www.sciencedirect.com/science/article/pii/S0168874X23001117" target="_blank" rel="noopener noreferrer">[Paper]</a> 
      </p>
    </div>
  </div>

  <!-- 3.4 -->
  <div class="card">
    <h3>3.4. Support Structure Design for LPBF</h3>
    <h4>3.4.1. Optimization results</h4>
    <div style="text-align: center;">
      <img src='/images/manufacturing_process/研究1-6.png' style="width: 90%; margin-top: 10px;">
      <p class="figure-caption">Support-structure optimization results considering residual distortion.</p>
    </div>

<h4>3.4.2. Related Publication</h4>
<div class="research-text3">
  <p>
    <strong>Xu, S.</strong>, Liu, J., Sun, Y., Li, X., & Ma, Y. (2024). 
    Support structure topology optimization considering the residual distortion for laser powder bed fusion metal additive manufacturing. 
    <em>Structural and Multidisciplinary Optimization</em>, 67(10), 1–20. 
    <a href="https://scholar.google.com/citations?view_op=view_citation&hl=zh-CN&user=lC1RMK0AAAAJ&sortby=pubdate&citation_for_view=lC1RMK0AAAAJ:YsMSGLbcyi4C" target="_blank" rel="noopener noreferrer">[Paper]</a>
  </p>
</div>

</div>

</div>

</div>
