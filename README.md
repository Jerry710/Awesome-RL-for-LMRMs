# Awesome-RL-for-LMRMs

<div align="center">

<!-- <img src="figures/survey_logo.png" style="width: 70%;"/> -->

## Steer, Assess, and Refine: <br> A Reinforcement Learning-Centric Multimodal Reasoning Survey

[![Awesome](https://img.shields.io/badge/Awesome-0066CC?style=flat&logo=awesome-lists&logoColor=white)](https://github.com/sindresorhus/awesome) 
[![Survey](https://img.shields.io/badge/Paper-A42C25?style=flat&logo=arxiv&logoColor=white)](#) 
[![Github](https://img.shields.io/badge/Awesome--RL--for--LRMs-000000?style=flat&logo=github&logoColor=white)](https://github.com/Jerry710/Awesome-RL-for-LMRMs) 
[![HF Papers](https://img.shields.io/badge/🤗%20Paper-%23FFD14D?style=flat)]() 
[![Citation](https://img.shields.io/badge/✒️%20Citation-F5F5F5?style=flat)](#Citation)
<!-- [:black_nib: Citation](#Citation) -->

</div>

🎉 *You're very welcome to join our discussion (on WeChat or Email) on the topic of multimodal reasoning.*  

:heart_decoration: *If you like our project, please consider giving us a star* ⭐ *on GitHub to stay updated with the latest developments.*

📌 *Please feel free to ping us for any possibly missed related work.*



## 🔔 News

- **2026-01-28**: Repository initialized.


## 🧭 Overview

<p align="center">
  <img src="figures\Fig-1.png" width="80%" />
<!--   <img src="./Images/methods.jpg" width="45%" height="50%" /> -->
</p>


RL is rapidly reshaping multimodal *System-2* reasoning. While most multimodal LLMs still behave like *System 1* (fast, fluent, pattern-driven), recent models (*e.g.*, o1, o3, and DeepSeek-R1) show that RL can internalize slow, deliberative reasoning, *i.e.*, planning before answering, verifying intermediate steps, and revising when uncertain. 

This repo accompanies our survey on RL-centric Large Multimodal Reasoning Models (LMRMs), where RL is treated not as a peripheral trick, but as the primary mechanism for building controllable, multi-step reasoning.

The above overview diagram summarizes our **GPI-inspired Steer–Assess–Refine (SAR)** lens across the *entire train–test pipeline*:

* **Steer:** how trajectories are generated via initialization, sampling, and search.
* **Assess:** how reward modeling and dynamic verification provide feedback signals.
* **Refine:** how train-time policy optimization and test-time trajectory optimization refine reasoning paths.

It also links this SAR pipeline to **five slow-thinking capability categories** (goal-driven, causal & verifiable, temporal & planning, tool & embodied, self-reflective), serving as a  map to place methods and benchmarks into a single coordinate system.
  

#### What you'll get from this GitHub

:one: A clean taxonomy of RL-centric LMRMs (data → training → test-time inference → evaluation).

:two: Curated papers, code, and benchmarks organized around SAR, not scattered chronologically.

:three: A gap-and-opportunity checklist for pushing multimodal slow thinking beyond current heuristic pipelines.



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
<!-- | Section | Subsection |  |
|:--|:--|:--|
| 📚 [1. Introduction](#1-introduction) | [Related surveys](#related-surveys) | [Contributions](#contributions) |
| 🧩 [2. CEI Framework](#2-cei-framework-gpi-view) | [Control](#control) · [Evaluate](#evaluate) · [Improve](#improve) |
| 🏗️ [3. Train-time Optimization](#3-train-time-optimization) | [3.1 Initialization](#31-initialization)<br> [3.3 Trajectory Sampling](#33-trajectory-sampling) | [3.2 Reward Modeling](#32-reward-modeling)<br> [3.4 Alignment & Algorithms](#34-alignment--algorithms) |
| 🧠 [4. Test-time Inference](#4-test-time-inference) | [4.1 Sampling](#41-sampling)<br> [4.3 Dynamic Verification](#43-dynamic-verification) | [4.2 Search](#42-search)<br> [4.4 Trajectory Optimization](#44-trajectory-optimization) |
| 🏁 [5. Benchmarks & Evaluation](#5-benchmarks--evaluation) | [5.1 Goal-driven](#51-goal-driven)<br> [5.3 Temporal & Planning](#53-temporal--planning)<br> [5.5 Self-Reflection](#55-self-reflection) | [5.2 Causal & Verifiable](#52-causal--verifiable)<br> [5.4 Tool-Enhanced & Embodied](#54-tool-enhanced--embodied) | -->


<table>
  <thead>
    <tr>
      <th align="left">Section</th>
      <th align="left" colspan="2">Subsection</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>📚 <a href="#1-introduction">1. Introduction</a></td>
      <td><a href="#related-surveys">Related surveys</a></td>
      <td><a href="#contributions">Contributions</a></td>
    </tr>
    <tr>
      <td>🧩 <a href="#2-sar-framework">2. SAR Framework</a></td>
      <td colspan="2">
        Steer-Assess-Refine
        <!-- <a href="#control">Steer</a> · <a href="#evaluate">Assess</a> · <a href="#improve">Refine</a> -->
      </td>
    </tr>
    <tr>
      <td> 🚗 <a href="#3-train-time-optimization-of-RL-centric-multimodal-reasoning">3. Train-time Optimization of RL-Centric Multimodal Reasoning</a></td>
      <td>
        <a href="#31-training-initialization">3.1 Training Initialization</a><br>
        <a href="#33-trajectory-sampling">3.3 Trajectory Sampling</a>
      </td>
      <td>
        <a href="#32-reward-modeling">3.2 Reward Modeling</a><br>
        <a href="#train-34-modal-alignment--learning-algorithm">3.4 Modal Alignment &amp; Learning Algorithm</a>
      </td>
    </tr>
    <tr>
      <td> 🚈 <a href="#4-test-time-inference-of-RL-centric-multimodal-reasoning">4. Test-time Inference of RL-centric Multimodal Reasoning</a></td>
      <td>
        <a href="#41-sampling">4.1 Sampling</a><br>
        <a href="#43-dynamic-verification">4.3 Dynamic Verification</a>
      </td>
      <td>
        <a href="#42-search">4.2 Search</a><br>
        <a href="#44-trajectory-optimization">4.4 Trajectory Optimization</a>
      </td>
    </tr>
    <tr>
      <td> 🏆 <a href="#5-datasets--benchmarks"> 5. Datasets &amp; Benchmarks</a></td>
      <td>
        <a href="#51-goal-driven-reasoning">5.1 Goal-driven Reasoning</a><br>
        <a href="#53-temporal--planning-reasoning">5.3 Temporal &amp; Planning Reasoning</a><br>
        <a href="#55-self-reflection-reasoning">5.5 Self-Reflection Reasoning</a>
      </td>
      <td>
        <a href="#52-causal--verifiable-reasoning">5.2 Causal &amp; Verifiable Reasoning</a><br>
        <a href="#54-tool-enhanced--embodied-reasoning">5.4 Tool-Enhanced &amp; Embodied Reasoning</a>
      </td>
    </tr>
    <tr>
      <td colspan="3"> 💡 <a href="#6-challenges--opportunities"> 6. Challenges &amp; Opportunities</a></td>
    </tr>
  </tbody>
</table>





## 1. Introduction
### <a id="related-surveys"></a>:page_with_curl:Related surveys
| Date | Title | Paper | Project Page |
|:-:|:-|:-:|:-:|
| 2025.02 | From System 1 to System 2: A Survey of Reasoning Large Language Models | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2502.17419) | [![Stars](https://img.shields.io/github/stars/zzli2022/Awesome-System2-Reasoning-LLM?style=social&label=Star)](https://github.com/zzli2022/Awesome-System2-Reasoning-LLM)|
| 2025.03 | A Survey of Efficient Reasoning for Large Reasoning Models: Language Multimodality and Beyond  | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.21614) | [![GitHub Stars](https://img.shields.io/github/stars/XiaoYee/Awesome_Efficient_LRM_Reasoning?style=social&label=Star)](https://github.com/XiaoYee/Awesome_Efficient_LRM_Reasoning) | 
| 2025.03 | Mind with Eyes: from Language Reasoning to Multimodal Reasoning | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.18071) |[![GitHub Stars](https://img.shields.io/github/stars/ADaM-BJTU/Mind_with_eyes_Awesome_MLLMs_Reasoning?style=social&label=Star)](https://github.com/ADaM-BJTU/Mind_with_eyes_Awesome_MLLMs_Reasoning) | 
| 2025.04 | Reinforced MLLM: A Survey on RL-Based Reasoning in Multimodal Large Language Models | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2504.21277) | - | 
| 2025.04 | Why Reasoning Matters? A Survey of Advancements in Multimodal Reasoning | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2504.03151) | - | 
| 2025.05 | A Survey of Slow Thinking-based Reasoning LLMs using Reinforced Learning and Inference-time Scaling Law | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.02665) | - |
| 2025.05 | Perception, Reason, Think, and Plan: A Survey on Large Multimodal Reasoning Models | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.04921) | [![GitHub Stars](https://img.shields.io/github/stars/HITsz-TMG/Awesome-Large-Multimodal-Reasoning-Models?style=social&label=Star)](https://github.com/HITsz-TMG/Awesome-Large-Multimodal-Reasoning-Models) | 
| 2025.05 | Reinforcement Fine-Tuning Powers Reasoning Capability of Multimodal Large Language Models | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.18536) | [![GitHub Stars](https://img.shields.io/github/stars/Sun-Haoyuan23/Awesome-RL-based-Reasoning-MLLMs?style=social&label=Star)](https://github.com/Sun-Haoyuan23/Awesome-RL-based-Reasoning-MLLMs) |
| 2025.08 | Reinforcement Learning for Large Model: A Survey | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2508.08189) | [![GitHub Stars](https://img.shields.io/github/stars/weijiawu/Awesome-Visual-Reinforcement-Learning?style=social&label=Star)](https://github.com/weijiawu/Awesome-Visual-Reinforcement-Learning) |
| 2025.09 | Reinforcement Learning Meets Large Language Models: A Survey of Advancements and Applications Across the LLM Lifecycle | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2509.16679) | - |
| 2025.09 | A Survey of Reinforcement Learning for Large Reasoning Models | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2509.08827) |[![GitHub Stars](https://img.shields.io/github/stars/TsinghuaC3I/Awesome-RL-for-LRMs?style=social&label=Star)](https://github.com/TsinghuaC3I/Awesome-RL-for-LRMs) | 


### <a id="contributions"></a> :star2: Contributions
:one: Sections 3 and 4 follow the SAR framework systematically review and compare methods in the training and testing phases under a unified GPI perspective. This
establishes an integrated framework and clarifies the inter relationship between the two phases.

:two: Section 5 introduces a novel RL-based benchmark taxonomy, achieving a SAR-aligned restructuring of multimodal reasoning benchmarks.

:three: Section 6 explores the challenges and future directions of RL-centric multimodal reasoning, with a particular emphasis on the intrinsic coupling between RL mechanisms and multimodal scenarios.


## 2. SAR Framework

<p align="center">
  <img src="figures\topic.png" width="60%" />
<!--   <img src="./Images/methods.jpg" width="45%" height="50%" /> -->
</p>

Our overview figure organizes RL-centric LMRMs as a unified train–test loop under a GPI-style pipeline:
**Steer → Assess → Refine**.  

- :one: **Steer: guide and control reasoning trajectories**
  - Training-time: [learning strategies & initialization](#31-training-initialization).
  - Test-time: inference-time construct that establishs candidate trajectories, including [sampling-based](#41-sampling) and [search-based](#42-search) inference.

- :two: **Assess: measure and verify reasoning**
  - Training-time: [reward modeling and supervision](#32-reward-modeling).
  - Test-time: [dynamic verification](#43-dynamic-verification) that scores and filters trajectories on the fly.

- :three: **Refine: optimize reasoning behavior**
  - Training-time: reasoning behavior improvement via trajectory-level refinement strategies and learning algorithms, including  
    [sampling strategies for trajectory optimization](#33-trajectory-sampling) and [modal alignment and learning algorithms](#34-modal-alignment--learning-algorithm) that improve policies.
  - Test-time: [trajectory optimization](#44-trajectory-optimization) that refines surviving paths under compute budgets.

**Why SAR matters.** 

It turns a fast-growing literature into a single, navigable map:  
*how LMRMs establish the reasoning substrate (Steer), how LMRMs measure reasoning competence (Assess), and how LMRMs optimize reasoning behavior (Refine), consistently across training and inference.*


## 3. Train-time Optimization of RL-Centric Multimodal Reasoning
### <a id="31--training-initialization"></a>3.1 Training Initialization

<p align="center">
  <img src="figures\initialization.png" width="80%" />
<!--   <img src="./Images/methods.jpg" width="45%" height="50%" /> -->
</p>

Training Initialization focuses on how to initially bootstrap an effective reasoning policy before large-scale RL optimization. We divide the existing methods into three categories:

#### 3.1.1 From-Scratch Policy Initialization
From-scratch policy initialization acquires reasoning behaviors solely from RL signals without reliance on pre-existing policies. 

#### 3.1.2 Cold-Start Policy Initialization
Cold-start policy initialization leverages a strong foundational MLLM prior through knowledge transfer, command interaction, or trajectory injection to enhance training stability in early phases.

#### 3.1.3 Curriculum-Guided Multistage Policy Optimization
Curriculum-guided multistage optimization systematically refines the policy across sequential stages to improve robustness and generalization. 

As illustrated, existing approaches can be characterized along two dimensions, strength of behavioral prior and required level of interaction granularity (ranging from static perception to tool-level interaction and fine-grained control), providing a unified framework for understanding the trade-offs among training stability, controllability, and sample efficiency in different initialization strategies.



| Date | Name | Title | Paper | Link |
|:-:|:-:|:-|:-:|:-:|
| 2025.04 | `VLAA-Thinking-RL` | SFT or RL? An Early Investigation into Training R1-Like Reasoning Large Vision-Language Models | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2504.11468) | [![GitHub Stars](https://img.shields.io/github/stars/UCSC-VLAA/VLAA-Thinking?style=social&label=Star)](https://github.com/UCSC-VLAA/VLAA-Thinking)  |
| 2025.03 | `VisualThinker-R1-Zero` | R1-Zero's "Aha Moment" in Visual Reasoning on a 2B Non-SFT Model | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.05132) | [![GitHub Stars](https://img.shields.io/github/stars/turningpoint-ai/VisualThinker-R1-Zero?style=social&label=Star)](https://github.com/turningpoint-ai/VisualThinker-R1-Zero) |
| 2025.03 | `MM-Eureka` | MM-Eureka: Exploring Visual Aha Moment with Rule-based Large-scale Reinforcement Learning | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.07365) | [![GitHub Stars](https://img.shields.io/github/stars/ModalMinds/MM-EUREKA?style=social&label=Star)](https://github.com/ModalMinds/MM-EUREKA)  |
| 2025.04 | `NoisyRollout` | NoisyRollout: Reinforcing Visual Reasoning with Data Augmentation | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2504.18458) | [![GitHub Stars](https://img.shields.io/github/stars/NUS-TRAIL/NoisyRollout?style=social&label=Star)](https://github.com/NUS-TRAIL/NoisyRollout) |
| 2025.04 | `FAST-GRPO` | Fast-Slow Thinking for Large Vision-Language Model Reasoning | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2504.13055) | [![GitHub Stars](https://img.shields.io/github/stars/Mr-Loevan/FAST?style=social&label=Star)](https://github.com/Mr-Loevan/FAST) |
| 2025.06 | `Metis-RISE` | Metis-RISE: RL Incentivizes and SFT Enhances Multimodal Reasoning Model Learning |  [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2506.13056) | [![GitHub Stars](https://img.shields.io/github/stars/MM-Thinking/Metis-RISE?style=social&label=Star)](https://github.com/MM-Thinking/Metis-RISE) |
| 2025.08 | `Affordance-R1` | Affordance-R1: Reinforcement Learning for Generalizable Affordance Reasoning in Multimodal Large Language Model | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2508.06206) | [![GitHub Stars](https://img.shields.io/github/stars/hq-King/Affordance-R1?style=social&label=Star)](https://github.com/hq-King/Affordance-R1) |
| 2025.03 | `UI-RL` | UI-R1: Enhancing Efficient Action Prediction of GUI Agents by Reinforcement Learning | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.21620) | [![GitHub Stars](https://img.shields.io/github/stars/lll6gg/UI-R1?style=social&label=Star)](https://github.com/lll6gg/UI-R1) |
| 2025.05 | `PixelThink` | PixelThink: Towards Efficient Chain-of-Pixel Reasoning | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.23727) | [![GitHub Stars](https://img.shields.io/github/stars/songw-zju/PixelThink?style=social&label=Star)](https://github.com/songw-zju/PixelThink) |
| 2025.07 | `VL-Cogito` | VL-Cogito: Progressive Curriculum Reinforcement Learning for Advanced Multimodal Reasoning | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2507.22607) | [![GitHub Stars](https://img.shields.io/github/stars/alibaba-damo-academy/VL-Cogito?style=social&label=Star)](https://github.com/alibaba-damo-academy/VL-Cogito) |
| 2025.03 | `OpenVLThinker` | OpenVLThinker: Complex Vision-Language Reasoning via Iterative SFT-RL Cycles | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.17352) | [![GitHub Stars](https://img.shields.io/github/stars/yihedeng9/OpenVLThinker?style=social&label=Star)](https://github.com/yihedeng9/OpenVLThinker)  |
| 2025.05 | `X-Reasoner` | X-Reasoner: Towards Generalizable Reasoning Across Modalities and Domains | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.03981) | [![GitHub Stars](https://img.shields.io/github/stars/microsoft/x-reasoner?style=social&label=Star)](https://github.com/microsoft/x-reasoner)  |
| 2025.06 | `ReVisual-R1` | Advancing Multimodal Reasoning: From Optimized Cold Start to Staged Reinforcement Learning | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2506.04207) | [![GitHub Stars](https://img.shields.io/github/stars/CSfufu/Revisual-R1?style=social&label=Star)](https://github.com/CSfufu/Revisual-R1)  |
| 2025.03 | `Visual-RFT` | Visual-RFT: Visual Reinforcement Fine-Tuning | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.01785) | [![GitHub Stars](https://img.shields.io/github/stars/Liuziyu77/Visual-RFT?style=social&label=Star)](ttps://github.com/Liuziyu77/Visual-RFT)  |
| 2025.01 | `Kimi k1.5` | Kimi k1.5: Scaling Reinforcement Learning with LLMs | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2501.12599) | [![GitHub Stars](https://img.shields.io/github/stars/MoonshotAI/Kimi-k1.5?style=social&label=Star)](https://github.com/MoonshotAI/Kimi-k1.5)  |
| 2025.05 | `OpenThinkIMG` | OpenThinkIMG: Learning to Think with Images via Visual Tool Reinforcement Learning | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.08617) | [![GitHub Stars](https://img.shields.io/github/stars/OpenThinkIMG/OpenThinkIMG?style=social&label=Star)](https://github.com/OpenThinkIMG/OpenThinkIMG) |
| 2025.08 | `VITAL` | Thinking With Videos: Multimodal Tool-Augmented Reinforcement Learning for Long Video Reasoning | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2508.04416) | [![GitHub Stars](https://img.shields.io/github/stars/zhang9302002/ThinkingWithVideos?style=social&label=Star)](https://github.com/zhang9302002/ThinkingWithVideos) |
| 2025.05 | `VPRL` | Visual Planning: Let's Think Only with Images | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.11409) | [![GitHub Stars](https://img.shields.io/github/stars/yix8/VisualPlanning?style=social&label=Star)](https://github.com/yix8/VisualPlanning) |
| 2025.05 | `VLM-R3` | VLM-R$^3$: Region Recognition, Reasoning, and Refinement for Enhanced Multimodal Chain-of-Thought | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.16192) | - |
| 2025.04 | `InfiGUI-R1` | InfiGUI-R1: Advancing Multimodal GUI Agents from Reactive Actors to Deliberative Reasoners | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2504.14239) | [![GitHub Stars](https://img.shields.io/github/stars/Reallm-Labs/InfiGUI-R1?style=social&label=Star)](https://github.com/Reallm-Labs/InfiGUI-R1) |
| 2025.04 | `GUI-R1` | GUI-R1: A Generalist R1-Style Vision-Language Action Model For GUI Agents | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2504.10458) | [![GitHub Stars](https://img.shields.io/github/stars/ritzz-ai/GUI-R1?style=social&label=Star)](https://github.com/ritzz-ai/GUI-R1) |
| 2025.05 | `G1` | G1: Bootstrapping Perception and Reasoning Abilities of Vision-Language Model via Reinforcement Learning | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.13426) | [![GitHub Stars](https://img.shields.io/github/stars/chenllliang/G1?style=social&label=Star)](https://github.com/chenllliang/G1) |
| 2025.05 | `PixelReasoner` | Pixel Reasoner: Incentivizing Pixel-Space Reasoning with Curiosity-Driven Reinforcement Learning | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.15966) | [![GitHub Stars](https://img.shields.io/github/stars/TIGER-AI-Lab/Pixel-Reasoner?style=social&label=Star)](https://github.com/TIGER-AI-Lab/Pixel-Reasoner) |
| 2025.06 | `E2H Reasoner` | Curriculum Reinforcement Learning from Easy to Hard Tasks Improves LLM Reasoning | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2506.06632) | [![GitHub Stars](https://img.shields.io/github/stars/divelab/E2H-Reasoning?style=social&label=Star)](https://github.com/divelab/E2H-Reasoning)  |
| 2025.05 | `Self-Evolving Curriculum` | Self-Evolving Curriculum for LLM Reasoning | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.14970) | [![GitHub Stars](https://img.shields.io/github/stars/ServiceNow/sec?style=social&label=Star)](https://github.com/ServiceNow/sec)  |
| 2025.05 | `Infi-MMR` | Infi-MMR: Curriculum-based Unlocking Multimodal Reasoning via Phased Reinforcement Learning in Multimodal Small Language Models | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.23091) | [![GitHub Stars](https://img.shields.io/github/stars/InfiXAI/Infi-MMR?style=social&label=Star)](https://github.com/InfiXAI/Infi-MMR)  |
| 2025.05 | `Seed1.5-VL` | Seed1.5-VL Technical Report | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.07062) | [![GitHub Stars](https://img.shields.io/github/stars/ByteDance-Seed/Seed1.5-VL?style=social&label=Star)](https://github.com/ByteDance-Seed/Seed1.5-VL)  |
| 2025.07 | `GLM-4.1V-Thinking` | GLM-4.5V and GLM-4.1V-Thinking: Towards Versatile Multimodal Reasoning with Scalable Reinforcement Learning | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2507.01006) | [![GitHub Stars](https://img.shields.io/github/stars/zai-org/GLM-V?style=social&label=Star)](https://github.com/zai-org/GLM-V)  |
| 2025.08 | `CX-Mind` | CX-Mind: A Pioneering Multimodal Large Language Model for Interleaved Reasoning in Chest X-ray via Curriculum-Guided Reinforcement Learning | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2508.03733) | [![GitHub Stars](https://img.shields.io/github/stars/SII-WenjieLisjtu/CX-Mind?style=social&label=Star)](https://github.com/SII-WenjieLisjtu/CX-Mind)  |
| 2025.06 | `Lingshu` | Lingshu: A Generalist Foundation Model for Unified Multimodal Medical Understanding and Reasoning | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2506.07044) | [![Hugging Face](https://img.shields.io/badge/🤗%20Model-white?style=flat)](https://huggingface.co/collections/lingshu-medical-mllm/lingshu-mllms) |
| 2025.06 | `MMedAgent-RL` | MMedAgent-RL: Optimizing Multi-Agent Collaboration for Multimodal Medical Reasoning | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2506.00555) | - |

### <a id="32-reward-modeling"></a>3.2 Reward Modeling
Summary of reward modeling in RL-centric LMRMs, organized by reward channel. For each method we report the input modalities, multimodal reasoning characteristics, feedback granularity, optimization target, reward type, evaluation type, initialization, learning algorithm, and tasks.

<table>
  <colgroup>
    <col style="width:22%;"> 
    <col style="width:12%;">
    <col style="width:12%;">
    <col style="width:25%;">
    <col style="width:4%;">
    <col style="width:5%;">
    <col style="width:7%;">
    <col style="width:18%;">
  </colgroup>
  <thead>
    <tr>
      <th>LMRM</th>
      <th>MM Char.</th>
      <th>Gran.</th>
      <th>Target</th>
      <th>RM</th>
      <th>ET</th>
      <th>Init.</th>
      <!-- <th style="width:8%;">Alg.</th> -->
      <th>Tasks</th>
    </tr>
  </thead>
  <tbody>
    <!-- ===================== Verifiable Rewards ===================== -->
    <tr>
      <td colspan="10"><b>Verifiable Rewards</b></td>
    </tr>
    <tr>
      <td colspan="10"><i>Task-Level Correctness</i></td>
    </tr>
    <tr>
      <td><code>Curr-ReFT</code><br>
        <a href="https://arxiv.org/abs/2503.07065">
        <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv"></a>
        <a href="https://github.com/ding523/Curr_REFT">
        <img src="https://img.shields.io/github/stars/divelab/E2H-Reasoning?style=social" alt="Stars"></a></td>
      <td>Ground</td>
      <td>Traj, Field</td>
      <td>Out.-Acc., Spat.-Temp.</td>
      <td>MR</td>
      <td>H</td>
      <td>RL</td>
      <!-- <td>GRPO</td> -->
      <td>Math, Detection, Classification</td>
    </tr>
    <tr>
      <td><code>MedVLThinker</code><br><a href="https://arxiv.org/abs/2508.02669">
        <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv"></a>
        <a href="https://github.com/UCSC-VLAA/MedVLThinker">
        <img src="https://img.shields.io/github/stars/UCSC-VLAA/MedVLThinker?style=social" alt="Stars"></a></td>
      <td>Dom.</td>
      <td>Traj</td>
      <td>Out.-Acc.</td>
      <td>ORM</td>
      <td>R</td>
      <td>SFT+RL</td>
      <!-- <td>GRPO</td> -->
      <td>General-Domain Medical QA, Modality-Specific QA</td>
    </tr>
    <tr>
      <td><code>R1-VL</code><br><a href="https://arxiv.org/abs/2503.12937">
          <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv"></a>
          <a href="https://github.com/jingyi0000/R1-VL">
          <img src="https://img.shields.io/github/stars/jingyi0000/R1-VL?style=social" alt="Stars"></a></td>
        <td>Struct, Dom.</td>
        <td>Step</td>
        <td>Proc.-Acc., Struct-Form</td>
        <td>PRM</td>
        <td>R</td>
        <td>SFT+RL</td>
        <!-- <td>StepGRPO</td> -->
        <td>Chart Rea., Visual Hallucination, Math, General Visual Rea.</td>
    </tr>
    <tr>
      <td><code>GRIT</code><br><a href="https://arxiv.org/abs/2505.15879">
        <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv"></a>
        <a href="https://github.com/eric-ai-lab/GRIT">
        <img src="https://img.shields.io/github/stars/eric-ai-lab/GRIT?style=social" alt="Stars"></a></td>
      <td>Spat., Align, Ground</td>
      <td>Traj, Field, Step</td>
      <td>Struct-Form, Spat.-Temp., Out.-Acc. </td>
      <td>MR</td>
      <td>H</td>
      <td>RL</td>
      <!-- <td>GRPO-GR</td> -->
      <td>Math, Spat. Rea., Object Count.</td>
    </tr>
    <tr>
      <td><code>Kimi k1.5</code><br><a href="https://arxiv.org/abs/2501.12599">
        <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv"></a>
        <a href="https://github.com/MoonshotAI/Kimi-k1.5">
        <img src="https://img.shields.io/github/stars/MoonshotAI/Kimi-k1.5?style=social" alt="Stars"></a></td>
      <td>Spat., Struct, Dom.</td>
      <td>Traj</td>
      <td>Out.-Acc., Struct-Form</td>
      <td>ORM</td>
      <td>H</td>
      <!-- <td>SFT+RL</td> -->
      <td>online PMD</td>
      <td>Math, Code Rea. and Gen., MM Rea., Knowledge and Logical Rea.</td>
    </tr>
    <!-- ===================== Structural Constraints ===================== -->
    <tr>
      <td colspan="10"><i>Structural Constraints</i></td>
    </tr>
    <tr>
      <td><code>Visionary-R1</code><br><a href="https://arxiv.org/abs/2505.14677">
          <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv">
        </a>
        <a href="https://github.com/maifoundations/Visionary-R1">
          <img src="https://img.shields.io/github/stars/maifoundations/Visionary-R1?style=social" alt="Stars">
        </a></td>
      <td>Ground, Align</td>
      <td>Traj, Field</td>
      <td>Out.-Acc., Struct-Form, Align-CM</td>
      <td>ORM</td>
      <td>H</td>
      <td>RL</td>
      <!-- <td>GRPO</td> -->
      <td>Visual Rea., Math, Chart Rea.</td>
    </tr>
    <tr>
      <td><code>Geoint-R1</code><br><a href="https://arxiv.org/abs/2508.03173">
          <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv">
        </a></td>
      <td>Ground, Spat., Struct, Dom.</td>
      <td>Traj, Field</td>
      <td>Out.-Acc., Spat.-Temp., Struct-Form</td>
      <td>ORM</td>
      <td>H</td>
      <td>SFT+RL</td>
      <!-- <td>GRPO</td> -->
      <td>Answer- and Proof-Type Geo QA</td>
    </tr>
    <tr>
      <td><code>R1-SGG</code><br><a href="https://arxiv.org/abs/2504.13617">
          <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv">
        </a>
        <a href="https://github.com/gpt4vision/R1-SGG">
          <img src="https://img.shields.io/github/stars/gpt4vision/R1-SGG?style=social" alt="Stars">
        </a></td>
      <td>Ground, Spat., Struct</td>
      <td>Traj, Field</td>
      <td>Struct-Form</td>
      <td>ORM</td>
      <td>R</td>
      <td>SFT+RL</td>
      <!-- <td>GRPO</td> -->
      <td>Scene Graph Gen. (SGG)</td>
    </tr>
    <tr>
      <td><code>VideoChat-R1</code><br><a href="https://arxiv.org/abs/2504.06958">
          <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv">
        </a>
        <a href="https://github.com/OpenGVLab/VideoChat-R1">
          <img src="https://img.shields.io/github/stars/OpenGVLab/VideoChat-R1?style=social" alt="Stars">
        </a></td>
      <td>Temp., Ground, Spat.</td>
      <td>Traj, Field</td>
      <td>Out.-Acc., Spat.-Temp., Struct-Form</td>
      <td>ORM</td>
      <td>H</td>
      <td>RL</td>
      <!-- <td>GRPO</td> -->
      <td>Video Rea., Temp. Ground, Tracking, Quality Assessment</td>
    </tr>
    <!-- ===================== Domain-Rule Verification ===================== -->
    <tr>
      <td colspan="10"><i>Domain-Rule Verification</i></td>
    </tr>
    <tr>
      <td><code>MetaSpatial</code><br><a href="https://arxiv.org/abs/2503.18470">
          <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv">
        </a>
        <a href="https://github.com/PzySeere/MetaSpatial">
          <img src="https://img.shields.io/github/stars/PzySeere/MetaSpatial?style=social" alt="Stars">
        </a></td>
      <td>Ground, Struct, Dom.</td>
      <td>Traj, Subgoal</td>
      <td>Dom.-Rule, Spat.-Temp., Struct-Form</td>
      <td>PRM</td>
      <td>H</td>
      <td>RL</td>
      <!-- <td>GRPO</td> -->
      <td>3D Spatial Rea.</td>
    </tr>
    <tr>
      <td><code>ChestX-Reasoner</code><br><a href="https://arxiv.org/abs/2504.20930">
          <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv">
        </a>
        <a href="https://github.com/MAGIC-AI4Med/ChestX-Reasoner">
          <img src="https://img.shields.io/github/stars/MAGIC-AI4Med/ChestX-Reasoner?style=social" alt="Stars">
        </a></td>
      <td>Dom., Temp.</td>
      <td>Traj</td>
      <td>Out.-Acc., Proc.-Acc., Struct-Form</td>
      <td>MR</td>
      <td>H</td>
      <td>SFT+RL</td>
      <!-- <td>GRPO</td> -->
      <td>Binary-/Single-/Multi-Disease Diagnosis</td>
    </tr>
    <!-- ===================== Model-Based Automatic Evaluation ===================== -->
    <tr>
      <td colspan="10"><i>Model-Based Automatic Evaluation</i></td>
    </tr>
    <tr>
      <td><code>GoT-R1</code><br><a href="https://arxiv.org/abs/2505.17022">
          <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv">
        </a>
        <a href="https://github.com/gogoduan/GoT-R1">
          <img src="https://img.shields.io/github/stars/gogoduan/GoT-R1?style=social" alt="Stars">
        </a></td>
      <td>Ground, Spat., Align, Struct</td>
      <td>Traj, Field</td>
      <td>Align-CM, Spat.-Temp., Out.-Acc.</td>
      <td>MR</td>
      <td>H</td>
      <td>SFT+RL</td>
      <!-- <td>GRPO</td> -->
      <td>Text-to-Image Gen.</td>
    </tr>
    <tr>
      <td><code>StructVRM</code><br><a href="https://arxiv.org/abs/2508.05383">
          <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv">
        </a></td>
      <td>Struct, Dom.</td>
      <td>Traj</td>
      <td>Out.-Acc., Struct-Form</td>
      <td>PRM</td>
      <td>H</td>
      <td>SFT+RL</td>
      <!-- <td>PPO</td> -->
      <td>Visual QA, Physics, Chemistry, Biology, Math Rea.</td>
    </tr>
    <tr>
      <td><code>DeepEyes</code><br><a href="https://arxiv.org/abs/2505.14362">
          <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv">
        </a>
        <a href="https://github.com/Visual-Agent/DeepEyes">
          <img src="https://img.shields.io/github/stars/Visual-Agent/DeepEyes?style=social" alt="Stars">
        </a></td>
      <td>Ground, Spat.</td>
      <td>Traj, Step</td>
      <td>Out.-Acc., Struct-Form</td>
      <td>ORM</td>
      <td>R</td>
      <td>RL</td>
      <!-- <td>GRPO</td> -->
      <td>Fine-Grained Visual Rea., MM Rea. Math, Grounding and Hallucination</td>
    </tr>
    <!-- ===================== Decomposed Rewards ===================== -->
    <tr>
      <td colspan="10"><i>Decomposed Rewards</i></td>
    </tr>
    <tr>
      <td><code>STAR-R1</code><br><a href="https://arxiv.org/abs/2505.15804">
          <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv">
        </a>
        <a href="https://github.com/zongzhao23/STAR-R1">
          <img src="https://img.shields.io/github/stars/zongzhao23/STAR-R1?style=social" alt="Stars">
        </a></td>
      <td>Spat., Ground</td>
      <td>Traj, Field</td>
      <td>Out.-Acc., Struct-Form</td>
      <td>PRM</td>
      <td>R</td>
      <td>RL</td>
      <!-- <td>GRPO</td> -->
      <td>Spatial Transformation Rea.</td>
    </tr>
    <tr>
      <td><code>DanceGRPO</code><br><a href="https://arxiv.org/abs/2505.07818">
          <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv">
        </a>
        <a href="https://github.com/XueZeyue/DanceGRPO">
          <img src="https://img.shields.io/github/stars/XueZeyue/DanceGRPO?style=social" alt="Stars">
        </a></td>
      <td>Align, Temp., Dom.</td>
      <td>Traj</td>
      <td>Pref-Qual, Align-CM, Dom.-Rule, Out.-Acc.</td>
      <td>ORM</td>
      <td>H</td>
      <td>RL</td>
      <!-- <td>GRPO</td> -->
      <td>Text-to-Image, Video Gen.</td>
    </tr>
    <tr>
      <td><code>TimeMaster</code><br><a href="https://arxiv.org/abs/2506.13705">
          <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv">
        </a>
        <a href="https://github.com/langfengQ/TimeMaster">
          <img src="https://img.shields.io/github/stars/langfengQ/TimeMaster?style=social" alt="Stars">
        </a></td>
      <td>Temp., Struct, Dom.</td>
      <td>Traj</td>
      <td>Out.-Acc., Struct-Form, Dom.-Rule</td>
      <td>ORM</td>
      <td>H</td>
      <td>SFT+RL</td>
      <!-- <td>GRPO</td> -->
      <td>MM Time-Series Rea.</td>
    </tr>
    <tr>
      <td><code>Mixed-R1</code><br><a href="https://arxiv.org/abs/2505.24164">
          <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv">
        </a></td>
      <td>Ground, Align, Spat.</td>
      <td>Traj, Field</td>
      <td>Out.-Acc., Struct-Form, Spat.-Temp., Align-CM</td>
      <td>ORM</td>
      <td>R</td>
      <td>SFT+RL</td>
      <!-- <td>GRPO</td> -->
      <td>Math, Science, Chart/OCR Rea., Fine-Grained Visual Rea.</td>
    </tr>
    <tr>
      <td><code>Relation-R1</code><br><a href="https://arxiv.org/abs/2504.14642">
          <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv">
        </a>
        <a href="https://github.com/HKUST-LongGroup/Relation-R1">
          <img src="https://img.shields.io/github/stars/HKUST-LongGroup/Relation-R1?style=social" alt="Stars">
        </a></td>
      <td>Ground, Spat., Struct, Dom.</td>
      <td>Traj, Field</td>
      <td>Spat.-Temp., Out.-Acc., Struct-Form</td>
      <td>ORM</td>
      <td>R</td>
      <td>SFT+RL</td>
      <!-- <td>GRPO</td> -->
      <td>Binary Relation Detection (SGG), N-ary Relation Rea.</td>
    </tr>
    <!-- ===================== Human Feedback Rewards ===================== -->
    <tr>
      <td colspan="10"><b>Human Feedback Rewards</b></td>
    </tr>
    <tr>
      <td colspan="10"><i>Direct Human Preference</i></td>
    </tr>
    <tr>
      <td><code>T2I-R1</code><br><a href="https://arxiv.org/abs/2505.00703">
          <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv">
        </a>
        <a href="https://github.com/CaraJ7/T2I-R1">
          <img src="https://img.shields.io/github/stars/CaraJ7/T2I-R1?style=social" alt="Stars">
        </a></td>
      <td>Align, Spat., Ground, Dom.</td>
      <td>Traj, Field</td>
      <td>Pref-Qual, Out.-Acc., Align-CM, Spat.-Temp.</td>
      <td>ORM</td>
      <td>M</td>
      <td>RL</td>
      <!-- <td>BiCoT-GRPO</td> -->
      <td>Text-to-Image Gen. with Human Preference Alignment</td>
    </tr>
    <tr>
      <td><code>SophiaVL-R1</code><br><a href="https://arxiv.org/abs/2505.17018">
          <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv">
        </a>
        <a href="https://github.com/kxfan2002/SophiaVL-R1">
          <img src="https://img.shields.io/github/stars/kxfan2002/SophiaVL-R1?style=social" alt="Stars">
        </a></td>
      <td>Spat., Dom.</td>
      <td>Traj, Step</td>
      <td>Struct-Form, Out.-Acc.</td>
      <td>MR</td>
      <td>H</td>
      <td>RL</td>
      <!-- <td>Trust-GRPO</td> -->
      <td>Math, Science, Visual Rea., Chart Rea., General MM QA</td>
    </tr>
    <tr>
      <td><code>Generative RLHF-V</code><br><a href="https://arxiv.org/abs/2505.18531">
          <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv">
        </a>
        <a href="https://github.com/volcengine/verl">
          <img src="https://img.shields.io/github/stars/volcengine/verl?style=social" alt="Stars">
        </a></td>
      <td>Align, Dom.</td>
      <td>Traj</td>
      <td>Pref-Qual, Out.-Acc.</td>
      <td>ORM</td>
      <td>M</td>
      <td>RL</td>
      <!-- <td>GRPO</td> -->
      <td>General MM Res.</td>
    </tr>
    <tr>
      <td><code>SaFeR-VLM</code><br><a href="https://arxiv.org/abs/2510.06871">
          <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv">
        </a>
        <a href="https://github.com/HarveyYi/SaFeR-VLM">
          <img src="https://img.shields.io/github/stars/HarveyYi/SaFeR-VLM?style=social" alt="Stars">
        </a></td>
      <td>Align, Dom.</td>
      <td>Traj</td>
      <td>Pref-Qual, Out.-Acc.</td>
      <td>ORM</td>
      <td>H</td>
      <td>SFT+RL</td>
      <!-- <td>GRPO</td> -->
      <td>Safety-Aware MM Rea.</td>
    </tr>
    <!-- ===================== Mixture-of-Rewards ===================== -->
     <tr>
      <td colspan="10"><i>Mixture-of-Rewards</i></td>
    </tr>
    <tr>
      <td><code>Intern-S1</code><br><a href="https://arxiv.org/abs/2508.15763">
          <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv">
        </a>
        <a href="https://github.com/InternLM/Intern-S1">
          <img src="https://img.shields.io/github/stars/InternLM/Intern-S1?style=social" alt="Stars">
        </a></td>
      <td>Dom., Struct, Align</td>
      <td>Traj, Field</td>
      <td>Out.-Acc., Struct-Form, Align-CM</td>
      <td>MR</td>
      <td>H</td>
      <td>SFT+RL</td>
      <!-- <td>OREAL</td> -->
      <td>Science, Instruction Following, MM Rea., Interdisciplinary QA</td>
    </tr>
  </tbody>
</table>

> **Abbreviations.**
(1) **MM Char.**: *Ground* = structured visual grounding (*e.g.*, boxes, masks, counting), *Spat.* = spatial relations, *Temp.* = temporal or time-series reasoning, *Struct* = structured outputs (*e.g.*, tables, JSON, scene graphs), *Dom.* = domain priors (*e.g.*, physics, medicine), *Align* = cross-modal alignment. 
(2) **Gran.**: *Traj* = trajectory-level, only one reward for the entire reasoning chain, *Step* = step-level (score each reasoning step or intermediate action), *Field* = field-level or token-level, check each field or coordinate in the answer one by one, *Subgoal* = subgoal-level, decompose reasoning subtasks, regions, or time slices.
(3) **Target**: *Out.-Acc.* = final-answer or task accuracy, *Proc.-Acc.* = correctness of intermediate reasoning steps, *Struct-Form* = format, syntax, or structural validity, *Spat.-Temp.* = spatial or temporal consistency, *Dom.-Rule* = satisfaction of domain rules (*e.g.*, physics, medical, safety constraints), *Align-CM* = cross-modal alignment scores, *Pref-Qual* = human preference or quality (helpfulness, fluency).  
(4) **RM (Reward Model)**: ORM = outcome reward model, PRM = process reward model, MR = mixed reward model.
(5) **ET (Evalation Type)**: *R* = rule-based rewards, *M* = model-based rewards, *H* = hybrid rewards.
(6) **Init.**: initialization strategy (RL from scratch vs. SFT+RL).




### <a id="train-33-trajectory-sampling"></a>3.3 Trajectory Sampling

Sampling governs how the policy generates reasoning trajectories for exploration and learning. Multimodal reasoning often requires explicit control over diversity, reasoning depth, task adaptability, and input distribution coverage. We group training-time trajectory sampling into four strategies:

:one: **Group Sampling & Rejection Sampling**: sample multiple trajectories per iteration; select high-advantage samples and optionally filter low-quality ones with external verifiers.


[Kimi k1.5: Scaling Reinforcement Learning with LLMs](https://arxiv.org/abs/2501.12599) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2501.12599) [![GitHub Stars](https://img.shields.io/github/stars/MoonshotAI/Kimi-k1.5?style=social&label=Star)](https://github.com/MoonshotAI/Kimi-k1.5)

[MedVLM-R1: Incentivizing Medical Reasoning Capability of Vision-Language Models (VLMs) via Reinforcement Learning](https://arxiv.org/abs/2502.19634) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2502.19634) [![GitHub Stars](https://img.shields.io/github/stars/JZPeterPan/MedVLM-R1?style=social&label=Star)](https://github.com/JZPeterPan/MedVLM-R1)



:two: **Fine-grained Sampling**: reuse and revise high-reward trajectories via mandatory rethinking / self-reflection to deepen reasoning chains.

[VL-Rethinker: Incentivizing Self-Reflection of Vision-Language Models with Reinforcement Learning](https://arxiv.org/abs/2504.08837) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2504.08837) [![GitHub Stars](https://img.shields.io/github/stars/TIGER-AI-Lab/VL-Rethinker?style=social&label=Star)](https://github.com/TIGER-AI-Lab/VL-Rethinker)

[Skywork R1V2: Multimodal Hybrid Reinforcement Learning for Reasoning](https://arxiv.org/abs/2504.16656) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2504.16656) [![GitHub Stars](https://img.shields.io/github/stars/SkyworkAI/Skywork-R1V?style=social&label=Star)](https://github.com/SkyworkAI/Skywork-R1V)

[GoT-R1: Unleashing Reasoning Capability of MLLM for Visual Generation with Reinforcement Learning](https://arxiv.org/abs/2505.17022) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.17022) [![GitHub Stars](https://img.shields.io/github/stars/gogoduan/GoT-R1?style=social&label=Star)](https://github.com/gogoduan/GoT-R1)

:three: **Dynamic Sampling**: adapt trajectory length/complexity to task difficulty; retain effective-gradient samples to improve stability and efficiency.

[Seed1.5-Thinking: Advancing Superb Reasoning Models with Reinforcement Learning](https://arxiv.org/abs/2504.13914) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2504.13914) [![GitHub Stars](https://img.shields.io/github/stars/ByteDance-Seed/Seed-Thinking-v1.5?style=social&label=Star)](https://github.com/ByteDance-Seed/Seed-Thinking-v1.5)

[Boosting the Generalization and Reasoning of Vision Language Models with Curriculum Reinforcement Learning](https://arxiv.org/abs/2503.07065) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.07065) [![GitHub Stars](https://img.shields.io/github/stars/ding523/Curr_REFT?style=social&label=Star)](https://github.com/ding523/Curr_REFT)

[Fast-Slow Thinking GRPO for Large Vision-Language Model Reasoning](https://arxiv.org/abs/2504.18458) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2504.18458) [![GitHub Stars](https://img.shields.io/github/stars/Mr-Loevan/FAST?style=social&label=Star)](https://github.com/Mr-Loevan/FAST)

[GuardReasoner-VL: Safeguarding VLMs via Reinforced Reasoning](https://arxiv.org/abs/2505.11049) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.11049) [![GitHub Stars](https://img.shields.io/github/stars/yueliu1999/GuardReasoner-VL?style=social&label=Star)](https://github.com/yueliu1999/GuardReasoner-VL)

:four: **Cross-modal Input Sampling**: extend sampling from text to visual inputs (*e.g.*, frame selection/subsampling) to control context length and computation.

[Omni-R1: Reinforcement Learning for Omnimodal Reasoning via Two-System Collaboration](https://arxiv.org/abs/2505.20256) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.20256) [![GitHub Stars](https://img.shields.io/github/stars/aim-uofa/Omni-R1?style=social&label=Star)](https://github.com/aim-uofa/Omni-R1)

[Seed1.5-VL Technical Report](https://arxiv.org/abs/2505.07062) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.07062) [![GitHub Stars](https://img.shields.io/github/stars/ByteDance-Seed/Seed1.5-VL?style=social&label=Star)](https://github.com/ByteDance-Seed/Seed1.5-VL)


### <a id="train-34-modal-alignment--learning-algorithm"></a>3.4 Modal Alignment & Learning Algorithm

This section focuses on *how* RL-centric LMRMs maintain cross-modal consistency during reasoning and *how* the policy is optimized. We view **cross-modal alignment** as the behavior generation mechanism under multimodal observations, and **training optimization strategies** as the update rules refining this policy. Together, they determine whether System-2 reasoning can generalize stably across modalities and tasks.

<p align="center">
  <img src="figures\alignment.png" width="80%" />
<!--   <img src="./Images/methods.jpg" width="45%" height="50%" /> -->
</p>

#### 3.4.1 Modal Alignment

(1) **Data-level alignment**: regulate input distribution via ① multimodal data construction (paired or interleaved), ② augmentation, and ③ modality transformation (*e.g.*, I2T textualization).  

:diamond_shape_with_a_dot_inside: [VLM-R1: A Stable and Generalizable R1-style Large Vision-Language Model](https://arxiv.org/abs/2504.07615) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2504.07615) [![GitHub Stars](https://img.shields.io/github/stars/om-ai-lab/VLM-R1?style=social&label=Star)](https://github.com/om-ai-lab/VLM-R1)

:diamond_shape_with_a_dot_inside: [Infi-MMR: Curriculum-based Unlocking Multimodal Reasoning via Phased Reinforcement Learning in Multimodal Small Language Models](https://arxiv.org/abs/2505.23091) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.23091) [![GitHub Stars](https://img.shields.io/github/stars/Reallm-Labs/Infi-MMR?style=social&label=Star)](https://github.com/Reallm-Labs/Infi-MMR)

:diamond_shape_with_a_dot_inside: [R1-ShareVL: Incentivizing Reasoning Capability of Multimodal Large Language Models via Share-GRPO](https://arxiv.org/abs/2505.16673) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.16673) [![GitHub Stars](https://img.shields.io/github/stars/HJYao00/R1-ShareVL?style=social&label=Star)](https://github.com/HJYao00/R1-ShareVL)

:diamond_shape_with_a_dot_inside: [C2-Evo: Co-Evolving Multimodal Data and Model for Self-Improving Reasoning](https://arxiv.org/abs/2507.16518) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2507.16518) [![GitHub Stars](https://img.shields.io/github/stars/chen-xw/C2-Evo?style=social&label=Star)](https://github.com/chen-xw/C2-Evo)

:diamond_shape_with_a_dot_inside: [Vision-R1: Incentivizing Reasoning Capability in Multimodal Large Language Models](https://arxiv.org/abs/2503.06749) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.06749) [![GitHub Stars](https://img.shields.io/github/stars/Osilly/Vision-R1?style=social&label=Star)](https://github.com/Osilly/Vision-R1)

:diamond_shape_with_a_dot_inside: [R2-MultiOmnia: Leading Multilingual Multimodal Reasoning via Self-Training](https://aclanthology.org/2025.acl-long.402/) [![Paper](https://img.shields.io/badge/ACL-b31b1b.svg)](https://aclanthology.org/2025.acl-long.402/)

:diamond_shape_with_a_dot_inside: [Visionary-R1: Mitigating Shortcuts in Visual Reasoning with Reinforcement Learning](https://arxiv.org/abs/2505.14677) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.14677) [![GitHub Stars](https://img.shields.io/github/stars/maifoundations/Visionary-R1?style=social&label=Star)](https://github.com/maifoundations/Visionary-R1)

:diamond_shape_with_a_dot_inside: [R1-Onevision: Advancing Generalized Multimodal Reasoning through Cross-Modal Formalization](https://arxiv.org/abs/2503.10615) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.10615) [![GitHub Stars](https://img.shields.io/github/stars/Fancy-MLLM/R1-Onevision?style=social&label=Star)](https://github.com/Fancy-MLLM/R1-Onevision)

:diamond_shape_with_a_dot_inside: [MathCoder-VL: Bridging Vision and Code for Enhanced Multimodal Mathematical Reasoning](https://arxiv.org/abs/2505.10557) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.10557) [![GitHub Stars](https://img.shields.io/github/stars/mathllm/MathCoder?style=social&label=Star)](https://github.com/mathllm/MathCoder)




(2) **Model-level alignment**: integrate heterogeneous signals into the reasoning policy via ① adapters & projection layers, ② visual tools-based alignment, and ③ grounding tools-based alignment for evidence-faithful reasoning.

:diamond_shape_with_a_dot_inside: [Skywork R1V2: Multimodal Hybrid Reinforcement Learning for Reasoning](https://arxiv.org/abs/2504.16656) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2504.16656) [![GitHub Stars](https://img.shields.io/github/stars/SkyworkAI/Skywork-R1V?style=social&label=Star)](https://github.com/SkyworkAI/Skywork-R1V)

:diamond_shape_with_a_dot_inside: [Skywork R1V: Pioneering Multimodal Reasoning with Chain-of-Thought](https://arxiv.org/abs/2504.05599) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2504.05599) [![GitHub Stars](https://img.shields.io/github/stars/SkyworkAI/Skywork-R1V?style=social&label=Star)](https://github.com/SkyworkAI/Skywork-R1V)

:diamond_shape_with_a_dot_inside: [Skywork-R1V3 Technical Report](https://arxiv.org/abs/2507.06167) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2507.06167) [![GitHub Stars](https://img.shields.io/github/stars/SkyworkAI/Skywork-R1V?style=social&label=Star)](https://github.com/SkyworkAI/Skywork-R1V)

:diamond_shape_with_a_dot_inside: [MiMo-VL Technical Report](https://arxiv.org/abs/2506.03569) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2506.03569) [![GitHub Stars](https://img.shields.io/github/stars/XiaomiMiMo/MiMo-VL?style=social&label=Star)](https://github.com/XiaomiMiMo/MiMo-VL)

:diamond_shape_with_a_dot_inside: [Kimi-VL Technical Report](https://arxiv.org/abs/2504.07491) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2504.07491) [![GitHub Stars](https://img.shields.io/github/stars/MoonshotAI/Kimi-VL?style=social&label=Star)](https://github.com/MoonshotAI/Kimi-VL)

:diamond_shape_with_a_dot_inside: [Seed1.5-VL Technical Report](https://arxiv.org/abs/2505.07062) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.07062) [![GitHub Stars](https://img.shields.io/github/stars/ByteDance-Seed/Seed1.5-VL?style=social&label=Star)](https://github.com/ByteDance-Seed/Seed1.5-VL)

:diamond_shape_with_a_dot_inside: [From Answers to Rationales: Self-Aligning Multimodal Reasoning with Answer-Oriented Chain-of-Thought](https://arxiv.org/abs/2507.02984) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2507.02984) [![GitHub Stars](https://img.shields.io/github/stars/WentaoTan/SMART?style=social&label=Star)](https://github.com/WentaoTan/SMART)

:diamond_shape_with_a_dot_inside: [Embodied-R: Collaborative Framework for Activating Embodied Spatial Reasoning in Foundation Models via Reinforcement Learning](https://arxiv.org/abs/2504.12680) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2504.12680) [![GitHub Stars](https://img.shields.io/github/stars/EmbodiedCity/Embodied-R.code?style=social&label=Star)](https://github.com/EmbodiedCity/Embodied-R.code)

:diamond_shape_with_a_dot_inside: [DeepEyes: Incentivizing "Thinking with Images" via Reinforcement Learning](https://arxiv.org/abs/2505.14362) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.14362) [![GitHub Stars](https://img.shields.io/github/stars/Visual-Agent/DeepEyes?style=social&label=Star)](https://github.com/Visual-Agent/DeepEyes)

:diamond_shape_with_a_dot_inside: [Chain-of-Focus: Adaptive Visual Search and Zooming for Multimodal Reasoning via RL](https://arxiv.org/abs/2505.15436v1) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.15436v1) [![GitHub Stars](https://img.shields.io/github/stars/xtong-zhang/Chain-of-Focus?style=social&label=Star)](https://github.com/xtong-zhang/Chain-of-Focus)

:diamond_shape_with_a_dot_inside: [GFlowVLM: Enhancing Multi-step Reasoning in Vision-Language Models with Generative Flow Networks](https://arxiv.org/abs/2503.06514) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.06514)

:diamond_shape_with_a_dot_inside: [Point-RFT: Improving Multimodal Reasoning with Visually Grounded Reinforcement Finetuning](https://arxiv.org/abs/2505.19702) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.19702)

:diamond_shape_with_a_dot_inside: [VLM-R$^3$: Region Recognition, Reasoning, and Refinement for Enhanced Multimodal Chain-of-Thought](https://arxiv.org/abs/2505.16192) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.16192)




#### 3.4.2 Learning Algorithm

(1) **Basic Algorithms**

- **PPO**

:diamond_shape_with_a_dot_inside: [Seed1.5-VL Technical Report](https://arxiv.org/abs/2505.07062) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.07062) [![GitHub Stars](https://img.shields.io/github/stars/ByteDance-Seed/Seed1.5-VL?style=social&label=Star)](https://github.com/ByteDance-Seed/Seed1.5-VL)

:diamond_shape_with_a_dot_inside: [LMM-R1: Empowering 3B LMMs with Strong Reasoning Abilities Through Two-Stage Rule-Based RL](https://arxiv.org/abs/2503.07536) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.07536) [![GitHub Stars](https://img.shields.io/github/stars/TideDra/lmm-r1?style=social&label=Star)](https://github.com/TideDra/lmm-r1)

- **DPO**

:diamond_shape_with_a_dot_inside: [VisRL: Intention-Driven Visual Perception via Reinforced Reasoning](https://arxiv.org/abs/2503.07523) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.07523) [![GitHub Stars](https://img.shields.io/github/stars/zhangquanchen/VisRL?style=social&label=Star)](https://github.com/zhangquanchen/VisRL)

:diamond_shape_with_a_dot_inside: [video-SALMONN-o1: Reasoning-enhanced Audio-visual Large Language Model](https://arxiv.org/abs/2502.11775) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2502.11775) [![GitHub Stars](https://img.shields.io/github/stars/BriansIDP/video-SALMONN-o1?style=social&label=Star)](https://github.com/BriansIDP/video-SALMONN-o1)

- **GRPO**

:diamond_shape_with_a_dot_inside: [Seg-Zero: Reasoning-Chain Guided Segmentation via Cognitive Reinforcement]() [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)]() [![GitHub Stars](https://img.shields.io/github/stars/JIA-Lab-research/Seg-Zero?style=social&label=Star)](https://github.com/JIA-Lab-research/Seg-Zero)

:diamond_shape_with_a_dot_inside: [VisionReasoner: Unified Reasoning-Integrated Visual Perception via Reinforcement Learning](https://arxiv.org/abs/2505.12081) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.12081) [![GitHub Stars](https://img.shields.io/github/stars/JIA-Lab-research/VisionReasoner?style=social&label=Star)](https://github.com/JIA-Lab-research/VisionReasoner)

:diamond_shape_with_a_dot_inside: [Reinforcement Learning Outperforms Supervised Fine-Tuning: A Case Study on Audio Question Answering](https://arxiv.org/abs/2503.11197) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.11197) [![GitHub Stars](https://img.shields.io/github/stars/xiaomi-research/r1-aqa?style=social&label=Star)](https://github.com/xiaomi-research/r1-aqa)

(1) <b>GRPO-based enhancements for efficiency and stability</b>

:diamond_shape_with_a_dot_inside: [Fast-Slow Thinking for Large Vision-Language Model Reasoning](https://arxiv.org/abs/2504.13055) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2504.13055) [![GitHub Stars](https://img.shields.io/github/stars/Mr-Loevan/FAST?style=social&label=Star)](https://github.com/Mr-Loevan/FAST)

:diamond_shape_with_a_dot_inside: [Skywork R1V2: Multimodal Hybrid Reinforcement Learning for Reasoning](https://arxiv.org/abs/2504.16656) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2504.16656) [![GitHub Stars](https://img.shields.io/github/stars/SkyworkAI/Skywork-R1V?style=social&label=Star)](https://github.com/SkyworkAI/Skywork-R1V)

:diamond_shape_with_a_dot_inside: [GRIT: Teaching MLLMs to Think with Images](https://arxiv.org/abs/2505.15879) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.15879) [![GitHub Stars](https://img.shields.io/github/stars/eric-ai-lab/GRIT?style=social&label=Star)](https://github.com/eric-ai-lab/GRIT)

:diamond_shape_with_a_dot_inside: [R1-VL: Learning to Reason with Multimodal Large Language Models via Step-wise Group Relative Policy Optimization](https://arxiv.org/abs/2503.12937) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.12937) [![GitHub Stars](https://img.shields.io/github/stars/jingyi0000/R1-VL?style=social&label=Star)](https://github.com/jingyi0000/R1-VL)

:diamond_shape_with_a_dot_inside: [OmniQuality-R: Advancing Reward Models Through All-Encompassing Quality Assessment](https://arxiv.org/abs/2510.10609) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2510.10609) [![GitHub Stars](https://img.shields.io/github/stars/yeppp27/OmniQuality-R?style=social&label=Star)](https://github.com/yeppp27/OmniQuality-R)

:diamond_shape_with_a_dot_inside: [R1-ShareVL: Incentivizing Reasoning Capability of Multimodal Large Language Models via Share-GRPO](https://arxiv.org/abs/2505.16673) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.16673) [![GitHub Stars](https://img.shields.io/github/stars/HJYao00/R1-ShareVL?style=social&label=Star)](https://github.com/HJYao00/R1-ShareVL)

:diamond_shape_with_a_dot_inside: [T2I-R1: Reinforcing Image Generation with Collaborative Semantic-level and Token-level CoT](https://arxiv.org/abs/2505.00703) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.00703) [![GitHub Stars](https://img.shields.io/github/stars/CaraJ7/T2I-R1?style=social&label=Star)](https://github.com/CaraJ7/T2I-R1) 



(2) <b>Reasoning-aware strategies for consistency and process optimization</b>

:diamond_shape_with_a_dot_inside: [SophiaVL-R1: Reinforcing MLLMs Reasoning with Thinking Reward](https://arxiv.org/abs/2505.17018) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.17018) [![GitHub Stars](https://img.shields.io/github/stars/kxfan2002/SophiaVL-R1?style=social&label=Star)](https://github.com/kxfan2002/SophiaVL-R1) 

:diamond_shape_with_a_dot_inside: [GRPO-CARE: Consistency-Aware Reinforcement Learning for Multimodal Reasoning](https://arxiv.org/abs/2506.16141) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2506.16141) [![GitHub Stars](https://img.shields.io/github/stars/TencentARC/GRPO-CARE?style=social&label=Star)](https://github.com/TencentARC/GRPO-CARE) 

:diamond_shape_with_a_dot_inside: [Perception-Consistency Multimodal Large Language Models Reasoning via Caption-Regularized Policy Optimization](https://arxiv.org/abs/2509.21854) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2509.21854)

:diamond_shape_with_a_dot_inside: [VLM-R$^3$: Region Recognition, Reasoning, and Refinement for Enhanced Multimodal Chain-of-Thought](https://arxiv.org/abs/2505.16192) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.16192)

:diamond_shape_with_a_dot_inside: [Video-R1: Reinforcing Video Reasoning in MLLMs](https://arxiv.org/abs/2503.21776) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.21776) [![GitHub Stars](https://img.shields.io/github/stars/tulerfeng/Video-R1?style=social&label=Star)](https://github.com/tulerfeng/Video-R1) 

:diamond_shape_with_a_dot_inside: [MetaSpatial: Reinforcing 3D Spatial Reasoning in VLMs for the Metaverse](https://arxiv.org/abs/2503.18470) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.18470) [![GitHub Stars](https://img.shields.io/github/stars/PzySeere/MetaSpatial?style=social&label=Star)](https://github.com/PzySeere/MetaSpatial) 

:diamond_shape_with_a_dot_inside: [OThink-MR1: Stimulating multimodal generalized reasoning capabilities via dynamic reinforcement learning](https://arxiv.org/abs/2503.16081) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.16081)

:diamond_shape_with_a_dot_inside: [Visionary-R1: Mitigating Shortcuts in Visual Reasoning with Reinforcement Learning](https://arxiv.org/abs/2505.14677) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.14677) [![GitHub Stars](https://img.shields.io/github/stars/maifoundations/Visionary-R1?style=social&label=Star)](https://github.com/maifoundations/Visionary-R1)

:diamond_shape_with_a_dot_inside: [GuardReasoner-VL: Safeguarding VLMs via Reinforced Reasoning](https://arxiv.org/abs/2505.11049) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.11049) [![GitHub Stars](https://img.shields.io/github/stars/yueliu1999/GuardReasoner-VL?style=social&label=Star)](https://github.com/yueliu1999/GuardReasoner-VL)

:diamond_shape_with_a_dot_inside: [One RL to See Them All: Visual Triple Unified Reinforcement Learning](https://arxiv.org/abs/2505.18129) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.18129) [![GitHub Stars](https://img.shields.io/github/stars/MiniMax-AI/One-RL-to-See-Them-All?style=social&label=Star)](https://github.com/MiniMax-AI/One-RL-to-See-Them-All) 

:diamond_shape_with_a_dot_inside: [Improved Visual-Spatial Reasoning via R1-Zero-Like Training](https://arxiv.org/abs/2504.00883) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2504.00883) [![GitHub Stars](https://img.shields.io/github/stars/zhijie-group/R1-Zero-VSI?style=social&label=Star)](https://github.com/zhijie-group/R1-Zero-VSI) 

(3) <b>Hybrid and alternative strategy</b>

:diamond_shape_with_a_dot_inside: [VerIPO: Cultivating Long Reasoning in Video-LLMs via Verifier-Gudied Iterative Policy Optimization](https://arxiv.org/abs/2505.19000) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.19000) [![GitHub Stars](https://img.shields.io/github/stars/HITsz-TMG/VerIPO?style=social&label=Star)](https://github.com/HITsz-TMG/VerIPO) 

:diamond_shape_with_a_dot_inside: [Vision-R1: Incentivizing Reasoning Capability in Multimodal Large Language Models](https://arxiv.org/abs/2503.06749) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.06749) [![GitHub Stars](https://img.shields.io/github/stars/Osilly/Vision-R1?style=social&label=Star)](https://github.com/Osilly/Vision-R1)

:diamond_shape_with_a_dot_inside: [MAPO: Mixed Advantage Policy Optimization](https://arxiv.org/abs/2509.18849) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2509.18849) [![GitHub Stars](https://img.shields.io/github/stars/WenkeHuang/MAPO?style=social&label=Star)](https://github.com/WenkeHuang/MAPO) 

:diamond_shape_with_a_dot_inside: [Perception-Aware Policy Optimization for Multimodal Reasoning](https://arxiv.org/abs/2507.06448) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2507.06448) [![GitHub Stars](https://img.shields.io/github/stars/MikeWangWZHL/PAPO?style=social&label=Star)](https://github.com/MikeWangWZHL/PAPO) 

:diamond_shape_with_a_dot_inside: [Kwai Keye-VL Technical Report](https://arxiv.org/abs/2507.01949) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2507.01949) [![GitHub Stars](https://img.shields.io/github/stars/Kwai-Keye/Keye?style=social&label=Star)](https://github.com/Kwai-Keye/Keye) 


## 4. Test-time Inference of RL-centric Multimodal Reasoning
### <a id="41-sampling"></a>4.1 Sampling

Test-time decoding and sampling strategies strongly influence the coherence and diversity of reasoning outputs. The objective is to explore the solution space efficiently under a limited compute budget and generate high-quality candidate outputs.
Common strategies include [greedy decoding](https://arxiv.org/abs/1409.0473), random sampling, [Top-k](https://arxiv.org/abs/1805.04833), [Top-p](https://arxiv.org/abs/1904.09751), and [beam search](https://arxiv.org/abs/1409.3215).

:o: **Multimodal-specific bottleneck**

Sampling is no longer confined to language tokens. It must also account for visual tokens and cross-modal interaction states. Consequently, the output shifts from a text sequence to a cross-modally consistent reasoning trajectory.


:no_entry_sign: **Limitation** 

(1) Deterministic decoding incurs substantially higher cost and exhibits greater instability in multimodal settings.

:diamond_shape_with_a_dot_inside: [MLLM can see? Dynamic Correction Decoding for Hallucination Mitigation](https://arxiv.org/abs/2410.11779) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2410.11779) [![GitHub Stars](https://img.shields.io/github/stars/zjunlp/DeCo?style=social&label=Star)](https://github.com/zjunlp/DeCo) 

:diamond_shape_with_a_dot_inside: [Curing Semantic Drift: A Dynamic Approach to Grounding Generation in Large Vision-Language Models](https://arxiv.org/abs/2506.21509v3) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2506.21509v3) [![GitHub Stars](https://img.shields.io/github/stars/JiaheChen2002/DLC?style=social&label=Star)](https://github.com/JiaheChen2002/DLC) 

(2) It is difficult to calibrate random-sampling thresholds consistently in multimodal settings.

:diamond_shape_with_a_dot_inside: [Assessing Diversity Collapse in Reasoning](https://openreview.net/forum?id=AMiKsHLjQh) [![Paper](https://img.shields.io/badge/ICLRW-green.svg)](https://openreview.net/forum?id=AMiKsHLjQh)

:diamond_shape_with_a_dot_inside: [AgentCPM-GUI: Building Mobile-Use Agents with Reinforcement Fine-Tuning](https://arxiv.org/abs/2506.01391) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2506.01391) [![GitHub Stars](https://img.shields.io/github/stars/OpenBMB/AgentCPM-GUI?style=social&label=Star)](https://github.com/OpenBMB/AgentCPM-GUI) 

Existing methods still primarily rely on likelihood-driven generation and lack test-time alignment constraints, making them prone to hallucinations that are linguistically plausible yet visually incorrect.

:round_pushpin: **Improvement direction**

Incorporating RL reward signals enables reinforcement feedback for candidate trajectories (*e.g.*, correctness, vision–language and temporal consistency, and safety), thereby dynamically reshaping the sampling distribution and prioritizing high-value trajectories, particularly on difficult cases or in uncertain regions. This shift moves TTI from probability-driven to constraint-guided generation. 

Highlight an open question: rather than relying on single-modality heuristics, we need a slow thinking strategy that can adaptively define the sampling space and state representation based on the joint multimodal distribution.

:diamond_shape_with_a_dot_inside: [Rethinking the Sampling Criteria in Reinforcement Learning for LLM Reasoning: A Competence-Difficulty Alignment Perspective](https://arxiv.org/abs/2505.17652) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.17652)

:diamond_shape_with_a_dot_inside: [LlamaV-o1: Rethinking Step-by-step Visual Reasoning in LLMs](https://arxiv.org/abs/2501.06186) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2501.06186) [![GitHub Stars](https://img.shields.io/github/stars/mbzuai-oryx/LlamaV-o1?style=social&label=Star)](https://github.com/mbzuai-oryx/LlamaV-o1) 

:diamond_shape_with_a_dot_inside: [LLaVA-CoT: Let Vision Language Models Reason Step-by-Step](https://arxiv.org/abs/2411.10440) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2411.10440) [![GitHub Stars](https://img.shields.io/github/stars/PKU-YuanGroup/LLaVA-CoT?style=social&label=Star)](https://github.com/PKU-YuanGroup/LLaVA-CoT) 

### <a id="test-42-search"></a>4.2 Search

Relative to sampling-based generation, search-based methods improve multimodal reasoning at test time by actively maintaining candidate branches and iteratively refining them, continually selecting higher-quality paths from the pool of sampled trajectories. Such methods can be broadly grouped into three categories: parallel search, sequential search, and structured search.

(1) **Parallel search** — diversity mitigates single-trajectory bias

Parallel search explores multiple candidate trajectories concurrently and selects the final answer via voting or scoring, thereby increasing the likelihood of recovering the correct solution. 


:diamond_shape_with_a_dot_inside: [Self-Consistency Improves Chain of Thought Reasoning in Language Models](https://arxiv.org/abs/2203.11171) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2203.11171)

:diamond_shape_with_a_dot_inside: [Rewarding Curse: Analyze and Mitigate Reward Modeling Issues for LLM Reasoning](https://arxiv.org/abs/2503.05188) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.05188)

:diamond_shape_with_a_dot_inside: [Not All Votes Count! Programs as Verifiers Improve Self-Consistency of Language Models for Math Reasoning](https://arxiv.org/abs/2410.12608) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2410.12608) [![GitHub Stars](https://img.shields.io/github/stars/declare-lab/prove?style=social&label=Star)](https://github.com/declare-lab/prove)

:diamond_shape_with_a_dot_inside: [Efficient Test-Time Scaling via Self-Calibration](https://arxiv.org/abs/2503.00031) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.00031) [![GitHub Stars](https://img.shields.io/github/stars/Chengsong-Huang/Self-Calibration?style=social&label=Star)](https://github.com/Chengsong-Huang/Self-Calibration)

:diamond_shape_with_a_dot_inside: [Bridging Internal Probability and Self-Consistency for Effective and Efficient LLM Reasoning](https://arxiv.org/abs/2502.00511) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2502.00511) [![GitHub Stars](https://img.shields.io/github/stars/wnjxyk/RPC?style=social&label=Star)](https://github.com/wnjxyk/RPC)

:diamond_shape_with_a_dot_inside: [PairJudge RM: Perform Best-of-N Sampling with Knockout Tournament](https://arxiv.org/abs/2501.13007v2) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2501.13007v2) [![GitHub Stars](https://img.shields.io/github/stars/THU-KEG/PairJudgeRM?style=social&label=Star)](https://github.com/THU-KEG/PairJudgeRM)

:diamond_shape_with_a_dot_inside: [TreeBoN: Enhancing Inference-Time Alignment with Speculative Tree-Search and Best-of-N Sampling](https://arxiv.org/abs/2410.16033) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2410.16033)

:diamond_shape_with_a_dot_inside: [Fast Best-of-N Decoding via Speculative Rejection](https://arxiv.org/abs/2410.20290) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2410.20290) [![GitHub Stars](https://img.shields.io/github/stars/Zanette-Labs/SpeculativeRejection?style=social&label=Star)](https://github.com/Zanette-Labs/SpeculativeRejection)

:diamond_shape_with_a_dot_inside: [Scaling Flaws of Verifier-Guided Search in Mathematical Reasoning](https://arxiv.org/abs/2502.00271) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2502.00271) 

:diamond_shape_with_a_dot_inside: [Accelerating Best-of-N via Speculative Rejection](https://openreview.net/forum?id=FKelfq62ay) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://openreview.net/forum?id=FKelfq62ay) [![GitHub Stars](https://img.shields.io/github/stars/Zanette-Labs/SpeculativeRejection?style=social&label=Star)](https://github.com/Zanette-Labs/SpeculativeRejection)

:diamond_shape_with_a_dot_inside: [Adaptive Inference-Time Compute: LLMs Can Predict if They Can Do Better, Even Mid-Generation](https://arxiv.org/abs/2410.02725) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2410.02725) 

:diamond_shape_with_a_dot_inside: [VisualPRM: An Effective Process Reward Model for Multimodal Reasoning](https://arxiv.org/abs/2503.10291v1) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.10291v1) [![GitHub Stars](https://img.shields.io/github/stars/OpenGVLab/InternVL?style=social&label=Star)](https://github.com/OpenGVLab/InternVL)

:no_entry_sign: **Limitation**

When trajectories interleave visual evidence with language-based reasoning, it remains unclear how to define fair and consistent voting or scoring criteria and simultaneously ensure semantic correctness and cross-modal alignment during selection.


(2) **Sequential search** — feedback-driven self-correction

Sequential search does not select a final answer in a single pass; instead, it repeatedly revises the reasoning trajectory using external feedback. 
<!-- Early methods relied on human corrections, later shifting toward programmable or domain-specific feedback. Motivated by the premise that verification is easier than generation, subsequent work introduced iterative self-critique for refinement. -->

:diamond_shape_with_a_dot_inside: [NL-edit: Correcting Semantic Parse Errors through Natural Language Interaction](https://arxiv.org/abs/2103.14540) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2103.14540) [![GitHub Stars](https://img.shields.io/github/stars/MSR-LIT/NLEdit?style=social&label=Star)](https://github.com/MSR-LIT/NLEdit)

:diamond_shape_with_a_dot_inside: [Interscript: A Dataset for Interactive Learning of Scripts through Error Feedback](https://arxiv.org/abs/2112.07867) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2112.07867) [![GitHub Stars](https://img.shields.io/github/stars/allenai/interscript?style=social&label=Star)](https://github.com/allenai/interscript)

:diamond_shape_with_a_dot_inside: [Learning to Repair: Repairing Model Output Errors after Deployment using a Dynamic Memory of Feedback](https://arxiv.org/abs/2112.09737) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2112.09737) [![GitHub Stars](https://img.shields.io/github/stars/allenai/interscript?style=social&label=Star)](https://github.com/allenai/interscript)

:diamond_shape_with_a_dot_inside: [Teaching Large Language Models to Self-Debug](https://arxiv.org/abs/2304.05128) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2304.05128) 

:diamond_shape_with_a_dot_inside: [RARR: Researching and Revising What Language Models Say, Using Language Models](https://arxiv.org/abs/2210.08726) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2210.08726) [![GitHub Stars](https://img.shields.io/github/stars/anthonywchen/RARR?style=social&label=Star)](https://github.com/anthonywchen/RARR)

:diamond_shape_with_a_dot_inside: [CRITIC: Large Language Models Can Self-Correct with Tool-Interactive Critiquing](https://arxiv.org/abs/2305.11738) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2305.11738) [![GitHub Stars](https://img.shields.io/github/stars/microsoft/ProphetNet?style=social&label=Star)](https://github.com/microsoft/ProphetNet/tree/master/CRITIC)

:diamond_shape_with_a_dot_inside: [Graph-based Self-supervised Program Repair from Diagnostic Feedback](https://arxiv.org/abs/2005.10636) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2005.10636) [![GitHub Stars](https://img.shields.io/github/stars/michiyasunaga/DrRepair?style=social&label=Star)](https://github.com/michiyasunaga/DrRepair)

:diamond_shape_with_a_dot_inside: [Is Self-Repair a Silver Bullet for Code Generation?](https://arxiv.org/abs/2306.09896) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2306.09896) [![GitHub Stars](https://img.shields.io/github/stars/theoxo/self-repair?style=social&label=Star)](https://github.com/theoxo/self-repair)

:diamond_shape_with_a_dot_inside: [Large Language Models Cannot Self-Correct Reasoning Yet](https://arxiv.org/abs/2310.01798) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2310.01798)

:diamond_shape_with_a_dot_inside: [Reasoning in Token Economics: Budget-aware Evaluation of LLM Reasoning Strategies](https://arxiv.org/abs/2406.06461) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2406.06461)

:diamond_shape_with_a_dot_inside: [Can Large Language Models Really Improve by Self-Critiquing Their Own Plans?](https://arxiv.org/abs/2310.08118) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2310.08118)

:diamond_shape_with_a_dot_inside: [GPT-4 Doesn’t Know It’s Wrong: An Analysis of Iterative Prompting for Reasoning Problems](https://arxiv.org/abs/2310.12397) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2310.12397)

:diamond_shape_with_a_dot_inside: [Training Language Models to Self-Correct via Reinforcement Learning](https://arxiv.org/abs/2409.12917) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2409.12917)

:diamond_shape_with_a_dot_inside: [Advancing Language Model Reasoning through Reinforcement Learning and Inference Scaling](https://arxiv.org/abs/2501.11651) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2501.11651) [![GitHub Stars](https://img.shields.io/github/stars/THUDM/T1?style=social&label=Star)](https://github.com/THUDM/T1)



:no_entry_sign: **Limitation** 

Under complex or adversarial inputs, self-correction can degrade previously correct solutions. In LMRMs, purely language-based reflection cannot reliably assess whether visual evidence is sufficient and often fails to maintain cross-modal consistency.

(3) **Structured search** — tree- or graph-based exploration and backtracking

Structured search more closely resembles human problem solving by exploring branches and backtracking over tree/graph structures. However, it often incurs high computational overhead, myopic search behavior, and poor performance in continuous spaces. In multimodal settings, it has been used primarily during SFT and has not yet been explicitly coupled with visual or cross-modal interaction.

:diamond_shape_with_a_dot_inside: [Airrag: Activating Intrinsic Reasoning for Retrieval Augmented Generation using Tree-based Search](https://arxiv.org/abs/2501.10053) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2501.10053)

:diamond_shape_with_a_dot_inside: [Serts: Self-rewarding Tree Search for Biomedical Retrieval-augmented Generation](https://arxiv.org/abs/2406.11258) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2406.11258)

:diamond_shape_with_a_dot_inside: [Rag-star: Enhancing Deliberative Reasoning with Retrieval Augmented Verification and Refinement](https://arxiv.org/abs/2412.12881) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2412.12881)

:diamond_shape_with_a_dot_inside: [Think&Cite: Improving Attributed Text Generation with Self-Guided Tree Search and Progress Reward Modeling](https://arxiv.org/abs/2412.14860) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2412.14860) [![GitHub Stars](https://img.shields.io/github/stars/nusnlp/Think-Cite?style=social&label=Star)](https://github.com/nusnlp/Think-Cite)

:diamond_shape_with_a_dot_inside: [Master: A Multi-agent System with LLM Specialized Agents](https://arxiv.org/abs/2501.14304) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2501.14304) 

:diamond_shape_with_a_dot_inside: [Kbqa-o1: Agentic Knowledge Base Question Answering with Monte Carlo Tree Search](https://arxiv.org/abs/2501.18922) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2501.18922) [![GitHub Stars](https://img.shields.io/github/stars/LHRLAB/KBQA-o1?style=social&label=Star)](https://github.com/LHRLAB/KBQA-o1)

:diamond_shape_with_a_dot_inside: [Think more, hallucinate less: Mitigating hallucinations via dual process of fast and slow thinking](https://arxiv.org/abs/2501.01306) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2501.01306) [![GitHub Stars](https://img.shields.io/github/stars/RUCAIBox/Slow_Thinking_with_LLMs?style=social&label=Star)](https://github.com/RUCAIBox/Slow_Thinking_with_LLMs)

:diamond_shape_with_a_dot_inside: [Mcts-sql: An effective framework for text-to-sql with monte carlo tree search](https://arxiv.org/abs/2501.16607) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2501.16607)

:diamond_shape_with_a_dot_inside: [Mulberry: Empowering MLLM with o1-like Reasoning and Reflection via Collective Monte Carlo Tree Search](https://arxiv.org/abs/2412.18319) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2412.18319) [![GitHub Stars](https://img.shields.io/github/stars/HJYao00/Mulberry?style=social&label=Star)](https://github.com/HJYao00/Mulberry)

:diamond_shape_with_a_dot_inside: [SoTA with Less: MCTS-Guided Sample Selection for Data-Efficient Visual Reasoning Self-Improvement](https://arxiv.org/abs/2504.07934) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2504.07934) [![GitHub Stars](https://img.shields.io/github/stars/si0wang/ThinkLite-VL?style=social&label=Star)](https://github.com/si0wang/ThinkLite-VL)

:diamond_shape_with_a_dot_inside: [Mastering the game of Go without human knowledge](https://arxiv.org/abs/1712.01815) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/1712.01815) 

:diamond_shape_with_a_dot_inside: [Marco-o1: Towards Open Reasoning Models for Open-Ended Solutions](https://arxiv.org/abs/2411.14405) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2411.14405) [![GitHub Stars](https://img.shields.io/github/stars/AIDC-AI/Marco-o1?style=social&label=Star)](https://github.com/AIDC-AI/Marco-o1)

:diamond_shape_with_a_dot_inside: [Inference scaling laws: An empirical analysis of compute-optimal inference for problem-solving with language models](https://arxiv.org/abs/2408.00724) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2408.00724) [![GitHub Stars](https://img.shields.io/github/stars/thu-wyz/inference_scaling?style=social&label=Star)](https://github.com/thu-wyz/inference_scaling)


:diamond_shape_with_a_dot_inside: [rStar-Math: Small LLMs Can Master Math Reasoning with Self-evolved Deep Thinking](https://arxiv.org/abs/2501.04519) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2501.04519) [![GitHub Stars](https://img.shields.io/github/stars/microsoft/rStar?style=social&label=Star)](https://github.com/microsoft/rStar)

:diamond_shape_with_a_dot_inside: [Graph of Thoughts: Solving Elaborate Problems with Large Language Models](https://arxiv.org/abs/2308.09687) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2308.09687) [![GitHub Stars](https://img.shields.io/github/stars/spcl/graph-of-thoughts?style=social&label=Star)](https://github.com/spcl/graph-of-thoughts)



:no_entry_sign: **Limitation** 

For LMRMs, the primary bottleneck lies in node construction and node evaluation. Redundant multimodal information complicates node selection, while existing evaluators struggle to quantify cross-modal alignment and the completeness of available information.

:round_pushpin: **Improvement direction**

- Establish a unified scoring criterion for heterogeneous trajectories
- Adaptively allocate computational resources to branches whose hypotheses are more consistent with the evidence;
- Leverage process-level rewards and intermediate evaluation to correct errors early, reduce backtracking, and lower search overhead.




### <a id="test-43-dynamic-verification"></a>4.3 Dynamic Verification

Dynamic verification assigns a rule-defined scalar score to assess how consistent LRMR-generated outputs are with either the ground-truth answer or a reference human reasoning process. By the source of the scoring signal, methods can be grouped into three types: outcome-based, process-based, and generative.


(1) **Outcome-based verification**

:diamond_shape_with_a_dot_inside: [Training Verifiers to Solve Math Word Problems](https://arxiv.org/abs/2110.14168) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2110.14168) [![GitHub Stars](https://img.shields.io/github/stars/openai/grade-school-math?style=social&label=Star)](https://github.com/openai/grade-school-math)

:diamond_shape_with_a_dot_inside: [When Is Tree Search Useful for LLM Planning? It Depends on the Discriminator](https://arxiv.org/abs/2402.10890) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2402.10890) [![GitHub Stars](https://img.shields.io/github/stars/OSU-NLP-Group/llm-planning-eval?style=social&label=Star)](https://github.com/OSU-NLP-Group/llm-planning-eval)

:diamond_shape_with_a_dot_inside: [Plan, Verify and Switch: Integrated Reasoning with Diverse X-of-Thoughts](https://arxiv.org/abs/2310.14628) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2310.14628) [![GitHub Stars](https://img.shields.io/github/stars/tengxiaoliu/XoT?style=social&label=Star)](https://github.com/tengxiaoliu/XoT)

:diamond_shape_with_a_dot_inside: [Wrong-of-Thought: An Integrated Reasoning Framework with Multi-Perspective Verification and Wrong Information](https://arxiv.org/abs/2410.04463) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2410.04463) [![GitHub Stars](https://img.shields.io/github/stars/BRZ911/Wrong-of-Thought?style=social&label=Star)](https://github.com/BRZ911/Wrong-of-Thought)

:diamond_shape_with_a_dot_inside: [Multi-Agent Verification: Scaling Test-Time Compute with Multiple Verifiers](https://arxiv.org/abs/2502.20379) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2502.20379) [![GitHub Stars](https://img.shields.io/github/stars/Shalev-Lifshitz/MultiAgentVerification?style=social&label=Star)](https://github.com/Shalev-Lifshitz/MultiAgentVerification)

:diamond_shape_with_a_dot_inside: [PlanGEN: A Multi-Agent Framework for Generating Planning and Reasoning Trajectories for Complex Problem Solving](https://arxiv.org/abs/2502.16111) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2502.16111) 

:diamond_shape_with_a_dot_inside: [Archon: An Architecture Search Framework for Inference-Time Techniques](https://arxiv.org/abs/2409.15254) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2409.15254) [![GitHub Stars](https://img.shields.io/github/stars/ScalingIntelligence/Archon?style=social&label=Star)](https://github.com/ScalingIntelligence/Archon)

:no_entry_sign: **Limitation** 
Sensitive to linguistic variation and visual noise, and can be easily disrupted by linguistic paraphrases or visual perturbations.

(2) **Process-based verification**

:diamond_shape_with_a_dot_inside: [Can Large Language Models Be an Alternative to Human Evaluations?](https://arxiv.org/abs/2305.01937) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2305.01937) [![GitHub Stars](https://img.shields.io/github/stars/d223302/LLM-Evaluation?style=social&label=Star)](https://github.com/d223302/LLM-Evaluation)

:diamond_shape_with_a_dot_inside: [G-Eval: NLG Evaluation using GPT-4 with Better Human Alignment](https://arxiv.org/abs/2303.16634) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2303.16634) [![GitHub Stars](https://img.shields.io/github/stars/nlpyang/geval?style=social&label=Star)](https://github.com/nlpyang/geval)

:diamond_shape_with_a_dot_inside: [ChatGPT as a Factual Inconsistency Evaluator for Text Summarization](https://arxiv.org/abs/2303.15621) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2303.15621)  

:diamond_shape_with_a_dot_inside: [Is ChatGPT a Good NLG Evaluator? A Preliminary Study](https://arxiv.org/abs/2303.04048) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2303.04048) [![GitHub Stars](https://img.shields.io/github/stars/krystalan/chatgpt_as_nlg_evaluator?style=social&label=Star)](https://github.com/krystalan/chatgpt_as_nlg_evaluator)

:diamond_shape_with_a_dot_inside: [Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena](https://arxiv.org/abs/2306.05685) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2306.05685) [![GitHub Stars](https://img.shields.io/github/stars/lm-sys/FastChat?style=social&label=Star)](https://github.com/lm-sys/FastChat)

:diamond_shape_with_a_dot_inside: [Learning to Retrieve Prompts for In-Context Learning](https://arxiv.org/abs/2112.08633) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2112.08633) [![GitHub Stars](https://img.shields.io/github/stars/OhadRubin/EPR?style=social&label=Star)](https://github.com/OhadRubin/EPR)

:diamond_shape_with_a_dot_inside: [Fenec: Fine-grained Language Model Evaluation and Correction Extended through Branching and Bridging](https://arxiv.org/abs/2405.12163) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2405.12163) [![GitHub Stars](https://img.shields.io/github/stars/dropreg/Fennec?style=social&label=Star)](https://github.com/dropreg/Fennec)

:diamond_shape_with_a_dot_inside: [PandaLM: An Automatic Evaluation Benchmark for LLM Instruction Tuning Optimization](https://arxiv.org/abs/2306.05087) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2306.05087) [![GitHub Stars](https://img.shields.io/github/stars/WeOpenML/PandaLM?style=social&label=Star)](https://github.com/WeOpenML/PandaLM)

:diamond_shape_with_a_dot_inside: [JudgeLM: Fine-tuned Large Language Models are Scalable Judges](https://arxiv.org/abs/2310.17631) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2310.17631) [![GitHub Stars](https://img.shields.io/github/stars/baaivision/JudgeLM?style=social&label=Star)](https://github.com/baaivision/JudgeLM)

:diamond_shape_with_a_dot_inside: [Shepherd: A Critic for Language Model Generation](https://arxiv.org/abs/2308.04592) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2308.04592) [![GitHub Stars](https://img.shields.io/github/stars/facebookresearch/shepherd?style=social&label=Star)](https://github.com/facebookresearch/shepherd)

:diamond_shape_with_a_dot_inside: [Generative Judge for Evaluating Alignment](https://arxiv.org/abs/2310.05470) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2310.05470) [![GitHub Stars](https://img.shields.io/github/stars/GAIR-NLP/auto-j?style=social&label=Star)](https://github.com/GAIR-NLP/auto-j)

:diamond_shape_with_a_dot_inside: [Prometheus: Inducing Fine-grained Evaluation Capability in Language Models](https://arxiv.org/abs/2310.08491) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2310.08491) [![GitHub Stars](https://img.shields.io/github/stars/prometheus-eval/prometheus?style=social&label=Star)](https://github.com/prometheus-eval/prometheus)

:diamond_shape_with_a_dot_inside: [Prometheus 2: An Open Source Language Model Specialized in Evaluating Other Language Models](https://arxiv.org/abs/2405.01535) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2405.01535) [![GitHub Stars](https://img.shields.io/github/stars/prometheus-eval/prometheus-eval?style=social&label=Star)](https://github.com/prometheus-eval/prometheus-eval)


:no_entry_sign: **Limitation** 

Offers stronger diagnostic capability, but depends on costly intermediate annotations, resulting in scarce data and high labeling cost.

(3) **Generative verification**

:diamond_shape_with_a_dot_inside: [Tree of Thoughts: Deliberate Problem Solving with Large Language Models](https://arxiv.org/abs/2305.10601) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2305.10601) [![GitHub Stars](https://img.shields.io/github/stars/princeton-nlp/tree-of-thought-llm?style=social&label=Star)](https://github.com/princeton-nlp/tree-of-thought-llm)

:diamond_shape_with_a_dot_inside: [Self-evaluation guided beam search for reasoning](https://arxiv.org/abs/2305.00633) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2305.00633) [![GitHub Stars](https://img.shields.io/github/stars/YuxiXie/SelfEval-Guided-Decoding?style=social&label=Star)](https://github.com/YuxiXie/SelfEval-Guided-Decoding)

:diamond_shape_with_a_dot_inside: [Math-Shepherd: Verify and Reinforce LLMs Step-by-Step without Human Annotations](https://arxiv.org/abs/2312.08935) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2312.08935) [![GitHub](https://img.shields.io/badge/web-00BFFF.svg)](https://achieved-bellflower-4d6.notion.site/Math-Shepherd-Verify-and-Reinforce-LLMs-Step-by-step-without-Human-Annotations-41b6e73c860840e08697d347f8889bac?pvs=4)

:diamond_shape_with_a_dot_inside: [Improve Mathematical Reasoning in Language Models by Automated Process Supervision](https://arxiv.org/abs/2406.06592) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2406.06592) [![GitHub Stars](https://img.shields.io/github/stars/sanowl/OmegaPRM?style=social&label=Star)](https://github.com/sanowl/OmegaPRM)

:diamond_shape_with_a_dot_inside: [An Efficient and Precise Training Data Construction Framework for Process-Supervised Reward Model in Mathematical Reasoning](https://arxiv.org/abs/2503.02382) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.02382) [![GitHub Stars](https://img.shields.io/github/stars/xiaolizh1/EpicPRM?style=social&label=Star)](https://github.com/xiaolizh1/EpicPRM)


:no_entry_sign: **Limitation** 

Highly sensitive to the choice of model and prompting, and often exhibits text bias at the expense of visual fidelity. Moreover, models' intrinsic biases and invocation costs are difficult to eliminate entirely.

:round_pushpin: **Improvement direction**
Use RL as a trajectory verifier at test time, leveraging verifier feedback to dynamically guide exploration, pruning, and backtracking. This could mitigate the brittleness of outcome-, process-, and generative verification in multimodal settings, yielding more reliable multimodal reasoning without parameter updates.


### <a id="test-44-trajectory-optimization"></a>4.4 Trajectory Optimization

In this context, trajectory optimization denotes controlling and refining candidate reasoning trajectories without parameter updates. Conditioned on task difficulty and uncertainty, it adaptively adjusts trajectory length and structure, improving accuracy while also increasing computational efficiency.

(1) **RL-free methods**

Data-driven distillation extracts shorter reasoning trajectories from a teacher model, which can mitigate overly long CoT traces in text-only tasks.

:diamond_shape_with_a_dot_inside: [Distilling Reasoning Capabilities into Smaller Language Models](https://arxiv.org/abs/2212.00193) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2212.00193) [![GitHub Stars](https://img.shields.io/github/stars/kumar-shridhar/Distiiling-LM?style=social&label=Star)](https://github.com/kumar-shridhar/Distiiling-LM)

:diamond_shape_with_a_dot_inside: [Distilling Step-by-Step! Outperforming Larger Language Models with Less Training Data and Smaller Model Sizes](https://arxiv.org/abs/2305.02301) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2305.02301) [![GitHub Stars](https://img.shields.io/github/stars/google-research/distilling-step-by-step?style=social&label=Star)](https://github.com/google-research/distilling-step-by-step)

:diamond_shape_with_a_dot_inside: [Unveiling the Key Factors for Distilling Chain-of-Thought Reasoning](https://arxiv.org/abs/2502.18001) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2502.18001) [![GitHub Stars](https://img.shields.io/github/stars/EIT-NLP/Distilling-CoT-Reasoning?style=social&label=Star)](https://github.com/EIT-NLP/Distilling-CoT-Reasoning)

:diamond_shape_with_a_dot_inside: [Recall with Reasoning: Chain-of-Thought Distillation for Mamba's Long-Context Memory and Extrapolation](https://arxiv.org/abs/2505.03320) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2505.03320)

:diamond_shape_with_a_dot_inside: [LLaVA-KD: A Framework of Distilling Multimodal Large Language Models](https://arxiv.org/abs/2410.16236) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2410.16236) [![GitHub Stars](https://img.shields.io/github/stars/Fantasyele/LLaVA-KD?style=social&label=Star)](https://github.com/Fantasyele/LLaVA-KD)


(2) **RL-based methods**

By incorporating sample selection, RL-based methods can enable early backtracking and prune erroneous trajectories, controlling computational cost under a fixed compute budget while preserving diversity. Appropriate reward signals further align the outputs with the intended reasoning objectives.

:diamond_shape_with_a_dot_inside: [Scaling Test-Time Compute Without Verification or RL is Suboptimal](https://arxiv.org/abs/2502.12118) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2502.12118)

:diamond_shape_with_a_dot_inside: [Optimizing Test-Time Compute via Meta Reinforcement Fine-Tuning](https://arxiv.org/abs/2503.07572) [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2503.07572) [![GitHub Stars](https://img.shields.io/github/stars/CMU-AIRe/MRT?style=social&label=Star)](https://github.com/CMU-AIRe/MRT)


:no_entry_sign: **Limitation** 

In LMRMs, tasks such as VQA often require multiple rounds of region-level attention, retrieval, and cross-modal verification, yielding longer trajectories and more pronounced error accumulation. The resulting expansion of the state space makes it difficult for distillation to cover the full set of reasoning states, which can lead to underfitting or the overlooking of high-value paths.

:round_pushpin: **Improvement direction**

In LMRMs, test-time trajectory optimization should move beyond naïve short-trajectory distillation toward alignment-aware process distillation, and integrate RL reward signals or trajectory selection mechanisms. By dynamically optimizing trajectories while preserving cross-modal consistency, such approaches will more robustly improve *System-2*-style reasoning quality.



## 5. Datasets & Benchmarks
### <a id="bench-51-goal-driven-reasoning"></a>5.1 Goal-driven Reasoning
<table>
  <thead>
    <tr>
      <th>Benchmark</th>
      <th>Year</th>
      <th>Size</th>
      <th>Metrics</th>
      <th>Q-Type</th>
      <th>Dom.</th>
      <th>Ann.</th>
      <th>Link</th>
    </tr>
  </thead>
  <tr>
    <td colspan="8"><i><b>General Visual Reasoning</b></i></td>
  </tr>
  <tbody>
    <tr>
      <td><a href="https://arxiv.org/abs/2307.06281"><code>MMBench</code></a></td>
      <td>2024</td>
      <td>3.2K</td>
      <td>Acc., CircularEval</td>
      <td>MC</td>
      <td>General</td>
      <td>HA + AA</td>
      <td align="center"><a href="https://huggingface.co/datasets/HuggingFaceM4/MMBench"><img src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg" alt="HF" width="18"></a></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2311.16502"><code>MMMU</code></a></td>
      <td>2024</td>
      <td>11.5K</td>
      <td>Acc.</td>
      <td>MC, OE</td>
      <td>Interdisciplinary</td>
      <td>HA</td>
      <td align="center"><a href="https://huggingface.co/datasets/MMMU/MMMU"><img src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg" alt="HF" width="18"></a></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2304.06364"><code>AGIEval</code></a></td>
      <td>2024</td>
      <td>8K</td>
      <td>Acc., F1 Score, Exact Match</td>
      <td>MC, OE</td>
      <td>Exams</td>
      <td>AA</td>
      <td align="center"><a href="https://github.com/ruixiangcui/AGIEval"><img src="https://img.shields.io/badge/-181717?style=social&logo=github" alt="GitHub"></a></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2310.14566"><code>HallusionBench</code></a></td>
      <td>2024</td>
      <td>0.2K</td>
      <td>Acc., AS</td>
      <td>OE</td>
      <td>Robustness</td>
      <td>HA</td>
      <td align="center"><a href="https://github.com/tianyi-lab/HallusionBench"><img src="https://img.shields.io/badge/-181717?style=social&logo=github" alt="GitHub"></a></td>
    </tr>
    <tr>
      <td colspan="8"><i><b>Structured and Task-Specific Reasoning</b></i></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2405.09711"><code>STAR</code></a></td>
      <td>2024</td>
      <td>60K</td>
      <td>Acc.</td>
      <td>MC</td>
      <td>Situational Rea.</td>
      <td>AA + HA</td>
      <td align="center"><a href="https://github.com/tianyi-lab/HallusionBench"><img src="https://img.shields.io/badge/web-00BFFF.svg" alt="GitHub"></a></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2502.14191"><code>Multimodal RewardBench</code></a></td>
      <td>2025</td>
      <td>5.2K</td>
      <td>Acc.</td>
      <td>MC, OE</td>
      <td>General, Safety</td>
      <td>HA</td>
      <td align="center"><a href="https://huggingface.co/datasets/syhuggingface/multimodal_rewardbench"><img src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg" alt="HF" width="18"></a></td>
    </tr>
    <tr>
      <td colspan="8">
        💖<b>Core Benchmarks (Milestone):</b><br>
        <a href="https://huggingface.co/datasets/ranjaykrishna/visual_genome"><code>Visual Genome</code></a>, <a href="https://huggingface.co/datasets/HuggingFaceM4/A-OKVQA"><code>A-OKVQA</code></a>, <a href="https://huggingface.co/datasets/derek-thomas/ScienceQA"><code>ScienceQA</code></a>, <a href="https://huggingface.co/datasets/AILab-CVC/SEED-Bench"><code>SEED-bench</code></a>, <a href="https://huggingface.co/datasets/BLINK-Benchmark/BLINK"><code>Blink</code></a>,
        <a href="https://huggingface.co/datasets/MilaWang/SpatialEval"><code>SpatialEval</code></a>, <a href="https://huggingface.co/datasets/HuanjinYao/Mulberry-SFT"><code>Mulberry-260K</code></a>, <a href="https://huggingface.co/collections/laolao77/virft-datasets"><code>Visual-RFT</code></a>.
      </td>
    </tr>
    <tr>
      <td colspan="8"> 
        💕<b>Representative Benchmarks:</b><br>
        <a href="https://github.com/T-SciQ/T-SciQ"><code>T-SciQ dataset</code></a>, <a href="https://visualabduction.com/"><code>Sherlock</code></a>, <a href="https://github.com/AILab-CVC/VL-GPT"><code>VL-GPT</code></a>, <a href="https://shramanpramanick.github.io/VistaLLM/"><code>CoinIt</code></a>, <a href="https://huggingface.co/datasets/whyu/mm-vet-v2"><code>MM-Vet v2</code></a>,
        <a href="https://huggingface.co/datasets/Harold328/OmniBench-99"><code>OmniBench</code></a>, <a href="https://huggingface.co/datasets/NukaSarsae/MM-SAP"><code>MM-SPA</code></a>, <a href="https://huggingface.co/datasets/czh-up/CoMT"><code>CoMT</code></a>, <a href="https://schowdhury671.github.io/avtrustbench_project/"><code>AVTrustBench</code></a>, <a href="https://huggingface.co/datasets/Salesforce/ProVision-10M"><code>ProVision</code></a>,
        <a href="https://huggingface.co/datasets/MMInstruction/VL-RewardBench"><code>VL-RewardBench</code></a>, <a href="https://huggingface.co/datasets/luckychao/EMMA"><code>EMMA</code></a>, <a href="https://github.com/kaist-ami/AVHBench"><code>AVHBench</code></a>, <a href="https://huggingface.co/datasets/FreedomIntelligence/ShareGPT-4o-Image"><code>ShareGPT-4o-Image</code></a>,
        <a href="https://huggingface.co/datasets/PCA-Bench/PCA-Bench-V1"><code>PCA-Bench</code></a>, <a href="https://github.com/adlnlp/magic_vqa"><code>MAGIC-VQA</code></a>, <a href="https://huggingface.co/datasets/huanqia/MM-IQ"><code>Mm-iq</code></a>, <a href="https://github.com/ZrrSkywalker/MAVIS"><code>MAVIS</code></a>, <a href="https://huggingface.co/datasets/m-a-p/II-Bench"><code>II-Bench</code></a>,
        <a href="https://huggingface.co/datasets/jmhb/microvqa"><code>MicroVQA</code></a>, <a href="https://huggingface.co/datasets/ShirohAO/tuxun#citation-information"><code>GeoComp</code></a>.
      </td>
    </tr>
    <tr>
      <td colspan="8"> 
        ❤️<b>Other Benchmarks (Emerging):</b><br>
        <a href="https://huggingface.co/datasets/jing-bi/verify-teaser"><code>VERIFY</code></a>, <a href="https://github.com/liujunzhuo/FineCops-Ref"><code>FineCops-Ref</code></a>, <a href="https://huggingface.co/datasets/xueyanz/FIND-Bench"><code>FIND-Bench</code></a>, <a href="https://huggingface.co/datasets/htlou/mm-interp-CompCap-gpt4-data"><code>CompCap</code></a>, <a href="https://huggingface.co/datasets/wphu/CapQA"><code>CapQA</code></a>,
        <a href="https://huggingface.co/datasets/SimulaMet/Kvasir-VQA-x1"><code>Ksavir-VQA-x1</code></a>, <a href="https://huggingface.co/datasets/HarrytheOrange/MMRB"><code>MMRB</code></a>, <a href="https://github.com/Zhanglei1103/MMESGBench"><code>MMESGBench</code></a>, <a href="https://github.com/jfliang3324/GUIDE"><code>GUIDE</code></a>, <a href="https://github.com/togethercomputer/SMiR"><code>SMIR</code></a>,
        <a href="https://huggingface.co/datasets/m-a-p/CII-Bench"><code>CII-Bench</code></a>, <a href="https://github.com/microsoft/MageBench"><code>MAGEBench</code></a>, <a href="https://huggingface.co/datasets/RUBBISHLIKE/PunchBench"><code>PunchBench</code></a>,
        <a href="https://journeybench.github.io/"><code>JourneyBench</code></a>, <a href="https://huggingface.co/datasets/yh0075/VisuRiddles"><code>VisuRiddles</code></a>.
      </td>
    </tr>
  </tbody>
</table>

> **Abbreviations.**
(1) **Metrics**: *AS* = Auto-Score.
(2) **Q-Type**: *OE* = Open-Ended Questions, *MC* = Multiple Choice Questions (Select all that apply).
(3) **Ann.**: *HA* = Human Annotation, *AA* = Auto-Annotation.


### <a id="bench-52-causal--verifiable-reasoning"></a>5.2 Causal & Verifiable Reasoning 

<table>
  <thead>
    <tr>
      <th>Benchmark</th>
      <th>Year</th>
      <th>Size</th>
      <th>Metrics</th>
      <th>Q-Type</th>
      <th>Dom.</th>
      <th>Ann.</th>
      <th>Link</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td colspan="8"><i><b>Domain-Specific Reasoning</b></i></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2310.02255"><code>MathVista</code></a></td>
      <td>2023</td>
      <td>6.1K</td>
      <td>Acc.</td>
      <td>MC, OE</td>
      <td>Math, Visual Und.</td>
      <td>AA + MV</td>
      <td align="center"><a href="https://huggingface.co/datasets/AI4Math/MathVista"><img src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg" alt="HF" width="18"></a></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2403.20330"><code>MM-Star</code></a></td>
      <td>2024</td>
      <td>1.5K</td>
      <td>Acc., Multimodal Gain and Leakag</td>
      <td>MC</td>
      <td>Visual Abductive Rea.</td>
      <td>AA + MV</td>
      <td align="center"><a href="https://huggingface.co/datasets/Lin-Chen/MMStar"><img src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg" alt="HF" width="18"></a></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2409.02813"><code>MMMU-Pro</code></a></td>
      <td>2025</td>
      <td>3.5K</td>
      <td>Acc.</td>
      <td>MC</td>
      <td>Interdisciplinary</td>
      <td>AA + MV</td>
      <td align="center"><a href="https://huggingface.co/datasets/MMMU/MMMU_Pro"><img src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg" alt="HF" width="18"></a></td>
    </tr>
    <tr>
      <td colspan="8"><i><b>Diagrammatic and Spatial Reasoning</b></i></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2401.12168"><code>SpatialVLM-Dataset</code></a></td>
      <td>2024</td>
      <td>2B</td>
      <td>Acc., MSE</td>
      <td>OE</td>
      <td>Embodied Robot Rea., Spat. Rea.</td>
      <td>AA</td>
      <td align="center"><a href="https://github.com/remyxai/VQASynth"><img src="https://img.shields.io/badge/-181717?style=social&logo=github" alt="GitHub"></a></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2406.18521"><code>CharXiv</code></a></td>
      <td>2024</td>
      <td>11.6K</td>
      <td>AS</td>
      <td>OE</td>
      <td>Chart Und.</td>
      <td>HA</td>
      <td align="center"><a href="https://huggingface.co/datasets/princeton-nlp/CharXiv"><img src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg" alt="HF" width="18"></a></td>
    </tr>
    <tr>
      <td colspan="8"><i><b>Counterfactual and Logical Reasoning</b></i></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2407.04973"><code>LogicVista</code></a></td>
      <td>2024</td>
      <td>0.45K</td>
      <td>Acc.</td>
      <td>MC</td>
      <td>Logical Rea.</td>
      <td>HA</td>
      <td align="center"><a href="https://github.com/Yijia-Xiao/LogicVista"><img src="https://img.shields.io/badge/-181717?style=social&logo=github" alt="GitHub"></a></td>
    </tr>
    <tr>
      <td colspan="8">
        💖<b>Core Benchmarks (Milestone):</b><br>
        <a href="https://cs.stanford.edu/people/jcjohns/clevr/"><code>CLEVR</code></a>, <a href="https://huggingface.co/datasets/lmms-lab/ChartQA"><code>ChartQA</code></a>, <a href="https://huggingface.co/datasets/Hothan/OlympiadBench"><code>OlympiadBench</code></a>, <a href="https://www.docvqa.org/datasets/infographicvqa"><code>InfographicVQA</code></a>, <a href="https://huggingface.co/datasets/AI4Math/MathVerse"><code>MathVerse</code></a>, <a href="https://github.com/amitakamath/whatsup_vlms"><code>WhatsUp</code></a>, <a href="https://huggingface.co/datasets/TIGER-Lab/TheoremQA"><code>TheoremQA</code></a>, 
        <a href="https://huggingface.co/datasets/MathLLMs/MathVision"><code>MATH-Vision</code></a>, <a href="https://github.com/Genesis-Embodied-AI/RoboGen"><code>RoboGen</code></a>, <a href="https://huggingface.co/datasets/nyu-visionx/VSI-Bench"><code>VSIBench</code></a>, <a href="https://huggingface.co/datasets/deepcs233/Visual-CoT"><code>Visual-CoT</code></a>, <a href="https://huggingface.co/datasets/We-Math/We-Math"><code>WE-MATH</code></a>.
      </td>
    </tr>
    <tr>
      <td colspan="8"> 
        💕<b>Representative Benchmarks:</b><br>
        <a href="https://github.com/thiippal/AI2D-RST"><code>AI2D</code></a>,
        <a href="https://huggingface.co/videophysics"><code>VideoPhy</code></a>,
        <a href="https://huggingface.co/datasets/SincereX/ChartBench"><code>ChartBench</code></a>,
        <a href="https://huggingface.co/datasets/ChartMimic/ChartMimic"><code>ChartMimic</code></a>,
        <a href="https://huggingface.co/datasets/TencentARC/Plot2Code"><code>Plot2Code</code></a>,
        <a href="https://huggingface.co/datasets/USC-GVL/PhysBench"><code>PhysBench</code></a>,
        <a href="https://huggingface.co/datasets/M4U-Benchmark/M4U"><code>M4U</code></a>,
        <a href="https://huggingface.co/datasets/PeijieWang/MV-MATH"><code>MV-MATH</code></a>,
        <a href="https://github.com/Letian2003/C-VQA"><code>C-VQA</code></a>,
        <a href="https://huggingface.co/datasets/m-a-p/CMMMU"><code>CMMMU</code></a>,
        <a href="https://github.com/ECNU-ICALK/EduChat-Math"><code>CMM-Math</code></a>,
        <a href="https://github.com/OpenMOSS/GAOKAO-MM"><code>GAOKAO-MM</code></a>,
        <a href="https://huggingface.co/datasets/HumanEval-V/HumanEval-V-Benchmark"><code>HumanEval-V</code></a>,
        <a href="https://github.com/lizhouf/NPHardEval4V"><code>NPHardEval4V</code></a>,
        <a href="https://huggingface.co/datasets/HanSolo9682/Flickr30k-Counterfactuals"><code>CounterCurate</code></a>,
        <a href="https://huggingface.co/datasets/SurplusDeficit/MultiHop-EgoQA"><code>MultiHop-EgoQA</code></a>,
        <a href="https://github.com/Zivenzhu/Multi-chart-QA"><code>MultiChartQA</code></a>,
        <a href="https://huggingface.co/datasets/MathLLMs/ImgCode-8.6M"><code>ImgCode-8.6M</code></a>,
        <a href="https://huggingface.co/datasets/VisuLogic/VisuLogic"><code>VisuLogic</code></a>,
        <a href="https://huggingface.co/datasets/MathLLMs/MM-MathInstruct"><code>MM-MathInstruct-3M</code></a>,
        <a href="https://huggingface.co/datasets/OpenStellarTeam/GeoSense"><code>GeoSense</code></a>,
        <a href="https://huggingface.co/datasets/DreamMr/HR-Bench"><code>HR-Bench</code></a>,
        <a href="https://huggingface.co/datasets/Michael4933/MGrounding-630k"><code>MGrounding-630k</code></a>, <a href="https://huggingface.co/datasets/Michael4933/MIG-Bench"><code>MIG-Bench</code></a>.
      </td>
    </tr>
    <tr>
      <td colspan="8"> 
        ❤️<b>Other Benchmarks (Emerging):</b><br>
        <a href="https://huggingface.co/datasets/AAAndyZ/VGCure"><code>MCDGRAPH</code></a>, <a href="https://github.com/Ahalfmoon/MathScape"><code>MathScape</code></a>, <a href="https://github.com/LUNAProject22/CausalChaos"><code>CausalChaos!</code></a>, <a href="https://microcosm.ai/ivispar/"><code>iVISPAR</code></a>, <a href="https://github.com/LanceZPF/MDK12"><code>MDK12-Bench</code></a>, <a href="https://huggingface.co/datasets/xuzhaopan/MPBench"><code>MPBench</code></a>, <a href="https://huggingface.co/datasets/Pinkygin/MuCR"><code>MuCR</code></a>, <a href="https://github.com/declare-lab/LLM-PuzzleTest/tree/master/AlgoPuzzleVQA"><code>AlgoPuzzleVQA</code></a>,
        <a href="https://huggingface.co/datasets/PrismaX/PhysUniBench"><code>PhysUniBench</code></a>, <a href="https://huggingface.co/datasets/OpenRaiser/Geoint"><code>Geoint</code></a>, <a href="https://huggingface.co/datasets/mrble/MARBLE"><code>MARBLE</code></a>, <a href="https://huggingface.co/datasets/junfeng0288/MathReal"><code>MathReal</code></a>, <a href="https://huggingface.co/datasets/erenzhou/AVI-Math"><code>AVI-MATH</code></a>, <a href="https://huggingface.co/datasets/sunshk/CRAVE-DB"><code>CRAVE</code></a>, <a href="https://huggingface.co/datasets/isobench/IsoBench"><code>ISO-BENCH</code></a>, <a href="https://huggingface.co/datasets/yueluoshuangtian/MLLM-CITBench"><code>MLLM-Cbench</code></a>,
        <a href="https://huggingface.co/datasets/We-Math/We-Math2.0-Standard"><code>WE-MATH 2.0</code></a>.
      </td>
    </tr>
  </tbody>
</table>

> **Abbreviations.**
(1) **Metrics**: *AS* = Auto-Score.
(2) **Q-Type**: *OE* = Open-Ended Questions, *MC* = Multiple Choice Questions (Select all that apply).
(3) **Ann.**: *HA* = Human Annotation, *AA* = Auto-Annotation, *MV* = Manual Verification.

### <a id="bench-53-temporal--planning-reasoning"></a>5.3 Temporal & Planning Reasoning

<table>
  <thead>
    <tr>
      <th>Benchmark</th>
      <th>Year</th>
      <th>Size</th>
      <th>Metrics</th>
      <th>Q-Type</th>
      <th>Dom.</th>
      <th>Ann.</th>
      <th>Link</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td colspan="8"><i><b>Planning Reasoning</b></i></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2206.08853"><code>MineDojo</code></a></td>
      <td>2022</td>
      <td>-</td>
      <td>SR, F1 Score, COR</td>
      <td>MC</td>
      <td>Long-Term Planning</td>
      <td>HA</td>
      <td align="center"><a href="https://github.com/MineDojo/MineDojo"><img src="https://img.shields.io/badge/-181717?style=social&logo=github" alt="GitHub"></a></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2310.04671"><code>DHPR</code></a></td>
      <td>2024</td>
      <td>15K</td>
      <td>Avg. Rank of GT, NDCG</td>
      <td>OE</td>
      <td>Visual Abductive Rea.</td>
      <td>HA</td>
      <td align="center"><a href="https://huggingface.co/datasets/DHPR/Driving-Hazard-Prediction-and-Reasoning"><img src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg" alt="HF" width="18"></a></td>
    </tr>
    <tr>
      <td colspan="8"><i><b>Temporal Reasoning</b></i></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2406.11303"><code>Videovista</code></a></td>
      <td>2024</td>
      <td>24.9K</td>
      <td>Acc.</td>
      <td>MC</td>
      <td>Vid. Und. and Rea.</td>
      <td>AA + MV</td>
      <td align="center"><a href="https://huggingface.co/datasets/Uni-MoE/VideoVista"><img src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg" alt="HF" width="18"></a></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2411.14794"><code>VideoEspresso</code></a></td>
      <td>2024</td>
      <td>200K+</td>
      <td>Acc., AS </td>
      <td>OE</td>
      <td>Fine-Grained Vid. Rea.</td>
      <td>AA</td>
      <td align="center"><a href="https://huggingface.co/datasets/hshjerry0315/VideoEspresso-Test"><img src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg" alt="HF" width="18"></a></td>
    </tr>
    <tr>
      <td colspan="8">
        💖<b>Core Benchmarks (Milestone):</b><br>
        <a href="https://huggingface.co/datasets/Video-R1/Video-R1-data"><code>Video-R1-data</code></a>.
      </td>
    </tr>
    <tr>
      <td colspan="8"> 
        💕<b>Representative Benchmarks:</b><br>
        <a href="https://huggingface.co/datasets/ReXTime/ReXTime"><code>ReXTime</code></a>, <a href="https://huggingface.co/datasets/yale-nlp/TOMATO"><code>TOMATO</code></a>, <a href="https://arxiv.org/abs/2407.05355"><code>VideoCoT</code></a>, <a href="https://gewu-lab.github.io/Ref-AVS/"><code>RefAVS</code></a>, <a href="https://huggingface.co/datasets/Yuqi1997/DrivingDojo"><code>DrivingDojo</code></a>, <a href="https://huggingface.co/datasets/fazliimam/temporal-vqa"><code>TemporalVQA</code></a>.
      </td>
    </tr>
    <tr>
      <td colspan="8"> 
        ❤️<b>Other Benchmarks (Emerging):</b><br>
        <a href="https://github.com/jfliang3324/GUIDE"><code>GUIDE</code></a>, <a href="https://csu-jpg.github.io/V-MAGE/"><code>V-MAGE</code></a>, <a href="https://huggingface.co/datasets/kanxue/MuEP_Dataset"><code>MuEP</code></a>, <a href="https://github.com/zihuixue/ProgCaptioner"><code>FrameCap</code></a>, <a href="https://huggingface.co/datasets/wangphoebe/ActiView"><code>ActiView</code></a>, <a href="https://huggingface.co/datasets/dreilly/ADL-X"><code>ADL-X</code></a>, <a href="https://huggingface.co/datasets/JokerJan/MMR-VBench"><code>MMR-V</code></a>, <a href="https://huggingface.co/datasets/MBZUAI/VideoMathQA"><code>VideoMathQA</code></a>, <a href="https://huggingface.co/datasets/Dongyh35/CVBench"><code>CVBench</code></a>,
        <a href="https://arxiv.org/abs/2501.07214v1"><code>TLQA</code></a>, <a href="https://huggingface.co/datasets/RyanWW/Spatial457"><code>PulseCheck457</code></a>, <a href="https://huggingface.co/datasets/Uni-MoE/VideoVista-CulturalLingo"><code>VideoVista-CulturalLingo</code></a>.
      </td>
    </tr>
  </tbody>
</table>

> **Abbreviations.**
(1) **Metrics**: *AS* = Auto-Score, *SR* = Success Rate.
(2) **Q-Type**: *OE* = Open-Ended Questions, *MC* = Multiple Choice Questions (Select all that apply).
(3) **Ann.**: *HA* = Human Annotation, *AA* = Auto-Annotation, *MV* = Manual Verification.

### <a id="bench-54-tool-enhanced--embodied-reasoning"></a>5.4 Tool-Enhanced & Embodied Reasoning

<table>
  <thead>
    <tr>
      <th>Benchmark</th>
      <th>Year</th>
      <th>Size</th>
      <th>Metrics</th>
      <th>Q-Type</th>
      <th>Dom.</th>
      <th>Ann.</th>
      <th>Link</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td colspan="8"><i><b>GUI Navigation Reasoning</b></i></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2404.07972"><code>OSWorld</code></a></td>
      <td>2024</td>
      <td>0.4K</td>
      <td>Execution-Based SR</td>
      <td>IE</td>
      <td>GUI Navi.</td>
      <td>HA</td>
      <td align="center"><a href="https://github.com/xlang-ai/OSWorld"><img src="https://img.shields.io/badge/-181717?style=social&logo=github" alt="GitHub"></a></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2404.05955"><code>VisualWebBench</code></a></td>
      <td>2024</td>
      <td>1.5K</td>
      <td>ROUGE-L, SQuAD style F1, Acc.</td>
      <td>MC, OE</td>
      <td>Webpage Und.</td>
      <td>HA</td>
      <td align="center"><a href="https://huggingface.co/datasets/visualwebbench/VisualWebBench"><img src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg" alt="HF" width="18"></a></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2406.08451"><code>GUIOdysse</code></a></td>
      <td>2025</td>
      <td>7.7K</td>
      <td>Action Matching Score, SR</td>
      <td>IE</td>
      <td>Cross-App. GUI Navi.</td>
      <td>HA</td>
      <td align="center"><a href="https://huggingface.co/datasets/hflqf88888/GUIOdyssey"><img src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg" alt="HF" width="18"></a></td>
    </tr>
    <tr>
      <td colspan="8"><i><b>Embodied Robotics Reasoning</b></i></td>
    </tr>
    <tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2502.09560"><code>Embodiedbench</code></a></td>
      <td>2025</td>
      <td>1.1K</td>
      <td>Task SR, Subgoal SR, Avg. Steps</td>
      <td>IE</td>
      <td>Multi-Env. Embodied Rea.</td>
      <td>AA + HA</td>
      <td align="center"><a href="https://huggingface.co/EmbodiedBench"><img src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg" alt="HF" width="18"></a></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2503.15558"><code>Embodied Reasoning</code></a></td>
      <td>2025</td>
      <td>0.61K</td>
      <td>Acc.</td>
      <td>MC</td>
      <td>Embodied Rea.</td>
      <td>HA</td>
      <td align="center"><a href="https://huggingface.co/collections/nvidia/cosmos-reason1"><img src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg" alt="HF" width="18"></a></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2411.00081"><code>PARTNR</code></a></td>
      <td>2024</td>
      <td>100K</td>
      <td>SR, Steps, Percent Complete</td>
      <td>OE</td>
      <td>Embodied AI Collab.</td>
      <td>AA + MV</td>
      <td align="center"><a href="https://github.com/facebookresearch/partnr-planner/"><img src="https://img.shields.io/badge/-181717?style=social&logo=github" alt="GitHub"></a></td>
    </tr>
    <tr>
      <td colspan="8">
        💖<b>Core Benchmarks (Milestone):</b><br>
        <a href="https://aihabitat.org/"><code>Habitat</code></a>, <a href="https://ai2thor.allenai.org/"><code>AI2-THOR</code></a>, <a href="https://huggingface.co/datasets/osunlp/Mind2Web"><code>Mind2Web</code></a>, <a href="https://github.com/princeton-nlp/WebShop"><code>WebShop</code></a>, <a href="https://sapien.ucsd.edu/"><code>SAPIEN</code></a>, <a href="https://github.com/web-arena-x/webarena"><code>WebArena</code></a>, <a href="http://calvin.cs.uni-freiburg.de/"><code>CALVIN</code></a>, <a href="https://github.com/isaac-sim/IsaacLab"><code>Isaac Lab</code></a>, <a href="https://github.com/EmbodiedGPT/EgoCOT_Dataset"><code>EgoCoT</code></a>,
        <a href="https://svl.stanford.edu/igibson/"><code>iGibson 2.0</code></a>, <a href="https://github.com/njucckevin/SeeClick"><code>ScreenSpot</code></a>, <a href="https://procthor.allenai.org/"><code>ProcTHOR</code></a>, <a href="https://arxiv.org/abs/2404.05719"><code>Ferret-UI</code></a>, <a href="https://ovmm.github.io/"><code>HomeRobot</code></a>, <a href="https://github.com/samuelschmidgall/agentclinic"><code>AgentClinic</code></a>, <a href="https://holoassist.github.io/"><code>HoloAssist</code></a>.
      </td>
    </tr>
    <tr>
      <td colspan="8"> 
        💕<b>Representative Benchmarks:</b><br>
        <a href="https://github.com/StanfordVL/BEHAVIOR-1K"><code>BEHAVIOR-1K</code></a>, <a href="https://github.com/THUDM/VisualAgentBench"><code>VisualAgentBench</code></a>, <a href="https://huggingface.co/datasets/Writer/omniact"><code>OmniACT</code></a>, <a href="https://huggingface.co/datasets/ServiceNow/ui-vision"><code>UI-Vision</code></a>, <a href="https://github.com/LlamaTouch/LlamaTouch"><code>LlamaTouch</code></a>, <a href="https://huggingface.co/datasets/ONE-Lab/GUI-World"><code>GUI-World</code></a>,
        <a href="https://huggingface.co/declare-lab/Emma-X"><code>EMMA-X-Dataset</code></a>, <a href="https://github.com/InfiXAI/InfiGUIAgent"><code>InfiGUIAgent-Data</code></a>, <a href="https://huggingface.co/collections/IffYuan/embodied-r1"><code>Embodied-Points-200K</code></a>, <a href="https://github.com/microsoft/WindowsAgentArena"><code>Windows Agent Arena</code></a>.
      </td>
    </tr>
    <tr>
      <td colspan="8"> 
        ❤️<b>Other Benchmarks (Emerging):</b><br>
        <a href="https://github.com/JHKim-snu/GVCCI"><code>GVCCI</code></a>, <a href="https://huggingface.co/datasets/Tajamul21/Agent-X"><code>Agent-X</code></a>, <a href="https://github.com/xavihart/PIO"><code>Point-It-Out</code></a>, <a href="https://github.com/agentsea/osuniverse"><code>OSUniverse</code></a>, <a href="https://huggingface.co/datasets/wangzx1210/OmniEAR"><code>OmniEAR</code></a>.
      </td>
    </tr>
  </tbody>
</table>

> **Abbreviations.**
(1) **Metrics**: *SR* = Success Rate.
(2) **Q-Type**: *OE* = Open-Ended Questions, *MC* = Multiple Choice Questions (Select all that apply), *IE* = Instruction Execution.
(3) **Ann.**: *HA* = Human Annotation, *AA* = Auto-Annotation, *MV* = Manual Verification.

### <a id="bench-55-self-reflection-reasoning"></a>5.5 Self-Reflection Reasoning

<table>
  <thead>
    <tr>
      <th>Benchmark</th>
      <th>Year</th>
      <th>Size</th>
      <th>Metrics</th>
      <th>Q-Type</th>
      <th>Dom.</th>
      <th>Ann.</th>
      <th>Link</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td colspan="8"><i><b>Multi-Round Reasoning</b></i></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2411.10440"><code>LLava-CoT-100k</code></a></td>
      <td>2025</td>
      <td>99K</td>
      <td>Acc.</td>
      <td>MC, OE</td>
      <td>General, Science, Math, Hallucinatio</td>
      <td>AA</td>
      <td align="center"><a href="https://huggingface.co/datasets/Xkev/LLaVA-CoT-100k"><img src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg" alt="HF" width="18"></a></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2405.16473"><code>M<sup>3</sup>CoT</code></a></td>
      <td>2024</td>
      <td>11.9K</td>
      <td>Acc.</td>
      <td>SC, MR</td>
      <td>General, Science, Math</td>
      <td>AA + HA</td>
      <td align="center"><a href="https://huggingface.co/datasets/LightChen2333/M3CoT"><img src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg" alt="HF" width="18"></a></td>
    </tr>
    <tr>
      <td colspan="8"><i><b>Self-Reflection Reasoning</b></i></td>
    </tr>
    <tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2407.11422"><code>Reflective</code></a></td>
      <td>2024</td>
      <td>254K</td>
      <td>F1 Score, Acc., Hallucination Rate</td>
      <td>SC, YN, IE</td>
      <td>General, Hallucination</td>
      <td>AA + HA</td>
      <td align="center"><a href="https://huggingface.co/datasets/zjr2000/REVERIE"><img src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg" alt="HF" width="18"></a></td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2412.02172"><code>VISCO</code></a></td>
      <td>2024</td>
      <td>1.65K</td>
      <td>F1 Score, VISCore, Correction Gain</td>
      <td>OE</td>
      <td>General, Science, Math, Hallucination</td>
      <td>HA</td>
      <td align="center"><a href="https://huggingface.co/datasets/uclanlp/VISCO"><img src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg" alt="HF" width="18"></a></td>
    </tr>
    <tr>
      <td colspan="8">
        💖<b>Core Benchmarks (Milestone):</b><br>
        <a href="https://huggingface.co/datasets/MMInstruction/VLFeedback"><code>VLFeedback</code></a>.
      </td>
    </tr>
    <tr>
      <td colspan="8"> 
        💕<b>Representative Benchmarks:</b><br>
        <a href="https://huggingface.co/datasets/lhpku20010120/MM-Verify-Data"><code>MM-Verify</code></a>, <a href="https://huggingface.co/datasets/OpenGVLab/VisualPRM400K"><code>VisualPRM400K</code></a>, <a href="https://huggingface.co/conme/ConMe"><code>ConMe</code></a>, <a href="https://zhangyuanhan-ai.github.io/WorldQA/"><code>WorldQA</code></a>, <a href="https://huggingface.co/datasets/CaraJ/MME-CoT"><code>MME-CoT</code></a>, <a href="https://huggingface.co/datasets/jonathan-roberts1/zerobench"><code>ZeroBench</code></a>, <a href="https://huggingface.co/datasets/VLM-Reasoning/VCR-Bench"><code>VCR-Bench</code></a>,
        <a href="https://huggingface.co/datasets/MAmmoTH-VL/MAmmoTH-VL-Instruct-12M"><code>MAmmoTH-VL-Instruct</code></a>.
      </td>
    </tr>
    <tr>
      <td colspan="8"> 
        ❤️<b>Other Benchmarks (Emerging):</b><br>
        <a href="https://huggingface.co/datasets/rippleripple/MMIR"><code>MMIR</code></a>, <a href="https://huggingface.co/datasets/PengxiangLi/FIRE"><code>FIRE</code></a>, <a href="https://github.com/alenai97/MiCEval"><code>MiCEval</code></a>, <a href="https://huggingface.co/datasets/MindIntLab/MTMEUR"><code>MTMEUR</code></a>, <a href="https://github.com/Mingzhen-Huang/D-TIIL"><code>D-TIIL</code></a>, <a href="https://huggingface.co/datasets/VIS-MPU-Agent/MMAT-1M"><code>MMAT-1M</code></a>.
      </td>
    </tr>
  </tbody>
</table>

> **Abbreviations.**
(1) **Metrics**: *AS* = Auto-Score, *SR* = Success Rate.
(2) **Q-Type**: *OE* = Open-Ended Questions, *MC* = Multiple Choice Questions (Select all that apply), *IE* = Instruction Execution, *MR* = Multi-step Reasoning, *SC* = Single Choice Questions, *YN* = Yes-No Questions.
(3) **Ann.**: *HA* = Human Annotation, *AA* = Auto-Annotation, *MV* = Manual Verification.


## 6. Challenges & Opportunities

### 6.1 The Foundational Substrate of Multimodal Reasoning

:triangular_flag_on_post: **Multimodal Reward Fuzziness**

  *How to eliminate the impact of noise, marking a shift from rigid scoring to interference- resistant rewards.*

  - [ ] Enhancing multimodal rewards with dense soft-reward mechanisms.
  - [ ] Counterfactual alignment verification.

:triangular_flag_on_post: **Cross-Modal Credit Assignment Inadequacy**

  *How to decouple the reasoning process, marking a shift from black-box reasoning to controllable and interpretable hierarchical reasoning.*

  - [ ] Hierarchical reinforcement learning.
  - [ ] Process labeling.
  - [ ] Interpretability evaluation.

:triangular_flag_on_post: **Error accumulation**

  *How to detect and track accumulated errors, marking a shift from passive failure logging to active self-correction.*

  - [ ] Checkpoint evaluation.
  - [ ] Verification–rollback.

:triangular_flag_on_post: **Modal Imbalance**

  *How to mitigate unbalanced contributions, marking a shift from text-dominant learning to balanced learning.*

  - [ ] Modality-wise decomposition of rewards and advantages.
  - [ ] Process reward models for modality verification.
  - [ ] Expert-based decision structures.

### 6.2 Ground-Truth Feedback and Evidential Reliability

:triangular_flag_on_post: **Fragmentation of Benchmarks**

  *How to evaluate the benefits of RL and feed them back into algorithm design, marking a shift from reasoning outcome evaluation to reasoning algorithm evaluation.*

  - [ ] Developing a unified capability taxonomy aligned with RL paradigms.
  - [ ] Establishing process-oriented evaluation protocols.

:triangular_flag_on_post: **Beyond Linear If-Then Reasoning**

  *How to shift multimodal reasoning from correlation-driven reasoning to causal reasoning grounded in RL.*

  - [ ] Structured RL training for analogical reasoning.
  - [ ] Causal state extraction for multimodal MDPs.
  - [ ] Intervention-driven training signals.

> :eight_pointed_black_star: **Supplementary Remark**: 
> RL renders open-ended **multimodal abstract reasoning**, characterized by its dispersed evidence, and difficult evaluation, amenable to systematic optimization.
> - [ ] Shift from data collection to controlled synthesis and preference construction.
> - [ ] Shift from a linear state representation to a structured state graph.
> - [ ] Shift from single-metric to multi-dimensional preference evaluation.

:triangular_flag_on_post: **Catastrophic Forgetting**

  *How to relieve multimodal forgetting under RL-centric post-training, and feed retention signals back into optimization and data curation, marking a shift from single-capability retention checks to joint-distribution preservation across perception–alignment–reasoning–tool use.*

  - [ ] Retention-aware on-policy (or near on-policy) multimodal data pipelines.
  - [ ] Continual RL for long-term multimodal reasoning with memory and retention guarantees.

### 6.3 Continuous Catalysis and the Engine of Progress

:triangular_flag_on_post: **Absence of Environmental Feedback**

  *how to integrate real-time environmental feedback, marking a shift from simulation environments to real-world deployment.*

  -[ ] Environment-aligned multi-source rewards.
  -[ ] Narrowing the sim-to-real gap.
  -[ ] Budget-constrained policy optimization under real-time constraints.

:triangular_flag_on_post: **Multimodal Multi-Agent**

  *how to simultaneously realize a plan representation that is executable, process-level evaluation that is verifiable, and coordination strategies that are learnable within a multimodal MDP.*

  - [ ] Execution-plan-centric agent capability building.
  - [ ] Imagination-based collaboration with world models.


## Citation


```bibtex
@article{Key,
  title={Steer, Assess, and Refine: A Reinforcement Learning-Centric Multimodal Reasoning Survey},
  author={...},
  journal={...},
  year={2026}
}
