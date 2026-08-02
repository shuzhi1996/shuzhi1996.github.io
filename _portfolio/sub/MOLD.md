---
title: "Geometry-Driven Cooling-Channel Design for Molding"
permalink: /portfolio/sub/MOLD/
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

<a class="project-link" href="{{ '/project/BsplineTO/bspline1.html' | relative_url }}">Full Project Page&nbsp;→</a>

<div class="research-text3">
  <p><strong>Shuzhi Xu</strong>, Kentaro Yaji</p>
</div>

## 1. Research Background

<div class="research-text3">
  <p>
    Conformal cooling channels can improve thermal management in molding, but
    conventional topology-optimization results are difficult to transfer directly
    into editable CAD geometry. This work uses explicit B-spline channel primitives
    so that geometry, analysis, and reconstruction share the same design variables.
  </p>
</div>

## 2. Geometry-Driven Design Framework

<div class="figure">
  <img src="{{ '/project/BsplineTO/images/图片1.svg' | relative_url }}" alt="Geometry-driven B-spline cooling-channel optimization framework">
  <p class="figure-caption">
    B-spline centerlines and sectional profiles provide a differentiable,
    geometry-controlled representation of the cooling channels.
  </p>
</div>

## 3. CAD Reconstruction

<div class="figure">
  <img src="{{ '/project/BsplineTO/images/图片10.svg' | relative_url }}" alt="CAD reconstruction of optimized cooling channels">
  <p class="figure-caption">
    Optimized design variables are reconstructed as editable lofted channel
    features inside the molding component.
  </p>
</div>

## 4. Representative Results

<div class="figure">
  <img src="{{ '/project/BsplineTO/images/图片13.svg' | relative_url }}" alt="Optimized molding cooling channels under manufacturability constraints">
  <p class="figure-caption">
    Representative cooling-channel configurations obtained with geometric and
    manufacturability constraints.
  </p>
</div>

</div>
