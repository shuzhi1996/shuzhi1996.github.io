---
title: "方向四：Composite Structure Design"
excerpt: "We develop methods that bridge topology optimization and CAD modeling, enabling the direct generation of editable, history-based geometric features. With Autodesk Inventor, optimized designs are reconstructed as fully parametric models, allowing seamless design refinement and rapid downstream modifications.<br/><br/><img src='/images/封面.png'>"
collection: portfolio
---

<style>

/* =========================================================
   页面基础设置
   ========================================================= */

.research-page {
  --accent-color: #1769aa;
  --accent-dark: #0f4f85;
  --text-color: #252525;
  --secondary-text: #606060;
  --border-color: #e2e5e8;

  width: 100%;
  max-width: 1100px;

  margin: 0 auto;
  box-sizing: border-box;
}


/* =========================================================
   章节
   ========================================================= */

.research-page .research-section {
  margin: 0 0 36px 0;
}


/* 最后一个章节减少底部空白 */

.research-page .research-section:last-child {
  margin-bottom: 16px;
}


/* =========================================================
   章节标题
   ========================================================= */

.research-page .section-title {
  display: flex;
  align-items: center;
  gap: 10px;

  margin: 0 0 14px 0;

  font-size: 24px;
  font-weight: 700;
  line-height: 1.35;

  color: var(--text-color);
}


/* 标题左侧装饰线 */

.research-page .section-title::before {
  content: "";

  flex: 0 0 auto;

  width: 4px;
  height: 25px;

  border-radius: 3px;

  background-color: var(--accent-color);
}


/* =========================================================
   章节介绍文字
   ========================================================= */

.research-page .research-text {
  margin: 0 0 18px 0;
}

.research-page .research-text p {
  margin: 0;

  font-size: 15px;
  line-height: 1.7;
  text-align: justify;

  color: #484848;
}


/* =========================================================
   卡片网格

   默认情况：
   一个 section 中有两个或更多卡片时，固定显示两列
   ========================================================= */

.research-page .card-grid {
  display: grid;

  grid-template-columns: repeat(2, minmax(0, 1fr));

  gap: 18px;

  width: 100%;
  margin: 0;
}


/* =========================================================
   单卡片布局

   当 section 只有一个卡片时：
   使用 class="card-grid single-card"
   ========================================================= */

.research-page .card-grid.single-card {
  grid-template-columns: minmax(0, 680px);
  justify-content: center;
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

  border: 1px solid var(--border-color);
  border-radius: 10px;

  background-color: #ffffff;

  box-shadow:
    0 2px 8px rgba(25, 35, 45, 0.06);

  transition:
    transform 0.22s ease,
    box-shadow 0.22s ease,
    border-color 0.22s ease;
}


/* 卡片悬停效果 */

.research-page .card:hover {
  transform: translateY(-3px);

  border-color: #cbd4dc;

  box-shadow:
    0 7px 18px rgba(25, 35, 45, 0.11);
}


/* =========================================================
   卡片图片区域

   高度根据图片原始比例自动调整
   ========================================================= */

.research-page .card-image {
  display: block;

  width: 100%;
  overflow: hidden;
  box-sizing: border-box;

  padding: 10px;

  border-bottom: 1px solid #eceff1;

  background-color: #ffffff;
}


/* 卡片图片 */

.research-page .card-image img {
  display: block;

  width: 100%;
  height: auto;
  max-width: 100%;

  margin: 0 auto;

  object-fit: contain;
  object-position: center;

  border: none;
  border-radius: 5px;

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

  padding: 15px 17px 17px 17px;

  text-align: left;

  background-color: #ffffff;
}


/* =========================================================
   卡片标题
   ========================================================= */

.research-page .card-title {
  margin: 0 0 9px 0;

  font-size: 16px;
  font-weight: 700;
  line-height: 1.45;

  color: var(--text-color);
}


/* =========================================================
   研究方向标签
   ========================================================= */

