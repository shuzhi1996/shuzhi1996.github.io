---
title: "方向三：Geometry Driven Topology Optimization"
excerpt: "We develop methods that bridge topology optimization and CAD modeling, enabling the direct generation of editable, history-based geometric features. With Autodesk Inventor, optimized designs are reconstructed as fully parametric models, allowing seamless design refinement and rapid downstream modifications.<br/><br/><img src='/images/封面.png'>"
collection: portfolio
---

<style>

/* =========================================================
   页面整体区域
   ========================================================= */

.research-page {
  width: 100%;
  margin: 0 auto;
  box-sizing: border-box;
}


/* =========================================================
   章节标题
   ========================================================= */

.research-page .section-title {
  margin: 0 0 20px 0;

  font-size: 26px;
  font-weight: 700;
  line-height: 1.4;

  color: #222222;
}


/* =========================================================
   章节介绍文字
   ========================================================= */

.research-page .research-text {
  margin: 0 0 28px 0;
}

.research-page .research-text p {
  margin: 0;

  font-size: 16px;
  line-height: 1.8;
  text-align: justify;

  color: #444444;
}


/* =========================================================
   卡片网格
   ========================================================= */

.research-page .card-grid {
  display: grid;

  /*
   * 页面较宽时自动排列成多列；
   * 页面较窄时自动排列成单列。
   */
  grid-template-columns: repeat(
    auto-fit,
    minmax(min(100%, 360px), 1fr)
  );

  gap: 26px;

  width: 100%;
  margin: 0 0 45px 0;
}


/* =========================================================
   单个卡片
   ========================================================= */

.research-page .card {
  display: flex;
  flex-direction: column;

  width: 100%;
  min-width: 0;

  overflow: hidden;
  box-sizing: border-box;

  border: 1px solid #dddddd;
  border-radius: 12px;

  background-color: #ffffff;

  box-shadow: 0 3px 10px rgba(0, 0, 0, 0.07);

  transition:
    transform 0.25s ease,
    box-shadow 0.25s ease,
    border-color 0.25s ease;
}


/* 鼠标移动到卡片上时 */

.research-page .card:hover {
  transform: translateY(-4px);

  border-color: #cccccc;

  box-shadow: 0 9px 24px rgba(0, 0, 0, 0.12);
}


/* =========================================================
   卡片图片区域
   高度根据图片自身比例自动调整
   ========================================================= */

.research-page .card-image {
  display: block;

  width: 100%;
  box-sizing: border-box;

  /*
   * 图片和卡片边缘之间的留白。
   * 不需要留白时可以改成 padding: 0;
   */
  padding: 18px;

  overflow: hidden;

  border-bottom: 1px solid #eeeeee;

  /*
   * 图片区域背景设置为纯白色
   */
  background-color: #ffffff;
}


/* 卡片图片 */

.research-page .card-image img {
  display: block;

  width: 100%;
  height: auto;
  max-width: 100%;

  margin: 0 auto;

  /*
   * 保持图片原始宽高比例；
   * 不裁剪图片。
   */
  object-fit: contain;
  object-position: center;

  border: none;
  border-radius: 0;

  background-color: #ffffff;

  box-shadow: none;
}


/* =========================================================
   卡片文字区域
   ========================================================= */

.research-page .card-content {
  display: flex;
  flex: 1;
  flex-direction: column;

  padding: 21px 24px 24px 24px;

  text-align: left;

  background-color: #ffffff;
}


/* =========================================================
   卡片标题
   ========================================================= */

.research-page .card-title {
  margin: 0 0 12px 0;

  font-size: 19px;
  font-weight: 700;
  line-height: 1.5;

  color: #222222;
}


/* =========================================================
   卡片说明文字
   ========================================================= */

.research-page .card-description {
  flex: 1;

  margin: 0 0 20px 0;

  font-size: 15px;
  line-height: 1.75;

  color: #555555;
}


/* =========================================================
   Project Page 按钮
   ========================================================= */

.research-page .card-button {
  display: inline-flex;
  align-items: center;
  align-self: flex-start;
  justify-content: center;

  margin-top: auto;
  padding: 9px 17px;

  border: 1px solid #0073e6;
  border-radius: 6px;

  background-color: #0073e6;
  color: #ffffff !important;

  font-size: 14px;
  font-weight: 600;
  line-height: 1.4;

  text-decoration: none !important;

  transition:
    background-color 0.2s ease,
    border-color 0.2s ease,
    transform 0.2s ease;
}


/* 按钮悬停效果 */

.research-page .card-button:hover {
  transform: translateY(-1px);

  border-color: #005bb5;
  background-color: #005bb5;

  color: #ffffff !important;
  text-decoration: none !important;
}


/* =========================================================
   平板和手机端适配
   ========================================================= */

@media screen and (max-width: 768px) {

  .research-page .section-title {
    font-size: 22px;
  }

  .research-page .research-text p {
    font-size: 15px;
  }

  .research-page .card-grid {
    grid-template-columns: 1fr;
    gap: 20px;
  }

  .research-page .card-image {
    padding: 12px;
    background-color: #ffffff;
  }

  .research-page .card-content {
    padding: 18px 19px 21px 19px;
  }

  .research-page .card-title {
    font-size: 17px;
  }

  .research-page .card-description {
    font-size: 14px;
    line-height: 1.7;
  }
}

</style>


<div class="research-page">

  <!-- =====================================================
       第一部分：标题和介绍
       ===================================================== -->

  <h2 class="section-title">
    1. Geometry-Driven Topology Optimization Using B-Spline Geometric Primitives
  </h2>


  <div class="research-text">

    <p>
      We develop geometry-driven topology optimization methods based on
      B-spline geometric primitives. The optimized structures are represented
      using editable centerlines and sectional profiles, enabling direct
      reconstruction as parameterized and manufacturing-compatible CAD models.
    </p>

  </div>


  <!-- =====================================================
       项目卡片网格
       ===================================================== -->

  <div class="card-grid">


    <!-- ===================================================
         Card 1
         =================================================== -->

    <article class="card">

      <!-- 卡片图片区域 -->

      <div class="card-image">

        <img
          src="{{ '/images/CAD/图片9.svg' | relative_url }}"
          alt="Thermal-fluid topology optimization based on B-spline geometry">

      </div>


      <!-- 卡片文字区域 -->

      <div class="card-content">

        <h3 class="card-title">
          1.1. Thermal-Fluid Topology Optimization
        </h3>

        <p class="card-description">
          Geometry-driven topology optimization for thermal-fluid problems
          based on editable, parameterized, and manufacturing-compatible
          B-spline loft features.
        </p>

        <a
          class="card-button"
          href="{{ '/project/BsplineTO/bspline1.html' | relative_url }}">

          Project Page&nbsp;→

        </a>

      </div>

    </article>


    <!-- ===================================================
         Card 2 示例

         需要添加第二个卡片时，可以取消下面的注释，
         然后修改图片、标题、介绍和链接。
         ===================================================

    <article class="card">

      <div class="card-image">

        <img
          src="{{ '/images/CAD/your-image.png' | relative_url }}"
          alt="Project image description">

      </div>

      <div class="card-content">

        <h3 class="card-title">
          1.2. Project Title
        </h3>

        <p class="card-description">
          Add the project description here.
        </p>

        <a
          class="card-button"
          href="{{ '/project/your-project.html' | relative_url }}">

          Project Page&nbsp;→

        </a>

      </div>

    </article>

    -->


  </div>

</div>