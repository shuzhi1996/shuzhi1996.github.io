---
title: "方向三：Geometry Driven Topology Optimization"
excerpt: "We develop methods that bridge topology optimization and CAD modeling, enabling the direct generation of editable, history-based geometric features. With Autodesk Inventor, optimized designs are reconstructed as fully parametric models, allowing seamless design refinement and rapid downstream modifications.<br/><br/><img src='/images/封面.png'>"
collection: portfolio
---

<style>

/* =========================================================
   研究卡片整体布局：固定为一列
   ========================================================= */

.card-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 24px;
  margin: 24px 0 45px 0;
  width: 100%;
}


/* =========================================================
   单个卡片
   ========================================================= */

.card {
  width: 100%;
  box-sizing: border-box;
  overflow: hidden;

  border: 1px solid #dddddd;
  border-radius: 12px;
  background-color: #ffffff;

  box-shadow: 0 3px 10px rgba(0, 0, 0, 0.07);
  transition:
    transform 0.25s ease,
    box-shadow 0.25s ease;
}


/* 鼠标移动到卡片上时的效果 */

.card:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 22px rgba(0, 0, 0, 0.12);
}


/* =========================================================
   卡片图片
   ========================================================= */

.card img {
  display: block;
  width: 100%;
  max-height: 420px;
  object-fit: cover;
  border-radius: 12px 12px 0 0;
}


/* =========================================================
   卡片文字区域
   ========================================================= */

.card-content {
  padding: 20px 24px 24px 24px;
  text-align: left;
}


/* 卡片标题 */

.card h4 {
  margin: 0 0 12px 0;
  font-size: 18px;
  line-height: 1.5;
}


/* 卡片说明文字 */

.card p {
  margin: 0 0 16px 0;
  font-size: 15px;
  line-height: 1.7;
  color: #555555;
}


/* =========================================================
   Read More 按钮
   ========================================================= */

.card a {
  display: inline-block;
  margin-top: 6px;
  padding: 8px 16px;

  border-radius: 6px;
  background-color: #0073e6;
  color: #ffffff;

  font-size: 14px;
  font-weight: 600;
  text-decoration: none;

  transition: background-color 0.2s ease;
}

.card a:hover {
  background-color: #0056a3;
  color: #ffffff;
}


/* =========================================================
   中英文介绍文字
   ========================================================= */

.research-text2 {
  margin-bottom: 24px;
}

.research-text2 p {
  line-height: 1.8;
  text-align: justify;
}


/* =========================================================
   手机端适配
   ========================================================= */

@media screen and (max-width: 768px) {

  .card-grid {
    grid-template-columns: 1fr;
    gap: 18px;
  }

  .card-content {
    padding: 16px 18px 20px 18px;
  }

  .card h4 {
    font-size: 17px;
  }

  .card img {
    max-height: 300px;
  }
}

</style>


---

## 1. Geometry-driven topology optimization using B-spline geometric primitives

<div class="research-text2">

<p>
We develop methods that bridge topology optimization and CAD modeling, enabling the direct generation of editable, history-based geometric features. With Autodesk Inventor, optimized designs are reconstructed as fully parametric models, allowing seamless design refinement and rapid downstream modifications.

Extrusion-based design is a fundamental modeling strategy in CAD and feature-based solid modeling. A 2D sketch, typically represented by a closed profile, is extruded along a straight or curved path to form a three-dimensional solid. This approach provides intuitive geometric control and is widely used in parametric modeling, design automation, and manufacturing-aware optimization. Extrusion features can represent important structural components such as ribs, walls, and channels, while remaining compatible with downstream manufacturing processes such as CNC machining and additive manufacturing.
</p>
</div>


<div class="card-grid">

  <div class="card">

    <img
      src="{{ '/images/CAD/Extrusion.png' | relative_url }}"
      alt="Thermal-Fluid Topology Optimization">
    <div class="card-content">

      <h4>
        1.1. Thermal-Fluid Topology Optimization
      </h4>

      <p>
        Geometry-driven topology optimization based on editable,
        parameterized, and manufacturing-compatible extrusion features.
      </p>

      <a href="{{ '/project/BsplineTO/bspline1.html' | relative_url }}">
        Read More →
      </a>

    </div>

  </div>
---