---
title: "Topology Optimization for Hybrid Additive-Subtractive Manufacturing"
permalink: /portfolio/sub/HASM/
---

<div style="max-width: 1000px; margin: 0 auto; font-family: 'Segoe UI', Arial, sans-serif; font-size: 16px; line-height: 1.6; color: #333;">

<h2 style="text-align: center; margin-top: 20px;">0. Research Background</h2>
<p style="text-align: justify;">
This research focuses on topology optimization specifically tailored for hybrid additive-subtractive manufacturing (HASM). The objective is to design structures that are fully compatible with both additive and subtractive processes, ensuring manufacturability while improving surface quality.
</p>

---

<h2 style="text-align: center; margin-top: 30px;">1. Design for HASM</h2>
<div style="text-align: center;">
    <img src='/images/HASM/result1.png' style="width: 90%; margin-top: 10px;">
    <p style="margin-top: 5px; font-style: italic;">Simulation flow chart based on inherited strain method.</p>
</div>

---

<h2 style="text-align: center; margin-top: 30px;">2. Fabrication Validation</h2>
<div style="text-align: center;">
    <img src='/images/HASM/overall.png' style="width: 100%; margin-top: 10px;">
    <p style="margin-top: 5px; font-style: italic;">Overall machining process for hybrid manufacturing.</p>
</div>

<p style="text-align: justify;">
The machining process consists of three stages. The majority of the solid part is processed during the first two stages, with 32.7% completed after the first stage and 81.5% after the second. To maximize workspace and avoid collisions, cutting tools for subtractive operations during additive phases are manually removed and reinstalled with minimal setup time.
</p>

---

<h3 style="text-align: center; margin-top: 20px;">Hybrid Fabrication Stages</h3>

<div style="display: flex; justify-content: center; gap: 15px; margin-top: 20px;">
    <div style="flex: 1; text-align: center;">
        <img src='/images/HASM/AM-1.gif' style="width: 100%;">
        <img src='/images/HASM/SM-1.gif' style="width: 100%; margin-top: 10px;">
        <p style="font-style: italic;">Stage 1 of hybrid fabrication.</p>
    </div>
    <div style="flex: 1; text-align: center;">
        <img src='/images/HASM/AM-2.gif' style="width: 100%;">
        <img src='/images/HASM/SM-2.gif' style="width: 100%; margin-top: 10px;">
        <p style="font-style: italic;">Stage 2 of hybrid fabrication.</p>
    </div>
    <div style="flex: 1; text-align: center;">
        <img src='/images/HASM/AM-3.gif' style="width: 100%;">
        <img src='/images/HASM/SM-3.gif' style="width: 100%; margin-top: 10px;">
        <p style="font-style: italic;">Stage 3 of hybrid fabrication.</p>
    </div>
</div>

<p style="text-align: justify; margin-top: 20px;">
Due to the CNC system limitations (open/close control of the extruder), retraction is not possible, leading to stringing and subpar surface quality during additive steps. However, this is fully corrected during subsequent subtractive machining, demonstrating the strength of HASM.
</p>

---

<h3 style="text-align: center; margin-top: 30px;">Final Prototype</h3>
<div style="text-align: center;">
    <img src='/images/HASM/result.png' style="width: 100%; margin-top: 10px;">
    <p style="margin-top: 5px; font-style: italic;">Successfully fabricated prototype without tool interference.</p>
</div>

<p style="text-align: justify;">
The fabricated prototype confirms that the topology-optimized structure is fully manufacturable with hybrid processes. Compared to pure additive manufacturing, the hybrid approach removes staircase effects and local material accumulations, resulting in visibly improved surface quality. Some minor interfacial gaps appear due to build direction transitions, an issue specific to extrusion-based AM and not present in laser-based metal AM.
</p>

---

<h3 style="text-align: center; margin-top: 30px;">Related Publication</h3>
<div style="text-align: center;">
    <a href="https://www.sciencedirect.com/science/article/abs/pii/S0045782524005267" target="_blank">
        Xu, S., Liu, J., Yaji, K., & Lu, L. (2024). Topology optimization for hybrid additive-subtractive manufacturing incorporating dynamic process planning. <em>Computer Methods in Applied Mechanics and Engineering</em>, 431, 117270.
    </a>
</div>

</div>
