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
    grid-template-columns: 218px minmax(0, 1fr);
    gap: 18px;
    padding: 17px 0;
    border-bottom: 1px solid var(--line);
  }

  .mit-publication:last-child {
    border-bottom: 0;
  }

  .mit-publication__media {
    display: flex;
    min-height: 132px;
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
    width: 100%;
    height: 132px;
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
      min-height: 165px;
    }

    .mit-publication__media img {
      height: 165px;
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
              <strong>The University of Osaka</strong>. My research lies at the intersection of
              computational mechanics, applied mathematics, and informatics.
            </p>
            <p>
              I develop generative design methods for advanced mechanical products, translating
              physical principles into mathematical formulations, scalable optimization algorithms,
              and high-performance software.
            </p>
            <p>
              I received my Ph.D. in Mechanical Engineering from the University of Alberta, with a
              dissertation on topology optimization under additive-manufacturing constraints.
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
            My current work focuses on manufacturable optimization methods that remain reliable
            and computationally scalable for complex engineering systems.
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
              <span>Topology optimization and advanced design methods for additive manufacturing.</span>
            </div>
          </li>
          <li>
            <time>Feb. 2024 — Aug. 2025</time>
            <div class="mit-experience__entry">
              <strong>Specially Appointed Researcher · Osaka University</strong>
              <span>Design Engineering Laboratory, supervised by Prof. Kentaro Yaji.</span>
            </div>
          </li>
          <li>
            <time>Dec. 2023</time>
            <div class="mit-experience__entry">
              <strong>Ph.D. in Mechanical Engineering · University of Alberta</strong>
              <span>Topology Optimization Considering Additive Manufacturing Constraints.</span>
            </div>
          </li>
          <li>
            <time>Feb. 2020 — Feb. 2021</time>
            <div class="mit-experience__entry">
              <strong>Visiting Research Student · Shandong University</strong>
              <span>Computational design and additive manufacturing in Prof. Jikai Liu’s group.</span>
            </div>
          </li>
          <li>
            <time>Jun. 2018</time>
            <div class="mit-experience__entry">
              <strong>B.Eng. in Mechanical Engineering · Taiyuan University of Science and Technology</strong>
              <span>Mechanical design, modeling, and engineering analysis.</span>
            </div>
          </li>
        </ol>
      </section>

      <section id="research" class="mit-section" aria-labelledby="research-title">
        <h2 id="research-title">Selected Research Works</h2>
        <p class="mit-section__note">
          Representative projects in manufacturable design, scalable computing, and geometric intelligence.
        </p>

        <article class="mit-publication">
          <a class="mit-publication__media" href="{{ '/portfolio/sub/HASM/' | relative_url }}">
            <img
              src="{{ '/images/HASM.png' | relative_url }}"
              alt="Hybrid additive-subtractive manufacturing optimization"
              loading="lazy">
          </a>
          <div>
            <p class="mit-publication__type">Design for Manufacturing</p>
            <h3>
              <a href="{{ '/portfolio/sub/HASM/' | relative_url }}">
                Topology Optimization for Multi-axis Hybrid Manufacturing
              </a>
            </h3>
            <p class="mit-publication__description">
              Design methods combining multi-axis forming with additive and subtractive processes
              for complex, high-quality components at lower manufacturing cost.
            </p>
            <p class="mit-publication__cn">
              面向多轴增减材复合制造的拓扑优化，在降低制造成本的同时实现复杂、高质量零件设计。
            </p>
            <ul class="mit-publication__links">
              <li><a href="{{ '/portfolio/sub/HASM/' | relative_url }}">project page</a></li>
              <li>·</li>
              <li><a href="{{ '/publications/' | relative_url }}">related publications</a></li>
            </ul>
          </div>
        </article>

        <article class="mit-publication">
          <a class="mit-publication__media" href="{{ '/portfolio/sub/HASM/' | relative_url }}">
            <img
              src="{{ '/images/SDGIF_Rusult_7.gif' | relative_url }}"
              alt="Hybrid additive-subtractive manufacturing optimization"
              loading="lazy">
          </a>
          <div>
            <p class="mit-publication__type">Design for Manufacturing</p>
            <h3>
              <a href="{{ '/portfolio/sub/HASM/' | relative_url }}">
                Topology Optimization for Multi-axis Additive Manufacturing
              </a>
            </h3>
            <p class="mit-publication__description">
              Design methods combining multi-axis forming with additive and subtractive processes
              for complex, high-quality components at lower manufacturing cost.
            </p>
            <p class="mit-publication__cn">
              面向多轴增减材复合制造的拓扑优化，在降低制造成本的同时实现复杂、高质量零件设计。
            </p>
            <ul class="mit-publication__links">
              <li><a href="{{ '/portfolio/sub/HASM/' | relative_url }}">project page</a></li>
              <li>·</li>
              <li><a href="{{ '/publications/' | relative_url }}">related publications</a></li>
            </ul>
          </div>
        </article>

        <article class="mit-publication">
          <a class="mit-publication__media" href="{{ '/portfolio/sub/MOLD/' | relative_url }}">
            <img
              src="{{ '/images/cooling2.png' | relative_url }}"
              alt="Optimized cooling-channel design"
              loading="lazy">
          </a>
          <div>
            <p class="mit-publication__type">Thermal Management</p>
            <h3>
              <a href="{{ '/portfolio/sub/MOLD/' | relative_url }}">
                Topology Optimization for Dual Flow Heat Exchanger
              </a>
            </h3>
            <p class="mit-publication__description">
              Intelligent cooling-channel layouts that shorten production cycles, improve surface
              quality, and reduce the cost of advanced mold fabrication.
            </p>
            <p class="mit-publication__cn">
              通过智能冷却流道设计缩短生产周期、提升表面质量，并降低先进模具的制造成本。
            </p>
            <ul class="mit-publication__links">
              <li><a href="{{ '/portfolio/sub/MOLD/' | relative_url }}">project page</a></li>
              <li>·</li>
              <li><a href="{{ '/publications/' | relative_url }}">related publications</a></li>
            </ul>
          </div>
        </article>


        <article class="mit-publication">
          <a class="mit-publication__media" href="{{ '/portfolio/sub/MOLD/' | relative_url }}">
            <img
              src="{{ '/images/SDGIF_Rusult_6.gif' | relative_url }}"
              alt="Optimized cooling-channel design"
              loading="lazy">
          </a>
          <div>
            <p class="mit-publication__type">Design for Manufacturing</p>
            <h3>
              <a href="{{ '/portfolio/sub/MOLD/' | relative_url }}">
                Metal Additive Manufacturing oriented Design
              </a>
            </h3>
            <p class="mit-publication__description">
              Intelligent cooling-channel layouts that shorten production cycles, improve surface
              quality, and reduce the cost of advanced mold fabrication.
            </p>
            <p class="mit-publication__cn">
              通过智能冷却流道设计缩短生产周期、提升表面质量，并降低先进模具的制造成本。
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
            href="{{ '/softwares/software_1/' | relative_url }}">
            <img
              src="{{ '/images/Fiber.png' | relative_url }}"
              alt="Large-scale topology optimization result"
              loading="lazy">
          </a>
          <div>
            <p class="mit-publication__type">Design for Manufacturing</p>
            <h3>
              <a href="{{ '/softwares/software_1/' | relative_url }}">
                Topology Optimization for Fiber Reinforced Composite Material
              </a>
            </h3>
            <p class="mit-publication__description">
              OpenMP- and PETSc-based solvers for high-resolution problems with tens of millions
              of elements, producing smooth and manufacturable structures.
            </p>
            <p class="mit-publication__cn">
              基于 OpenMP 与 PETSc 的高性能求解框架，面向千万级单元实现平滑、可制造的大规模设计。
            </p>
            <ul class="mit-publication__links">
              <li><a href="{{ '/softwares/software_1/' | relative_url }}">software page</a></li>
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
                Topology Optimization Meets Editable CAD
              </a>
            </h3>
            <p class="mit-publication__description">
              Reconstruction of optimized shapes as editable, history-based, fully parametric CAD
              models for fast downstream refinement.
            </p>
            <p class="mit-publication__cn">
              将优化结果重建为可编辑、保留建模历史的参数化 CAD 模型，支持快速设计迭代。
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
            Embed process constraints directly into generative design.
          </li>
          <li>
            <strong>Physics → Algorithms</strong>
            Translate essential mechanisms into robust formulations.
          </li>
          <li>
            <strong>Algorithms → Software</strong>
            Scale optimization through high-performance computing.
          </li>
        </ul>
      </section>

      <section class="mit-side-panel">
        <h2>Contact &amp; Links</h2>
        <ul class="mit-contact-list">
          <li><a href="mailto:shuzhi@ualberta.ca">shuzhi@ualberta.ca</a></li>
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
