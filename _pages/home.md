---
title: "AnesBench"
layout: splash
permalink: /
header:
    overlay_color: "rgba(7, 165, 7, 0.3)"
    overlay_filter: "0.1"
    # overlay_image: {{ site.baseurl }}/assets/overview.png
excerpt: "Multi-Dimensional Evaluation of LLM Reasoning in Anesthesiology"
classes:
    - wide
---

  <div style="display: flex; justify-content: center; align-items: center;">
    <div style="text-align: center; padding: 20px;">
      <div>
        <a href="https://github.com/MiliLab/AnesBench" target="_blank" style="display: inline-block; margin: 15px;">
          <img src="https://img.shields.io/badge/Project-AnesBench-4183C4.svg?logo=Github" alt="Project Page" style="height: 30px; transition: transform 0.25s ease;" onmouseover="this.style.transform='scale(1.15)'" onmouseout="this.style.transform='scale(1)'">
        </a>
        <a href="https://arxiv.org/abs/2504.02404" target="_blank" style="display: inline-block; margin: 15px;">
          <img src="https://img.shields.io/badge/Arxiv-2504.02404-b31b1b.svg?logo=arXiv" alt="arXiv Link" style="height: 30px; transition: transform 0.25s ease;" onmouseover="this.style.transform='scale(1.15)'" onmouseout="this.style.transform='scale(1)'">
        </a>
        <a href="https://huggingface.co/datasets/MiliLab/AnesBench" target="_blank" style="display: inline-block; margin: 15px;">
          <img src="https://img.shields.io/badge/🤗%20HuggingFace-AnesBench-FFD43B.svg" alt="HuggingFace Dataset" style="height: 30px; transition: transform 0.25s ease;" onmouseover="this.style.transform='scale(1.15)'" onmouseout="this.style.transform='scale(1)'">
        </a>
      </div>
    </div>
  </div>


# 🌞 Intro
**AnesBench** is designed to assess anesthesiology-related reasoning capabilities of Large Language Models (LLMs). 
It contains 4,427 anesthesiology questions in English. 
Each question is labeled with a three-level categorization of cognitive demands and includes Chinese-English translations, 
enabling evaluation of LLMs’ knowledge, application, and clinical reasoning abilities across diverse linguistic contexts.

# 🔍 Overview
<figure>
<div align="center">
<img src="{{ site.baseurl }}/assets/overview.png">
</div>
<div align="center">
<!-- <figcaption align = "center"><b>Figure 1: Overview of the AnesBench. 
    </b></figcaption> -->
</div>
</figure>


# ⭐ Citation

If you find AnesBench helpful, please consider giving this repo a ⭐ and citing:

```latex
@article{AnesBench,
  title={AnesBench: Multi-Dimensional Evaluation of LLM Reasoning in Anesthesiology},
  author={Xiang Feng and Wentao Jiang and Zengmao Wang and Yong Luo and Pingbo Xu and Baosheng Yu and Hua Jin and Bo Du and Jing Zhang},
  journal={arXiv preprint arXiv:2504.02404},
  year={2025}
}
```