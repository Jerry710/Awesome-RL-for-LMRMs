# Awesome-RL-for-LMRMs

<div align="center">

<img src="figures/survey_logo.png" style="width: 70%;"/>

## Control, Evaluate, and Improve: A Reinforcement Learning-Centric Multimodal Reasoning Survey

[![Awesome](https://img.shields.io/badge/Awesome-0066CC?style=for-the-badge&logo=awesome-lists&logoColor=white)](https://github.com/sindresorhus/awesome) 
[![Survey](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](#) 
[![Github](https://img.shields.io/badge/Awesome--RL--for--LRMs-000000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Jerry710/Awesome-RL-for-LMRMs) 
[![HF Papers](https://img.shields.io/badge/HF--Paper-%23FFD14D?style=for-the-badge&logo=huggingface&logoColor=black)]() 
[![Twitter](https://img.shields.io/badge/Twitter-%23000000.svg?style=for-the-badge&logo=x&logoColor=white)]( )

</div>

> 💡 *You're very welcome to join our discussion (on WeChat or Slack) on the topic of multimodal reasoning.*  
> 📌 *Please feel free to ping us for any possibly missed related work.*

---

## 🔔 News

- **2025-11-XX**: Repository initialized.

---

## 🧭 Overview

一句话说明这是什么综述（领域 + 目标 + 覆盖范围）。

---

<!-- ## 📚 Contents

- [1. Introduction & Background](#1-introduction--background)
- [3. Train-time Optimization](#3-train-time-optimization)
  - [3.1 Learning Strategies & Initialization](#31-learning-strategies--initialization)
  - [3.2 Reward Modeling & Supervision](#32-reward-modeling--supervision)
  - [3.3 Trajectory Sampling](#33-trajectory-sampling)
  - [3.4 Modal Alignment & Learning Algorithm](#34-modal-alignment--learning-algorithm)
- [4. Test-time Inference](#4-test-time-inference)
  - [4.1 Sampling-based Inference](#41-sampling-based-inference)
  - [4.2 Search-based Inference](#42-search-based-inference)
  - [4.3 Dynamic Verification](#43-dynamic-verfication)
  - [4.4 Trajectory Optimization](#44-trajectory-optimization)
- [Benchmarks (5 Families)](#benchmarks)
- [Models & Systems](#models)
- [Datasets & Tools](#datasets--tools)
- [Timeline / Trends](#timeline--trends)
- [Contributing](#contributing)
- [Citation](#citation)
--- -->


## 🧭 Contents

<table width="100%; table-layout:fixed;">
  <thead>
    <colgroup>
    <col style="width:30%;">
    <col style="width:70%;">
  </colgroup>
  <thead>
    <tr>
      <th align="left">Section</th>
      <th align="left">Subsection</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>📚 <a href="#1-introduction">1. Introduction</a></td>
      <td>
        <!-- <a href="#related-surveys">Related surveys</a> ·
        <a href="#contributions">Contributions</a> -->
        <table width="100%" style="border-collapse:collapse;">
          <tr>
            <td style="border:none !important; padding:0 !important; background:transparent !important; width:50%;">
              <a href="#related-surveys">Related surveys</a>
            </td>
            <td style="border:none !important; padding:0 !important; background:transparent !important; width:50%;">
              <a href="#contributions">Contributions</a>
            </td>
          </tr>
        </table>
      </td>
    </tr>
    <tr>
      <td>🧩 <a href="#2-cei-framework-gpi-view">2. CEI Framework (GPI View)</a></td>
      <td>
        <a href="#control">Control</a> ·
        <a href="#evaluate">Evaluate</a> ·
        <a href="#improve">Improve</a>
      </td>
    </tr>
    <tr>
      <td>🏗️ <a href="#3-train-time-optimization">3. Train-time Optimization</a></td>
      <td>
        <table width="100%" style="border-collapse:collapse;">
          <tr>
            <td style="border:none !important; padding:0 !important; background:transparent !important; width:50%;">
              <a href="#31-initialization">3.1 Initialization</a><br>
              <a href="#33-trajectory-sampling">3.3 Trajectory Sampling</a><br>
            </td>
            <td style="border:none !important; padding:0 !important; background:transparent !important; width:50%;">
              <a href="#32-reward-modeling">3.2 Reward Modeling</a><br>
              <a href="#34-alignment--algorithms">3.4 Alignment &amp; Algorithms</a>
            </td>
          </tr>
        </table>
      </td>
    <tr>
      <td>🧠 <a href="#4-test-time-inference">4. Test-time Inference</a></td>
      <td>
        <table width="100%" style="border-collapse:collapse;">
          <tr>
            <td style="border:none !important; padding:0 !important; background:transparent !important; width:50%;">
              <a href="#41-sampling">4.1 Sampling</a><br>
              <a href="#43-dynamic-verification">4.3 Dynamic Verification</a>
            </td>
            <td style="border:none !important; padding:0 !important; background:transparent !important; width:50%;">
              <a href="#42-search">4.2 Search</a><br>
              <a href="#44-trajectory-optimization">4.4 Trajectory Optimization</a>
            </td>
          </tr>
        </table>
      </td>
    </tr>
    <tr>
      <td>🏁 <a href="#5-benchmarks--evaluation">5. Benchmarks &amp; Evaluation</a></td>
      <td>
        <table>
          <tr style="border:none !important; background:transparent !important;">
            <td style="border:none !important; padding:0 !important; background:transparent !important; width:50%;">
              <a href="#51-goal-driven-reasoning">5.1 Goal-driven</a><br>
              <a href="#53-temporal--planning-reasoning">5.3 Temporal &amp; Planning</a><br>
              <a href="#55-self-reflection-reasoning">5.5 Self-Reflection</a>
            </td>
            <td style="border:none !important; padding:0 !important; background:transparent !important; width:50%;">
              <a href="#52-causal--verifiable-reasoning">5.2 Causal &amp; Verifiable</a><br>
              <a href="#54-tool-enhanced--embodied-reasoning">5.4 Tool-Enhanced &amp; Embodied</a><br>
            </td>
          </tr>
          </table>
      </td>
    </tr>
    
  </tbody>
</table>

---

## 1. Introduction
### <a name="related surveys"></a>Related surveys
### <a name="contributions"></a>Contributions

## 2. CEI Framework (GPI View)
### <a name="control"></a>Control
### <a name="evaluate"></a>Evaluate
### <a name="improve"></a>Improve

## 3. Train-time Optimization
### <a name="train-31-initialization"></a>3.1 Initialization
### <a name="train-32-reward-modeling"></a>3.2 Reward Modeling
### <a name="train-33-trajectory-sampling"></a>3.3 Trajectory Sampling
### <a name="train-34-alignment--algorithms"></a>3.4 Alignment & Algorithms

## 4. Test-time Inference
### <a name="test-41-sampling"></a>4.1 Sampling
### <a name="test-42-search"></a>4.2 Search
### <a name="test-43-dynamic-verification"></a>4.3 Dynamic Verification
### <a name="test-44-trajectory-optimization"></a>4.4 Trajectory Optimization

## 5. Benchmarks & Evaluation
### <a name="bench-51-goal-driven-reasoning"></a>5.1 Goal-driven Reasoning
### <a name="bench-52-causal--verifiable-reasoning"></a>5.2 Causal & Verifiable Reasoning 
### <a name="bench-53-temporal--planning-reasoning"></a>5.3 Temporal & Planning Reasoning
### <a name="bench-54-tool-enhanced--embodied-reasoning"></a>5.4 Tool-Enhanced & Embodied Reasoning
### <a name="bench-55-self-reflection-reasoning"></a>5.5 Self-Reflection Reasoning



<!-- ## 1. Introduction & Background

简单 1–2 段，复述论文中的背景与动机。

---

## 3. Train-time Optimization
### 3.1 Learning Strategies & Initialization
- From-scratch
- Cold-start
- Curriculum-guided multistage
(See `docs/train/3.1-initialization.md`)

### 3.2 Reward Modeling & Supervision
(See `docs/train/3.2-reward.md`)

### 3.3 Trajectory Sampling
(See `docs/train/3.3-sampling.md`)

### 3.4 Modal Alignment & Learning Algorithm
(See `docs/train/3.4-alignment-algo.md`)

## 4. Test-time Inference
### 4.1 Sampling-based Inference
### 4.2 Search-based Inference
### 4.3 Dynamic Verification
### 4.4 Trajectory Optimization -->


## 2. Taxonomy of Methods

列出分类：

- Category A: ...
- Category B: ...
- Category C: ...

---

## 3. Paper List

按类别预留结构：

### 3.1 Category A

| Date | Name | Title | Paper | Code |
|------|------|-------|-------|------|

### 3.2 Category B

| Date | Name | Title | Paper | Code |
|------|------|-------|-------|------|

---

## 4. Datasets and Benchmarks

### 4.1 Goal-Driven Reasoning

| Date | Name | Title | Paper | Github |
|:-:|:-:|:-|:-:|:-:|
| 2025-08 | `Intern-S1` | Intern-S1: A Scientific Multimodal Foundation Model | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2508.15763v1) | [![GitHub Stars](https://img.shields.io/github/stars/InternLM/Intern-S1?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/InternLM/Intern-S1) |

### 4.2 Causal and Verifiable Reasoning

| Date | Name | Title | Paper | Github |
|:-:|:-:|:-|:-:|:-:|
| 2025-08 | `Intern-S1` | Intern-S1: A Scientific Multimodal Foundation Model | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2508.15763v1) | [![GitHub Stars](https://img.shields.io/github/stars/InternLM/Intern-S1?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/InternLM/Intern-S1) |

### 4.3 Temporal and Planning-Oriented Reasoning

| Date | Name | Title | Paper | Github |
|:-:|:-:|:-|:-:|:-:|
| 2025-08 | `Intern-S1` | Intern-S1: A Scientific Multimodal Foundation Model | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2508.15763v1) | [![GitHub Stars](https://img.shields.io/github/stars/InternLM/Intern-S1?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/InternLM/Intern-S1) |

### 4.4 Tool-Enhanced and Embodied Reasoning

| Date | Name | Title | Paper | Github |
|:-:|:-:|:-|:-:|:-:|
| 2025-08 | `Intern-S1` | Intern-S1: A Scientific Multimodal Foundation Model | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2508.15763v1) | [![GitHub Stars](https://img.shields.io/github/stars/InternLM/Intern-S1?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/InternLM/Intern-S1) |

### 4.5  Self-Reflection and Multi-Round Reasoning

| Date | Name | Title | Paper | Github |
|:-:|:-:|:-|:-:|:-:|
| 2025-08 | `Intern-S1` | Intern-S1: A Scientific Multimodal Foundation Model | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2508.15763v1) | [![GitHub Stars](https://img.shields.io/github/stars/InternLM/Intern-S1?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/InternLM/Intern-S1) |

---


## 5. Open Problems

先写 3–5 条你在论文里已经总结好的 future directions 的标题。

---

## 6. Citation

预留 BibTeX 区域：

```bibtex
@article{YourKey,
  title={...},
  author={...},
  journal={...},
  year={2025}
}
