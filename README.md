<h1 align="center">
  SODiff: Semantic-Oriented Diffusion Model <br>
  for JPEG Compression Artifacts Removal 
</h1>

<p align="center">
  <a href="https://arxiv.org/abs/2508.07346">
    <img src="https://img.shields.io/badge/Paper-arXiv-red?logo=arxiv&logoSvg">
  </a>
  <a href="https://github.com/frakenation/SODiff/releases/download/Paper/supp.pdf">
    <img src="https://img.shields.io/badge/Supplementary_material-Paper-orange.svg">
  </a>
  <a href="https://github.com/frakenation/SODiff/releases">
    <img src="https://img.shields.io/github/downloads/frakenation/SODiff/total.svg">
  </a>
  <a href="https://github.com/frakenation/SODiff">
    <img src="https://visitor-badge.laobi.icu/badge?page_id=frakenation.SODiff&right_color=violet">
  </a>
  <a href="https://github.com/frakenation/SODiff">
    <img src="https://img.shields.io/github/stars/frakenation/SODiff?style=social">
  </a>
</p>


#### 🔥🔥🔥 News

- **2025-08-10:** This repo is released.
---

> **Abstract:** JPEG, as a widely used image compression standard, often introduces severe visual artifacts when achieving high compression ratios. Although existing deep learning-based restoration methods have made considerable progress, they often struggle to recover complex texture details, resulting in over-smoothed outputs. To overcome these limitations, we propose SODiff, a novel and efficient semantic-oriented one-step diffusion model for JPEG artifacts removal. Our core idea is that effective restoration hinges on providing semantic-oriented guidance to the pre-trained diffusion model, thereby fully leveraging its powerful generative prior. To this end, SODiff incorporates a semantic-aligned image prompt extractor (SAIPE). SAIPE extracts rich features from low-quality (LQ) images and projects them into an embedding space semantically aligned with that of the text encoder. Simultaneously, it preserves crucial information for faithful reconstruction. Furthermore, we propose a quality factor-aware time predictor that implicitly learns the compression quality factor (QF) of the LQ image and adaptively selects the optimal denoising start timestep for the diffusion process. Extensive experimental results show that our SODiff outperforms recent leading methods in both visual quality and quantitative metrics. 

<p align="center">
  <img src="images/SAIPE.png" alt="SAIPE" style="width:85%;"/><br>
  <b>Figure 1:</b> SAIPE (semantic-aligned image prompt extractor) overview.
</p>

<p align="center">
  <img src="images/SODiff.png" alt="SODiff model architecture" style="width:85%;"/><br>
  <b>Figure 2:</b> Model structure of SODiff (semantic-oriented diffusion).
</p>

<table>
  <tr>
    <td align="center">
      <a href="https://imgsli.com/NDA2NDk5"><img src="images/LIVE-1_church.png" height="200"/></a><br>
<!--       <a href="https://imgsli.com/MzgzMjE3"><img src="images/val_2.png" height="200"/></a><br> -->
      <b>LIVE-1 (QF=5)</b>
    </td>
    <td align="center">
      <a href="https://imgsli.com/NDA2NTA2"><img src="images/Urban100_051.png" height="200"/></a><br>
<!--       <a href="https://imgsli.com/MzgzMjEx"><img src="images/mpii_2.png" height="200"/></a><br> -->
      <b>Urban100 (QF=5)</b>
    </td>
    <td align="center">
      <a href="https://imgsli.com/MzgzMjE0"><img src="images/test_1.png" height="200"/></a><br>
<!--       <a href="https://imgsli.com/MzgzMjE1"><img src="images/test_2.png" height="200"/></a><br> -->
      <b>PERSONA-Test</b>
    </td>
  </tr>
</table>
