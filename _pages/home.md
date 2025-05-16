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

<div align="center">
<h5>
<em>Xiang Feng<sup>1 *</sup>, Wentao Jiang<sup>1 *</sup>, Zengmao Wang<sup>1</sup>, Yong Luo<sup>1 †</sup>, Pingbo Xu<sup>2,3</sup>, Baosheng Yu<sup>4</sup>,<br/> Hua Jin<sup>5,6</sup>, Bo Du<sup>1 †</sup>, Jing Zhang<sup>1 †</sup> </em>
    <br><br>
       	<sup>1</sup> School of Computer Science, Wuhan University, China,<br/>
        <sup>2</sup> Department of Anesthesiology, Zhejiang Cancer Hospital, China,<br/> 
        <sup>3</sup> Institute of Medicine, Chinese Academy of Sciences, Hangzhou, Zhejiang, China<br/> 
        <sup>4</sup> Lee Kong Chian School of Medicine, Nanyang Technological University, Singapore<br/> 
        <sup>5</sup> Department of Anesthesiology, First People’s Hospital of Yunnan Province, China<br/> 
        <sup>6</sup> Kunming University of Science and Technology, China<br/> 
</h5>
<h5>
<sup>∗</sup> Equal contribution, <sup>†</sup> Corresponding author
</h5>
</div>

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
This project aims to enhance the reasoning capabilities of large language models in the field of anesthesiology. We focus on two key questions: (1) What model characteristics are associated with stronger anesthetic reasoning abilities? (2) How do training methodologies and test-time scaling influence LLM performance in anesthesiology-specific reasoning tasks?

During the course of the project, we developed three datasets: **AnesBench**, a bilingual benchmark for anesthetic reasoning; **AnesQA**, a supervised fine-tuning dataset; and **AnesCorpus**, a continual pretraining corpus.

**This homepage is used to display the key insights and conclusions from the paper, and it also features a detailed and interactive leaderboard.**

