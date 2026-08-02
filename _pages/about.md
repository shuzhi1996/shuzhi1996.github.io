---
permalink: /
title: "About"
author_profile: false
redirect_from:
  - /about/
  - /about.html
---

<link
  rel="stylesheet"
  href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css"
  integrity="sha256-p4NxAoJBhIIN+hmNHrzRCf9tD/miZyoHS5obTRR9BMY="
  crossorigin="">

<style>
  .page__title {
    display: none;
  }

  /* Release the theme's unused author-sidebar space on desktop. */
  @media (min-width: 57.8125em) {
    #main > .page {
      width: 100%;
      float: none;
      margin: 0;
      padding-left: 0;
      padding-right: 0;
    }
  }

  .mit-home {
    --ink: #333333;
    --muted: #666666;
    --line: #e5e5e5;
    --soft: #f7f7f7;
    --accent: #1386a8;
    --accent-dark: #096b88;
    container: mit-home / inline-size;
    color: var(--ink);
    font-family: "Helvetica Neue", Helvetica, Arial, "PingFang SC", "Microsoft YaHei", sans-serif;
    font-size: 14px;
    line-height: 1.55;
    text-align: left;
  }

  .mit-home,
  .mit-home * {
    box-sizing: border-box;
  }

  .mit-home p,
  .mit-home li,
  .mit-home h1,
  .mit-home h2,
  .mit-home h3 {
    hyphens: none;
    text-align: left;
    word-spacing: normal;
  }

  .mit-home a {
    color: var(--accent);
    text-decoration: none;
  }

  .mit-home a:hover,
  .mit-home a:focus-visible {
    color: var(--accent-dark);
    text-decoration: underline;
  }

  .mit-layout {
    display: grid;
    grid-template-columns: minmax(0, 3fr) minmax(250px, 1fr);
    gap: clamp(28px, 4cqi, 42px);
    align-items: start;
  }

  .mit-main {
    min-width: 0;
  }

  .mit-home h1 {
    margin: 0 0 18px;
    padding: 0 0 14px;
    border-bottom: 1px solid var(--line);
    color: var(--ink);
    font-size: clamp(1.85rem, 4cqi, 2.15rem);
    font-weight: 700;
    line-height: 1.15;
    letter-spacing: -0.025em;
  }

  .mit-home h1 span {
    color: #777777;
    font-size: 0.62em;
    font-weight: 500;
    letter-spacing: 0;
  }

  .mit-bio {
    scroll-margin-top: 58px;
  }

  .mit-bio__row {
    display: grid;
    grid-template-columns: 198px minmax(0, 1fr);
    gap: 18px;
    align-items: start;
  }

  .mit-bio__portrait {
    display: block;
    width: 100%;
    aspect-ratio: 0.9;
    border: 1px solid #777777;
    background: var(--soft);
    object-fit: cover;
  }

  .mit-bio__copy p {
    max-width: 74ch;
    margin: 0 0 12px;
    color: #444444;
    line-height: 1.62;
  }

  .mit-bio__copy strong {
    color: var(--ink);
  }

  .mit-quick-links {
    display: flex;
    flex-wrap: wrap;
    gap: 6px 14px;
    margin-top: 14px;
    padding-top: 12px;
    border-top: 1px solid var(--line);
    font-size: 0.9rem;
  }

  .mit-interest-summary {
    margin-top: 18px;
    padding: 15px 0 2px;
    border-top: 1px solid var(--line);
    color: #444444;
  }

  .mit-interest-summary p {
    margin: 0 0 9px;
    line-height: 1.62;
  }

  .mit-section {
    scroll-margin-top: 58px;
    margin-top: 26px;
    padding-top: 20px;
    border-top: 1px solid var(--line);
  }

  .mit-section h2 {
    margin: 0 0 14px;
    padding: 0;
    border: 0;
    color: var(--ink);
    font-size: 1.55rem;
    font-weight: 700;
    line-height: 1.3;
    letter-spacing: -0.015em;
  }

  .mit-section__note {
    margin: -7px 0 16px;
    color: #777777;
    font-size: 0.84rem;
  }

  .mit-experience {
    position: relative;
    display: grid;
    margin: 0;
    padding: 3px 0;
    list-style: none;
  }

  .mit-experience::before {
    position: absolute;
    top: 21px;
    bottom: 22px;
    left: 152px;
    width: 1px;
    background: linear-gradient(to bottom, #a9d4e0, #dce8ec);
    content: "";
  }

  .mit-experience li {
    position: relative;
    display: grid;
    grid-template-columns: 132px 16px minmax(0, 1fr);
    gap: 12px;
    align-items: start;
    margin: 0;
    padding: 10px 0 0;
  }

  .mit-experience li::before {
    z-index: 1;
    grid-column: 2;
    grid-row: 1;
    justify-self: center;
    width: 9px;
    height: 9px;
    margin-top: 5px;
    border: 2px solid #ffffff;
    border-radius: 50%;
    background: var(--accent);
    box-shadow: 0 0 0 2px rgba(19, 134, 168, 0.18);
    content: "";
  }

  .mit-experience time {
    grid-column: 1;
    grid-row: 1;
    padding-top: 1px;
    color: #52636a;
    font-size: 0.78rem;
    font-weight: 700;
    font-variant-numeric: tabular-nums;
    line-height: 1.45;
    text-align: right;
  }

  .mit-experience__entry {
    grid-column: 3;
    grid-row: 1;
    min-width: 0;
    padding: 0 0 16px;
    border-bottom: 1px solid var(--line);
  }

  .mit-experience li:last-child .mit-experience__entry {
    border-bottom: 0;
  }

  .mit-experience__entry strong {
    display: block;
    color: var(--ink);
    font-size: 0.94rem;
    font-weight: 700;
    line-height: 1.45;
  }

  .mit-experience__entry span {
    display: block;
    max-width: 68ch;
    margin-top: 4px;
    color: var(--muted);
    font-size: 0.84rem;
    line-height: 1.55;
  }

  .mit-publication {
    display: grid;
    grid-template-columns: 350px minmax(0, 1fr);
    gap: 18px;
    padding: 17px 0;
    border-bottom: 1px solid var(--line);
  }

  .mit-publication:last-child {
    border-bottom: 0;
  }

  .mit-publication__media {
    display: flex;
    min-height: 0;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    border: 1px solid #ffffffff;
    background: #ffffffff;
  }

  .mit-publication__media--split {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 4px;
    padding: 4px;
  }

  .mit-publication__media--triple {
    grid-template-columns: repeat(3, minmax(0, 1fr));
  }

  .mit-publication__media img {
    display: block;
    width: auto;
    max-width: 100%;
    height: auto;
    max-height: 240px;
    margin: 0;
    border: 0;
    object-fit: contain;
  }

  .mit-publication__type {
    margin: 0 0 4px;
    color: #777777;
    font-size: 0.73rem;
    font-weight: 700;
    letter-spacing: 0.07em;
    text-transform: uppercase;
  }

  .mit-publication h3 {
    margin: 0 0 7px;
    color: var(--ink);
    font-size: 1.03rem;
    font-weight: 700;
    line-height: 1.38;
  }

  .mit-publication__description {
    max-width: 72ch;
    margin: 0 0 6px;
    color: #505050;
    font-size: 0.9rem;
    line-height: 1.55;
  }

  .mit-publication__cn {
    max-width: 72ch;
    margin: 0 0 8px;
    color: #777777;
    font-size: 0.82rem;
    line-height: 1.65;
  }

  .mit-publication__links {
    display: flex;
    flex-wrap: wrap;
    gap: 4px 9px;
    margin: 0;
    padding: 0;
    color: #999999;
    font-size: 0.82rem;
    list-style: none;
  }

  .mit-sidebar {
    min-width: 0;
  }

  .mit-side-panel {
    margin-bottom: 18px;
    padding: 18px;
    border: 1px solid #dddddd;
    background: var(--soft);
  }

  .mit-side-panel h2,
  .mit-side-panel h3 {
    margin: 0 0 13px;
    padding: 0;
    border: 0;
    color: var(--ink);
    font-size: 1.08rem;
    font-weight: 700;
    line-height: 1.35;
    text-align: center;
  }

  .mit-side-panel__image {
    display: block;
    width: 100%;
    max-height: 185px;
    margin: 0 0 14px;
    border: 0;
    object-fit: contain;
  }

  .mit-focus-list,
  .mit-contact-list {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  .mit-focus-list li {
    margin: 0;
    padding: 8px 0;
    border-top: 1px solid #e2e2e2;
    color: #555555;
    font-size: 0.86rem;
    line-height: 1.45;
  }

  .mit-focus-list strong {
    display: block;
    color: #333333;
  }

  .mit-contact-list li {
    margin: 0;
    padding: 4px 0;
    font-size: 0.87rem;
  }

  .mit-location {
    margin: 13px 0 0;
    padding-top: 11px;
    border-top: 1px solid #e2e2e2;
    color: #666666;
    font-size: 0.84rem;
    line-height: 1.5;
  }

  #visitor-map {
    width: 100%;
    height: 235px;
    border: 1px solid #d5d5d5;
    background: #e3eaed;
  }

  .mit-map-status {
    margin: 8px 0 0;
    color: #777777;
    font-size: 0.76rem;
    line-height: 1.45;
  }

  .mit-map-status[data-state="error"] {
    color: #9b3c32;
  }

  .leaflet-container {
    font-family: inherit;
  }

  @container mit-home (max-width: 860px) {
    .mit-layout {
      grid-template-columns: 1fr;
    }

    .mit-sidebar {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 16px;
    }

    .mit-side-panel {
      margin-bottom: 0;
    }

    .mit-side-panel--map {
      grid-column: 1 / -1;
    }
  }

  @container mit-home (max-width: 600px) {
    .mit-bio__row {
      grid-template-columns: 126px minmax(0, 1fr);
      gap: 14px;
    }

    .mit-bio__portrait {
      aspect-ratio: 0.82;
    }

    .mit-publication {
      grid-template-columns: 1fr;
      gap: 11px;
    }

    .mit-publication__media {
      min-height: 0;
    }

    .mit-publication__media img {
      height: auto;
      max-height: 320px;
    }

    .mit-sidebar {
      grid-template-columns: 1fr;
    }

    .mit-side-panel--map {
      grid-column: auto;
    }

    .mit-experience::before {
      left: 7px;
    }

    .mit-experience li {
      grid-template-columns: 16px minmax(0, 1fr);
      gap: 11px;
      padding-top: 12px;
    }

    .mit-experience li::before {
      grid-column: 1;
    }

    .mit-experience time {
      grid-column: 2;
      text-align: left;
    }

    .mit-experience__entry {
      grid-column: 2;
      grid-row: 2;
      padding-bottom: 17px;
    }
  }

  @container mit-home (max-width: 430px) {
    .mit-bio__row {
      grid-template-columns: 1fr;
    }

    .mit-bio__portrait {
      width: min(190px, 62%);
      aspect-ratio: 0.9;
    }

  }
</style>

<div class="mit-home">
  <div class="mit-layout">
    <main class="mit-main">
      <section id="bio" class="mit-bio" aria-labelledby="bio-title">
        <h1 id="bio-title">Shuzhi Xu <span>徐庶之</span></h1>

        <div class="mit-bio__row">
          <img
            class="mit-bio__portrait"
            src="{{ '/images/profile.png' | relative_url }}"
            alt="Portrait of Shuzhi Xu"
            fetchpriority="high">

          <div class="mit-bio__copy">
            <p>
              I am a <strong>JSPS Postdoctoral Fellow</strong> at
              <strong>The University of Osaka</strong>. My research focuses on topology optimization,
              computational design, and design for advanced manufacturing.
            </p>
            <p>
              I develop optimization methods that incorporate physical behavior and manufacturing
              constraints directly into the design process. My work spans structural and thermal-fluid
              design, additive and hybrid manufacturing, composite materials, and CAD reconstruction.
            </p>
            <p>
              I received my Ph.D. in Mechanical Engineering from the University of Alberta. My
              doctoral research investigated topology optimization with additive-manufacturing
              constraints.
            </p>

            <div class="mit-quick-links" aria-label="Profile links">
              <a href="{{ '/publications/' | relative_url }}">Publications</a>
              <a href="{{ '/research/' | relative_url }}">Research</a>
              <a href="{{ '/cv/' | relative_url }}">Curriculum Vitae</a>
              <a href="mailto:shuzhi@ualberta.ca">Email</a>
            </div>
          </div>
        </div>

        <div class="mit-interest-summary">
          <p>
            <strong>Research Interests:</strong>
            Topology Optimization; Design for Manufacturing; Multi-fidelity Modeling;
            High-Performance Computing.
          </p>
          <p>
            My current work aims to make optimized designs physically meaningful, computationally
            tractable, and compatible with practical manufacturing processes.
          </p>
        </div>
      </section>

      <section id="experience" class="mit-section" aria-labelledby="experience-title">
        <h2 id="experience-title">Experience</h2>
        <ol class="mit-experience">
          <li>
            <time>Since Sep. 2025</time>
            <div class="mit-experience__entry">
              <strong>JSPS Postdoctoral Fellow · The University of Osaka</strong>
              <span>Topology optimization and computational design for advanced manufacturing.</span>
            </div>
          </li>
          <li>
            <time>Feb. 2024 — Aug. 2025</time>
            <div class="mit-experience__entry">
              <strong>Specially Appointed Researcher · The University of Osaka</strong>
              <span>Research on topology optimization and design engineering in Prof. Kentaro Yaji’s group.</span>
            </div>
          </li>
          <li>
            <time>Sep. 2018 — Dec. 2023</time>
            <div class="mit-experience__entry">
              <strong>Ph.D. in Mechanical Engineering · University of Alberta</strong>
              <span>Topology Optimization Considering Additive Manufacturing Constraints.</span>
            </div>
          </li>
          <li>
            <time>Feb. 2020 — Feb. 2021</time>
            <div class="mit-experience__entry">
              <strong>Visiting Research Student · Shandong University</strong>
              <span>Research collaboration on topology optimization and additive manufacturing in Prof. Jikai Liu’s group.</span>
            </div>
          </li>
          <li>
            <time>Sep. 2014 — Jun. 2018</time>
            <div class="mit-experience__entry">
              <strong>B.Eng. in Mechanical Engineering · Taiyuan University of Science and Technology</strong>
              <span>Undergraduate study in mechanical design, modeling, and engineering analysis.</span>
            </div>
          </li>
        </ol>
      </section>

      <section id="research" class="mit-section" aria-labelledby="research-title">
        <h2 id="research-title">Selected Research Works</h2>
        <p class="mit-section__note">
          Representative projects in manufacturing-aware optimization, thermal-fluid design,
          composite structures, and CAD reconstruction.
        </p>

        <article class="mit-publication">
          <a class="mit-publication__media" href="{{ '/project/HASM/HASM.html' | relative_url }}">
            <img
              src="{{ '/images/HASM.png' | relative_url }}"
              alt="Hybrid additive-subtractive manufacturing optimization"
              loading="lazy">
          </a>
          <div>
            <p class="mit-publication__type">Design for Manufacturing</p>
            <h3>
              <a href="{{ '/project/HASM/HASM.html' | relative_url }}">
                1. Topology Optimization for Multi-Axis Hybrid Manufacturing
              </a>
            </h3>
            <p class="mit-publication__description">
              Topology optimization methods for integrated multi-axis additive and subtractive
              manufacturing, accounting for process accessibility when generating complex,
              manufacturable components.
            </p>
            <p class="mit-publication__cn">
              面向多轴增材与减材复合制造的拓扑优化方法，在设计过程中考虑加工可达性，
              以生成复杂且具备可制造性的零件结构。
            </p>
            <ul class="mit-publication__links">
              <li><a href="{{ '/portfolio/portfolio-1/' | relative_url }}">research page</a></li>
              <li>·</li>
              <li><a href="{{ '/project/HASM/HASM.html' | relative_url }}">project page</a></li>
              <li>·</li>
              <li><a href="{{ '/publications/' | relative_url }}">related publications</a></li>
            </ul>
          </div>
        </article>

        <article class="mit-publication">
          <a class="mit-publication__media" href="{{ '/project/MAM/mam.html' | relative_url }}">
            <img
              src="{{ '/images/SDGIF_Rusult_7.gif' | relative_url }}"
              alt="Topology optimization for multi-axis additive manufacturing"
              loading="lazy">
          </a>
          <div>
            <p class="mit-publication__type">Design for Manufacturing</p>
            <h3>
              <a href="{{ '/project/MAM/mam.html' | relative_url }}">
                2. Topology Optimization for Multi-Axis Additive Manufacturing
              </a>
            </h3>
            <p class="mit-publication__description">
              Optimization methods that exploit multiple deposition directions in multi-axis
              additive manufacturing to reduce support requirements and expand the feasible
              design space.
            </p>
            <p class="mit-publication__cn">
              利用多轴增材制造中的多方向沉积能力开展拓扑优化，减少支撑结构需求，
              并拓展可制造结构的设计空间。
            </p>
            <ul class="mit-publication__links">
              <li><a href="{{ '/portfolio/portfolio-1/' | relative_url }}">research page</a></li>
              <li>·</li>
              <li><a href="{{ '/project/MAM/mam.html' | relative_url }}">project page</a></li>
              <li>·</li>
              <li><a href="{{ '/publications/' | relative_url }}">related publications</a></li>
            </ul>
          </div>
        </article>

        <article class="mit-publication">
          <a class="mit-publication__media" href="{{ '/portfolio/sub/' | relative_url }}">
            <img
              src="{{ '/images/cooling2.png' | relative_url }}"
              alt="Optimized cooling-channel design"
              loading="lazy">
          </a>
          <div>
            <p class="mit-publication__type">Thermal Management</p>
            <h3>
              <a href="{{ '/portfolio/sub/' | relative_url }}">
                3. Topology Optimization of Dual-Flow Heat Exchangers
              </a>
            </h3>
            <p class="mit-publication__description">
              Coupled thermal-fluid topology optimization for compact dual-flow heat exchangers,
              balancing heat-transfer performance and flow resistance within a prescribed
              design domain.
            </p>
            <p class="mit-publication__cn">
              面向紧凑型双流换热器的热流体耦合拓扑优化，在给定设计域内协调换热性能
              与流动阻力。
            </p>
            <ul class="mit-publication__links">
              <li><a href="{{ '/portfolio/sub/' | relative_url }}">project page</a></li>
              <li>·</li>
              <li><a href="{{ '/publications/' | relative_url }}">related publications</a></li>
            </ul>
          </div>
        </article>


        <article class="mit-publication">
          <a class="mit-publication__media" href="{{ '/portfolio/sub/MOLD/' | relative_url }}">
            <img
              src="{{ '/images/SDGIF_Rusult_6.gif' | relative_url }}"
              alt="Manufacturing-aware design for metal additive manufacturing"
              loading="lazy">
          </a>
          <div>
            <p class="mit-publication__type">Design for Manufacturing</p>
            <h3>
              <a href="{{ '/portfolio/sub/MOLD/' | relative_url }}">
                4. Design for Metal Additive Manufacturing
              </a>
            </h3>
            <p class="mit-publication__description">
              Manufacturing-aware topology optimization for metal additive manufacturing,
              incorporating build direction, overhang limitations, and minimum feature
              requirements into the design process.
            </p>
            <p class="mit-publication__cn">
              面向金属增材制造的可制造性拓扑优化，在设计过程中考虑成形方向、悬垂限制
              与最小特征尺寸等工艺约束。
            </p>
            <ul class="mit-publication__links">
              <li><a href="{{ '/portfolio/sub/MOLD/' | relative_url }}">project page</a></li>
              <li>·</li>
              <li><a href="{{ '/publications/' | relative_url }}">related publications</a></li>
            </ul>
          </div>
        </article>


        <article class="mit-publication">
          <a
            class="mit-publication__media"
            href="{{ '/project/GeodesicWaving/geodesic-waving.html' | relative_url }}">
            <img
              src="{{ '/images/Fiber.png' | relative_url }}"
              alt="Topology optimization of a fiber-reinforced composite structure"
              loading="lazy">
          </a>
          <div>
            <p class="mit-publication__type">Composite Design</p>
            <h3>
              <a href="{{ '/project/GeodesicWaving/geodesic-waving.html' | relative_url }}">
                5. Topology Optimization of Fiber-Reinforced Composite Structures
              </a>
            </h3>
            <p class="mit-publication__description">
              Concurrent optimization of structural topology and anisotropic material orientation
              for fiber-reinforced composites, improving structural performance while accounting
              for material and fabrication characteristics.
            </p>
            <p class="mit-publication__cn">
              针对纤维增强复合材料协同优化结构拓扑与各向异性材料方向，在考虑材料特性
              和制造要求的同时提升结构性能。
            </p>
            <ul class="mit-publication__links">
              <li><a href="{{ '/portfolio/portfolio-1/' | relative_url }}">Research page</a></li>
              <li>·</li>
              <li><a href="{{ '/project/GeodesicWaving/geodesic-waving.html' | relative_url }}">Project page</a></li>
              <li>·</li>
              <li><a href="{{ '/publications/' | relative_url }}">related publications</a></li>
            </ul>
          </div>
        </article>

        <article class="mit-publication">
          <a
            class="mit-publication__media mit-publication__media--split mit-publication__media--triple"
            href="{{ '/portfolio/portfolio-3/' | relative_url }}">
            <img
              src="{{ '/images/CAD/AM4.gif' | relative_url }}"
              alt="Topology-optimized geometry"
              loading="lazy">
            <img
              src="{{ '/images/CAD/SDGIF_Rusult_5.gif' | relative_url }}"
              alt="Editable CAD reconstruction process"
              loading="lazy">
            <img
              src="{{ '/images/CAD/SDGIF_Rusult_6.gif' | relative_url }}"
              alt="Parametric CAD feature reconstruction"
              loading="lazy">
          </a>
          <div>
            <p class="mit-publication__type">Geometric Intelligence</p>
            <h3>
              <a href="{{ '/portfolio/portfolio-3/' | relative_url }}">
                6. Topology Optimization Meets Editable CAD
              </a>
            </h3>
            <p class="mit-publication__description">
              Reconstruction of topology-optimized geometries as editable, history-based parametric
              CAD models, enabling efficient downstream modification and engineering reuse.
            </p>
            <p class="mit-publication__cn">
              将拓扑优化几何重建为可编辑且保留建模历史的参数化 CAD 模型，支持后续修改、
              工程复用与快速设计迭代。
            </p>
            <ul class="mit-publication__links">
              <li><a href="{{ '/portfolio/portfolio-3/' | relative_url }}">project page</a></li>
              <li>·</li>
              <li><a href="{{ '/publications/' | relative_url }}">related publications</a></li>
            </ul>
          </div>
        </article>
      </section>
    </main>

    <aside class="mit-sidebar" aria-label="Profile details">
      <section class="mit-side-panel">
        <h2>Research Overview</h2>
        <img
          class="mit-side-panel__image"
          src="{{ '/images/封面1.png' | relative_url }}"
          alt="Overview of topology optimization research"
          loading="lazy">
        <ul class="mit-focus-list">
          <li>
            <strong>Design → Manufacturing</strong>
            Integrate additive, subtractive, and hybrid-manufacturing constraints into topology optimization.
          </li>
          <li>
            <strong>Physics → Algorithms</strong>
            Formulate structural and thermal-fluid behavior as computational design problems.
          </li>
          <li>
            <strong>Optimization → Geometry</strong>
            Connect optimized results with manufacturable structures and editable CAD models.
          </li>
        </ul>
      </section>

      <section class="mit-side-panel">
        <h2>Contact &amp; Links</h2>
        <ul class="mit-contact-list">
          <li><a href="mailto:shuzhi@ualberta.ca">shuzhi@ualberta.ca</a></li>
          <li>WeChat: xushuzhi1996</li>
          <li>
            <a href="https://scholar.google.com.hk/citations?user=lC1RMK0AAAAJ&amp;hl=zh-CN&amp;oi=sra">
              Google Scholar
            </a>
          </li>
          <li>
            <a href="https://www.researchgate.net/profile/Shuzhi-Xu?ev=hdr_xprf">
              ResearchGate
            </a>
          </li>
          <li><a href="{{ '/cv/' | relative_url }}">Curriculum Vitae</a></li>
        </ul>
        <p class="mit-location">
          The University of Osaka<br>
          Osaka, Japan
        </p>
      </section>

      <section id="visitor" class="mit-side-panel mit-side-panel--map" aria-labelledby="visitor-title">
        <h2 id="visitor-title">Visitor Map</h2>
        <div
          id="visitor-map"
          role="region"
          aria-label="Map showing the current visitor's approximate location"></div>
        <p id="visitor-map-status" class="mit-map-status" aria-live="polite">
          Loading the map and approximate visitor location…
        </p>
      </section>
    </aside>
  </div>
</div>

<script>
  (function () {
    var mapElement = document.getElementById("visitor-map");
    var statusElement = document.getElementById("visitor-map-status");

    if (!mapElement || !statusElement) return;

    function setStatus(message, isError) {
      statusElement.textContent = message;
      statusElement.dataset.state = isError ? "error" : "ready";
    }

    function startMap() {
      if (!window.L) {
        setStatus("The map library could not be loaded. Please check your network connection.", true);
        return;
      }

      var map = window.L.map(mapElement, {
        center: [20, 0],
        zoom: 2,
        minZoom: 2,
        maxZoom: 12,
        scrollWheelZoom: false,
        worldCopyJump: true
      });

      window.L.tileLayer("https://tile.openstreetmap.org/{z}/{x}/{y}.png", {
        maxZoom: 19,
        attribution:
          '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
      }).addTo(map);

      fetch("https://ipwho.is/")
        .then(function (response) {
          if (!response.ok) throw new Error("Location service unavailable");
          return response.json();
        })
        .then(function (location) {
          var latitude = Number(location.latitude);
          var longitude = Number(location.longitude);

          if (!location.success || !Number.isFinite(latitude) || !Number.isFinite(longitude)) {
            throw new Error("Location unavailable");
          }

          var place = [location.city, location.region, location.country]
            .filter(Boolean)
            .join(", ");
          var popup = document.createElement("div");
          var popupTitle = document.createElement("strong");
          var popupPlace = document.createElement("div");

          popupTitle.textContent = "Current visit";
          popupPlace.textContent = place || "Approximate location";
          popup.appendChild(popupTitle);
          popup.appendChild(popupPlace);

          window.L.circleMarker([latitude, longitude], {
            radius: 7,
            color: "#ffffff",
            weight: 3,
            fillColor: "#1386a8",
            fillOpacity: 1
          })
            .addTo(map)
            .bindPopup(popup)
            .openPopup();

          map.setView([latitude, longitude], 4);
          setStatus(
            place
              ? "Approximate location for this visit: " + place
              : "The current visit is shown on the map.",
            false
          );
        })
        .catch(function () {
          setStatus(
            "The map is available, but the approximate location could not be detected.",
            false
          );
        });
    }

    if (window.L) {
      startMap();
      return;
    }

    var leafletScript = document.createElement("script");
    leafletScript.src = "https://unpkg.com/leaflet@1.9.4/dist/leaflet.js";
    leafletScript.integrity = "sha256-20nQCchB9co0qIjJZRGuk2/Z9VM+kNiyxNV1lvTlZBo=";
    leafletScript.crossOrigin = "";
    leafletScript.onload = startMap;
    leafletScript.onerror = function () {
      setStatus("The map library could not be loaded. Please check your network connection.", true);
    };
    document.body.appendChild(leafletScript);
  })();
</script>
