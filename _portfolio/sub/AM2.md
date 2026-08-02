---
title: "Topology Optimization for Multi-Axis Additive Manufacturing"
permalink: /portfolio/sub/AM2/
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

<a class="project-link" href="{{ '/project/MAM/mam.html' | relative_url }}">Full Project Page&nbsp;→</a>

## 1. Research Background

<div class="figure">
  <img src="{{ '/images/multi-axis AM/GIF4.gif' | relative_url }}" alt="Self-support limitations in conventional additive manufacturing">
</div>

<div class="research-text3">
  <p>
    Conventional additive manufacturing is limited by material self-support
    requirements. Designers must either compromise structural performance to
    obtain self-supporting geometry or add supports that can be difficult to
    remove. Multi-axis additive manufacturing offers a promising way to reduce
    these restrictions.
  </p>
</div>

<div class="figure">
  <img src="{{ '/images/multi-axis AM/GIF5.gif' | relative_url }}" alt="Geometric motion and collision constraints in multi-axis additive manufacturing">
</div>

<div class="research-text3">
  <p>
    Multi-axis motion does not make every structure automatically manufacturable.
    Platform rotation and deposition-path planning introduce collision risks, while
    local overhang angles still constrain feasible printing. The structure and
    process therefore need to be designed concurrently.
  </p>
</div>

## 2. Concurrent Design Framework

<div class="figure">
  <img src="{{ '/images/multi-axis AM/图片5.png' | relative_url }}" alt="Concurrent optimization framework for structure and curved-layer slicing">
</div>

<div class="research-text3">
  <p>
    The framework simultaneously optimizes structural topology and curved-layer
    slicing. It maintains feasible forming angles, improves layer quality, and
    avoids potential collisions during fabrication.
  </p>
</div>

## 3. Post-Processing

<div class="figure">
  <img src="{{ '/images/multi-axis AM/GIF2.gif' | relative_url }}" alt="Curved-layer slicing process" style="width: 48%;">
  <p class="figure-caption">Curved-layer slicing process.</p>
</div>

<div class="research-text3">
  <p>
    An in-house post-processing algorithm converts the optimized design and slicing
    result into G-code that can be executed by a multi-axis additive manufacturing
    system.
  </p>
</div>

<div class="figure">
  <img src="{{ '/images/multi-axis AM/GIF3.gif' | relative_url }}" alt="Validation of the generated multi-axis printing path">
  <p class="figure-caption">
    Validation of the generated printing path. Dynamic motion optimization is
    outside the present scope.
  </p>
</div>

## 4. Fabrication Process

<div class="figure">
  <img src="{{ '/images/multi-axis AM/GIF1.gif' | relative_url }}" alt="Multi-axis additive manufacturing process" style="width: 48%;">
  <p class="figure-caption">Fabrication process.</p>
</div>

## 5. Related Publication

<div class="research-text3">
  <p>
    [1] <strong>Xu, S.</strong>, Liu, J., He, D., Tang, K., &amp; Yaji, K. (2025).
    <a href="https://www.sciencedirect.com/science/article/pii/S0045782525001136" target="_blank" rel="noopener noreferrer">
      Self-support structure topology optimization for multi-axis additive manufacturing incorporated with curved layer slicing.
    </a>
    <em>Computer Methods in Applied Mechanics and Engineering</em>, 438, 117841.
  </p>
</div>

## 6. Cooperation

<div class="figure">
  <img src="{{ '/images/multi-axis AM/图片2.png' | relative_url }}" alt="Experimental cooperation for multi-axis additive manufacturing">
</div>

</div>