> For dataset access, please refer to our Hugging Face repository: [AnesBench](https://huggingface.co/datasets/MiliLab/AnesBench), [AnesQA](https://huggingface.co/datasets/MiliLab/AnesQA) and [AnesCorpus](https://huggingface.co/datasets/MiliLab/AnesCorpus).

> For the overview of the dataset, including usage examples and code, please refer to the [AnesBench GitHub repository](https://github.com/MiliLab/AnesBench).

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

 Overview of AnesBench and our work. The top section of the figure presents the benchmark's basic information, including examples for three question types and statistics. The bottom section displays multiple dimensions that may be related to the model’s reasoning ability, as revealed by our analyses and experiments.

# 📖 Paper Abstract

The application of large language models (LLMs) in the medical field has gained significant attention, yet their reasoning capabilities in more specialized domains like anesthesiology remain underexplored.In this paper, we systematically evaluatreasoning capabilities of LLMs in anesthesiology and analyze key factors influencing their performance. To this end, we introduce AnesBench, a cross-lingual benchmark designed to assess anesthesiology-related reasoning across three levels: factual retr(System 1), hybrid reasoning (System 1.x), and complex decision-making (System 2). Through extensive experiments, we first explore how model characteristics, including model scale, Chain of Thought (CoT) length, and language transferability, affect reasperformance. Then, we further evaluate the effectiveness of different training strategies, leveraging our curated anesthesiology-related dataset, including continuous pre-training (CPT) and supervised fine-tuning (SFT). Additionally, we also investigatthe test-time reasoning techniques, such as Best-of-N sampling and beam search, influence reasoning performance, and assess the impact of reasoning-enhanced model distillation, specifically DeepSeek-R1.We publicly released AnesBench, along with our CPSFT training datasets and evaluation code at https://github.com/MiliLab/AnesBench.

# 😼 Impact of Model Characteristics


<div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 15px;">
  <div style="flex: 0 1 45%; min-width: 700px; margin-bottom: 40px;">
    <figure style="position: relative;">
      <img src="{{ site.baseurl }}/assets/updated1_models_cn.png" alt="Model Scale Analysis" style="width: 100%;">
      <figcaption style="position: absolute; top: 110%; left: 50%; transform: translate(-50%, -50%); text-align: left;">
        <div style="min-width: 1000px; border: 2px solid #98ff98; border-radius: 10px; padding: 15px; margin: 10px auto; max-width: 600px; background-color: rgba(240, 255, 240, 0.7);">
          <b style="font-size: 1.2em;">Conclusion 1:</b> <b style="font-size: 1.05em;">Model performance is strongly positively correlated with model scale, yet this relationship exhibits diminishing marginal returns.</b><br>
          <b style="font-size: 1.2em;">Conclusion 2:</b> <b style="font-size: 1.05em;">Compared to System 1, the performance gains achieved by increasing model scale on System 2 are significantly lower.</b>
        </div>
      </figcaption>
    </figure>
  </div>

  <div style="flex: 0 1 45%; min-width: 700px; margin-bottom: 40px;">
    <figure style="position: relative;">
      <img src="{{ site.baseurl }}/assets/updated1_models_en.png" alt="Model Scale Analysis" style="width: 100%;">
      <figcaption style="position: absolute; top: 110%; left: 50%; transform: translate(-50%, -50%); text-align: left;">
        <div style="min-width: 1000px; border: 2px solid #98ff98; border-radius: 10px; padding: 15px; margin: 10px auto; max-width: 600px; background-color: rgba(240, 255, 240, 0.7);">
          <b style="font-size: 1.2em;">Conclusion 3:</b> <b style="font-size: 1.05em;">Consistent with findings on AnesBench, Chinese AMCQA also demonstrates a positive correlation between model performance and scale, exhibiting diminishing returns. However, the distinction between system1,system1.x and system2 is not pronounced, potentially due to dataset's limited differentiation in difficulty levels.</b><br>
        </div>
      </figcaption>
    </figure>
  </div>

  <div style="flex: 0 1 45%; min-width: 700px; margin-bottom: 40px;">
    <figure style="position: relative;">
      <img src="{{ site.baseurl }}/assets/translation_lollipop.png" alt="Model Scale Analysis" style="width: 100%;">
      <figcaption style="position: absolute; top: 110%; left: 50%; transform: translate(-50%, -50%); text-align: left;">
        <div style="min-width: 1000px; border: 2px solid #98ff98; border-radius: 10px; padding: 15px; margin: 10px auto; max-width: 600px; background-color: rgba(240, 255, 240, 0.7);">
          <b style="font-size: 1.2em;">Conclusion 4:</b> <b style="font-size: 1.05em;">Language transfer ability remains critical for multilingual model performance in anesthesia reasoning. We recommend continued pre-training to address the deficiency in domain-specific knowledge across languages at the stable language ability stage.</b><br>
        </div>
      </figcaption>
    </figure>
  </div>

  <div style="flex: 0 1 45%; min-width: 1000px; margin-bottom: 40px;">
    <figure style="position: relative;">
      <img src="{{ site.baseurl }}/assets/models_length.png" alt="Model Scale Analysis" style="width: 100%;">
      <figcaption style="position: absolute; top: 110%; left: 50%; transform: translate(-50%, -50%); text-align: left;">
        <div style="min-width: 1000px; border: 2px solid #98ff98; border-radius: 10px; padding: 15px; margin: 10px auto; max-width: 600px; background-color: rgba(240, 255, 240, 0.7);">
          <b style="font-size: 1.2em;">Conclusion 5:</b> <b style="font-size: 1.05em;">Models that achieve superior performance on System2 questions often engage in longer CoT reasoning processes.</b><br>
        </div>
      </figcaption>
    </figure>
  </div>
</div>

# 😺 Impact of Training Strategies and Reasoning Techniques


<div style="width: 100%; display: flex; flex-wrap: wrap; justify-content: center; gap: 30px;">

  <div style="flex: 0 1 45%; margin-bottom: 30px; display: flex; justify-content: center; flex-direction: column;">
    <div style="display: flex; justify-content: center; width: 100%;">
    <table style="width: 100%; width: 600px; border-collapse: collapse;">
 <thead>
            <tr>
              <th style="text-align: center;" rowspan="2">Model</th>
              <th style="text-align: center;" colspan="2">SFT Data</th>
              <th style="text-align: center;" rowspan="2">Accuracy ANESBENCH</th>
            </tr>
            <tr>
              <th style="text-align: center;">AnesQA</th>
              <th style="text-align: center;">Medical-o1</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td style="text-align: center;">Qwen2.5-7B-Instruct</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">51.5</td>
            </tr>
            <tr>
              <td style="text-align: center;" rowspan="3">Qwen2.5-7B-Base</td>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">X</td>
              <td style="text-align: center;">49.3</td>
            </tr>
            <tr>
              <td style="text-align: center;">X</td>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">49.1</td>
            </tr>
            <tr>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">49.7</td>
            </tr>
            <tr>
              <td style="text-align: center;" rowspan="3">Qwen2.5-7B-Base-CPT</td>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">X</td>
              <td style="text-align: center;">49.7</td>
            </tr>
            <tr>
              <td style="text-align: center;">X</td>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">50.7</td>
            </tr>
            <tr>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">51.2</td>
            </tr>
          </tbody>
    </table>
    </div>
    <figcaption style="position: relative; margin-top: 30px; text-align: left;">
      <div style="min-width: 1000px; border: 2px solid #98ff98; border-radius: 10px; padding: 15px; margin: 10px auto; max-width: 600px; background-color: rgba(240, 255, 240, 0.7);">
        <b style="font-size: 1.2em;">Conclusion x:</b> <b style="font-size: 1.05em;">test content</b><br>
      </div>
    </figcaption>
  </div>

  <div style="flex: 0 1 45%; margin-bottom: 30px; display: flex; justify-content: center; flex-direction: column;">
    <div style="display: flex; justify-content: center; width: 100%;">
    <table style="width: 100%; width: 600px; border-collapse: collapse;">
      <thead>
            <tr>
              <th style="text-align: center;">Reasoning Strategy</th>
              <th style="text-align: center;">Tree Width</th>
              <th style="text-align: center;">Beam Size</th>
              <th style="text-align: center;">Step Tokens</th>
              <th style="text-align: center;">Accuracy(%)</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td style="text-align: center;">None</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">51.2</td>
            </tr>
            <tr>
              <td style="text-align: center;" rowspan="2">Best-of-N [21]</td>
              <td style="text-align: center;">4</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">51.5</td>
            </tr>
            <tr>
              <td style="text-align: center;">8</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">51.5</td>
            </tr>
            <tr>
              <td style="text-align: center;" rowspan="2">Beam Search [19]</td>
              <td style="text-align: center;">4</td>
              <td style="text-align: center;">4</td>
              <td style="text-align: center;">32</td>
              <td style="text-align: center;">52.1</td>
            </tr>
            <tr>
              <td style="text-align: center;">8</td>
              <td style="text-align: center;">8</td>
              <td style="text-align: center;">32</td>
              <td style="text-align: center;"><strong>52.4</strong></td>
            </tr>
          </tbody>
    </table>
    </div>
    <figcaption style="position: relative; margin-top: 30px; text-align: left;">
      <div style="min-width: 1000px; border: 2px solid #98ff98; border-radius: 10px; padding: 15px; margin: 10px auto; max-width: 600px; background-color: rgba(240, 255, 240, 0.7);">
        <b style="font-size: 1.2em;">Conclusion x:</b> <b style="font-size: 1.05em;">test content</b><br>
      </div>
    </figcaption>
  </div>

  <div style="flex: 0 1 45%; min-width: 500px; margin-bottom: 30px;">
    <figure style="position: relative;">
      <img src="{{ site.baseurl }}/assets/impact_of_r1_distillation.png" alt="Model Scale Analysis" style="width: 100%;">
      <figcaption style="position: absolute; top: 110%; left: 50%; transform: translate(-50%, -50%); text-align: left;">
        <div style="min-width: 1000px; border: 2px solid #98ff98; border-radius: 10px; padding: 15px; margin: 10px auto; max-width: 600px; background-color: rgba(240, 255, 240, 0.7);">
        <b style="font-size: 1.2em;">Conclusion x:</b> <b style="font-size: 1.05em;">test content</b><br>
        </div>
      </figcaption>
    </figure>
  </div>
</div>


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