.research-page .card-tag {
  display: inline-block;

  margin: 6px 0 0 0;
  padding: 3px 8px;

  border: 1px solid #dbe7f1;
  border-radius: 20px;

  background-color: #f3f8fc;
  color: #4f6f88;

  font-size: 12px;
  font-weight: 500;
  line-height: 1.35;
}


/* =========================================================
   卡片说明文字
   ========================================================= */

.research-page .card-description {
  flex: 1;

  margin: 0 0 13px 0;

  font-size: 13.5px;
  line-height: 1.6;

  color: var(--secondary-text);
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
  padding: 6px 12px;

  border: 1px solid var(--accent-color);
  border-radius: 5px;

  background-color: #ffffff;
  color: var(--accent-color) !important;

  font-size: 12.5px;
  font-weight: 600;
  line-height: 1.4;

  text-decoration: none !important;

  transition:
    background-color 0.2s ease,
    color 0.2s ease,
    transform 0.2s ease;
}


/* 按钮悬停效果 */

.research-page .card-button:hover {
  transform: translateY(-1px);

  background-color: var(--accent-color);
  color: #ffffff !important;

  text-decoration: none !important;
}


/* =========================================================
   手机端适配
   ========================================================= */

@media screen and (max-width: 640px) {

  .research-page .research-section {
    margin-bottom: 30px;
  }

  .research-page .section-title {
    gap: 8px;

    margin-bottom: 12px;

    font-size: 20px;
  }

  .research-page .section-title::before {
    width: 3px;
    height: 22px;
  }

  .research-page .research-text {
    margin-bottom: 15px;
  }

  .research-page .research-text p {
    font-size: 14px;
    line-height: 1.65;
  }

  /*
   * 手机端无论有几个卡片都显示一列
   */

  .research-page .card-grid,
  .research-page .card-grid.single-card {
    grid-template-columns: 1fr;
    gap: 15px;
  }

  .research-page .card-image {
    padding: 8px;
  }

  .research-page .card-content {
    padding: 14px 15px 16px 15px;
  }

  .research-page .card-title {
    font-size: 15.5px;
  }

  .research-page .card-description {
    font-size: 13.5px;
  }
}

</style>


<div class="research-page">


  <!-- =====================================================
       第一部分：混合制造
       该 section 有两个卡片，因此使用两列布局
       ===================================================== -->

  <!-- =====================================================
       第三部分：复合材料
       该 section 只有一个卡片，因此使用 single-card
       ===================================================== -->

  <section class="research-section">

    <h2 class="section-title">
      1. Design for Composite Structure
    </h2>


    <!-- 单卡片居中布局 -->

    <div class="card-grid">


      <!-- ===================================================
           Card 1.1
           =================================================== -->

      <article class="card">

        <div class="card-image">

          <img
            src="{{ '/images/fiber/fiber.png' | relative_url }}"
            alt="Topology optimization for boundary fiber-reinforced materials">

        </div>


        <div class="card-content">

          <h3 class="card-title">

            3.1. Topology Optimization for Boundary Fiber-Reinforced
            Materials

            <span class="card-tag">
              灌水工作
            </span>

          </h3>


          <p class="card-description">
            Topology optimization of fiber-reinforced structures considering
            material anisotropy, fiber orientation, and manufacturing
            requirements.
          </p>


        </div>

      </article>

      <!-- ===================================================
           Card 1.1
           =================================================== -->

      <article class="card">

        <div class="card-image">

          <img
            src="{{ '/images/Fiber.png' | relative_url }}"
            alt="Topology optimization for boundary fiber-reinforced materials">

        </div>


        <div class="card-content">

          <h3 class="card-title">

            3.2. Derivable geodesic weaving: tension-compression anisotropic continuous fiber topology optimization

            <span class="card-tag">
              指导方向
            </span>

          </h3>


          <p class="card-description">
            A dual-field topology optimization framework that converts differentiable geodesic fields into dense, continuous, fabrication-ready fiber paths while accounting for the bi-modulus behavior of printed composites.
          </p>


        </div>

      </article>
    </div>

  </section>
</div>
