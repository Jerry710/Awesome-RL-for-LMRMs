# Awesome-RL-for-LMRMs

<div align="center">

<img src="figures/survey_logo.png" style="width: 70%;"/>

## Control, Evaluate, and Improve: A Reinforcement Learning-Centric Multimodal Reasoning Survey

[![Awesome](https://img.shields.io/badge/Awesome-0066CC?style=flat&logo=awesome-lists&logoColor=white)](https://github.com/sindresorhus/awesome) 
[![Survey](https://img.shields.io/badge/Paper-A42C25?style=flat&logo=arxiv&logoColor=white)](#) 
[![Github](https://img.shields.io/badge/Awesome--RL--for--LRMs-000000?style=flat&logo=github&logoColor=white)](https://github.com/Jerry710/Awesome-RL-for-LMRMs) 
[![HF Papers](https://img.shields.io/badge/🤗%20Paper-%23FFD14D?style=flat)]() 
[![Twitter](https://img.shields.io/badge/Twitter-%23000000.svg?style=flat&logo=x&logoColor=white)]( )

</div>

> 💡 *You're very welcome to join our discussion (on WeChat or Slack) on the topic of multimodal reasoning.*  
> 📌 *Please feel free to ping us for any possibly missed related work.*

---

## 🔔 News

- **2025-11-XX**: Repository initialized.

---

## 🧭 Overview

<p align="center">
  <img src="figures\Fig-1.png" width="80%" />
<!--   <img src="./Images/methods.jpg" width="45%" height="50%" /> -->
</p>

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
      <td>🧩 <a href="#2-cei-framework-gpi-view">2. CEI Framework</a></td>
      <td colspan="2">
        <a href="#control">Control</a> · <a href="#evaluate">Evaluate</a> · <a href="#improve">Improve</a>
      </td>
    </tr>
    <tr>
      <td>🏗️ <a href="#3-train-time-optimization">3. Train-time Optimization</a></td>
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
      <td>🧠 <a href="#4-test-time-inference-of-RL-centric-multimodal-reasoning">4. Test-time Inference of RL-centric Multimodal Reasoning</a></td>
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
      <td>🎖 <a href="#-5-datasets--benchmarks"> 5. Datasets &amp; Benchmarks</a></td>
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
  </tbody>
</table>


---



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
:one: Sections 3 and 4 follow the CEI framework systematically review and compare methods in the training and testing phases under a unified GPI perspective. This
establishes an integrated framework and clarifies the inter relationship between the two phases.

:two: Section 5 introduces a novel RL-based benchmark taxonomy, achieving a CEI-aligned restructuring of multimodal reasoning benchmarks.

:three: Section 6 explores the challenges and future directions of RL-centric multimodal reasoning, with a particular emphasis on the intrinsic coupling between RL mechanisms and multimodal scenarios.


## 2. CEI Framework
### <a id="control"></a>Control
### <a id="evaluate"></a>Evaluate
### <a id="improve"></a>Improve

## 3. Train-time Optimization
### <a id="train-31--training-initialization"></a>3.1 Training Initialization

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



| Date | Name | Title | Paper | Github |
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




### <a id="train-32-reward-modeling"></a>3.2 Reward Modeling
Summary of reward modeling in RL-centric MLRMs, organized by reward channel. For each method we report the input modalities, multimodal reasoning characteristics, feedback granularity, optimization target, reward type, evaluation type, initialization, learning algorithm, and tasks.

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
      <th>MLRM</th>
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
      <td>Curr-ReFT <br>
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
      <td>MedVLThinker<br><a href="https://arxiv.org/abs/2508.02669">
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
      <td>R1-VL<br><a href="https://arxiv.org/abs/2503.12937">
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
      <td>GRIT<br><a href="https://arxiv.org/abs/2505.15879">
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
      <td>Kimi k1.5<br><a href="https://arxiv.org/abs/2501.12599">
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
      <td>Visionary-R1<br><a href="https://arxiv.org/abs/2505.14677">
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
      <td>Geoint-R1<br><a href="https://arxiv.org/abs/2508.03173">
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
      <td>R1-SGG<br><a href="https://arxiv.org/abs/2504.13617">
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
      <td>VideoChat-R1<br><a href="https://arxiv.org/abs/2504.06958">
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
      <td>MetaSpatial<br><a href="https://arxiv.org/abs/2503.18470">
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
      <td>ChestX-Reasoner<br><a href="https://arxiv.org/abs/2504.20930">
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
      <td>GoT-R1<br><a href="https://arxiv.org/abs/2505.17022">
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
      <td>StructVRM<br><a href="https://arxiv.org/abs/2508.05383">
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
      <td>DeepEyes<br><a href="https://arxiv.org/abs/2505.14362">
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
      <td>STAR-R1<br><a href="https://arxiv.org/abs/2505.15804">
          <img src="https://img.shields.io/badge/arXiv-b31b1b.svg" alt="arXiv">
        </a>
        <a href="https://github.com/zongzhao23/STAR-R1">
          <img src="https://img.shields.io/github/stars/zongzhao23/STAR-R1?style=social" alt="Stars">
        </a></td>
      <td>Spat., Ground</td>
      <td>Traj, Field</td>
      <td>Out.-Acc., Struct-Form</td>
      <td>PRM</td>
      <td>RL</td>
      <td>R</td>
      <!-- <td>GRPO</td> -->
      <td>Spatial Transformation Rea.</td>
    </tr>
    <tr>
      <td>DanceGRPO<br><a href="https://arxiv.org/abs/2505.07818">
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
      <td>TimeMaster<br><a href="https://arxiv.org/abs/2506.13705">
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
      <td>Mixed-R1<br><a href="https://arxiv.org/abs/2505.24164">
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
      <td>Relation-R1<br><a href="https://arxiv.org/abs/2504.14642">
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
      <td>T2I-R1<br><a href="https://arxiv.org/abs/2505.00703">
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
      <td>SophiaVL-R1<br><a href="https://arxiv.org/abs/2505.17018">
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
      <td>Generative RLHF-V<br><a href="https://arxiv.org/abs/2505.18531">
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
      <td>SaFeR-VLM<br><a href="https://arxiv.org/abs/2510.06871">
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
      <td>Intern-S1<br><a href="https://arxiv.org/abs/2508.15763">
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




### <a id="train-33-trajectory-sampling"></a>3.3 Trajectory Sampling

Sampling governs how the policy generates reasoning trajectories for exploration and learning. Multimodal reasoning often requires explicit control over diversity, reasoning depth, task adaptability, and input distribution coverage. We group training-time sampling into four strategies:

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
### <a id="test-41-sampling"></a>4.1 Sampling

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

:diamond_shape_with_a_dot_inside: []() [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)]() [![GitHub Stars](https://img.shields.io/github/stars/?style=social&label=Star)]() 


### <a id="test-43-dynamic-verification"></a>4.3 Dynamic Verification

:diamond_shape_with_a_dot_inside: []() [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)]() [![GitHub Stars](https://img.shields.io/github/stars/?style=social&label=Star)]() 

### <a id="test-44-trajectory-optimization"></a>4.4 Trajectory Optimization

:diamond_shape_with_a_dot_inside: []() [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)]() [![GitHub Stars](https://img.shields.io/github/stars/?style=social&label=Star)]() 


## 🎖 5. Datasets & Benchmarks
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
    <td colspan="8"><i><b><span style="color:blue;">General Visual Reasoning</span></b></i></td>
  </tr>
  <tbody>
    <tr>
      <td>MMBench</td>
      <td>2024</td>
      <td>3.2K</td>
      <td>Acc., CircularEval</td>
      <td>MC</td>
      <td>General</td>
      <td>HA + AA</td>
      <td>🤗</td>
    </tr>
    <tr>
      <td>MMMU</td>
      <td>2024</td>
      <td>11.5K</td>
      <td>Acc.</td>
      <td>MC, OE</td>
      <td>Interdisciplinary</td>
      <td>HA</td>
      <td>🤗</td>
    </tr>
    <tr>
      <td>AGIEval</td>
      <td>2024</td>
      <td>8K</td>
      <td>Acc., F1 Score, Exact Match</td>
      <td>MC, OE</td>
      <td>Exams</td>
      <td>AA</td>
      <td>🤗</td>
    </tr>
    <tr>
      <td>HallusionBench</td>
      <td>2024</td>
      <td>0.2K</td>
      <td>Acc., AS (GPT4)</td>
      <td>OE</td>
      <td>Robustness</td>
      <td>HA</td>
      <td>🤗</td>
    </tr>
    <tr>
      <td colspan="8"><i><b><span style="color:#32a7f7;">Structured and Task-Specific Reasoning</span></b></i></td>
    </tr>
    <tr>
      <td>STAR</td>
      <td>2024</td>
      <td>60K</td>
      <td>Acc.</td>
      <td>MC</td>
      <td>Situational Rea.</td>
      <td>AA + HA</td>
      <td>🤗</td>
    </tr>
    <tr>
      <td>Multimodal RewardBench</td>
      <td>2025</td>
      <td>5.2K</td>
      <td>Acc.</td>
      <td>MC, OE</td>
      <td>General, Safety</td>
      <td>HA</td>
      <td>🤗</td>
    </tr>
    <tr>
      <td colspan="8">
        💖<span style="color:#32a7f7;"><b>Core Benchmarks (Milestone):</b></span><br>
        Visual Genome [248], A-OKVQA [249], ScienceQA [330], SEED-bench [331], Blink [332],
        SpatialEval [333], Mulberry-260K [190], Visual-RFT [52].
      </td>
    </tr>
    <tr>
      <td colspan="8"> 
        💕<span style="color:#32a7f7;"><b>Representative Benchmarks:</b></span><br>
        T-SoQ [334], Sherlock [335], VL-GPT [336], AttCoSeg [337], MM-Vet v2 [338],
        MMBench [39], MM-SPA [340], CoMT [341], AVTrustBench [342], ProVision [343],
        VL-RewardBench [252], MMMU [344], AVHBench [345], ShareGPT-4o-Image [346],
        PCA-Bench [347], MAGIC-VQA [348], Mmi-q [251], MAVIS [349], II-Bench [350],
        MicroVQA [351], GeoComp [352].
      </td>
    </tr>
    <tr>
      <td colspan="8"> 
        ❤️<font color="#32a7f7"><b>Other Benchmarks (Emerging):</b></font><br>
        VERIFY [353], FineCops-Ref [354], FIND-Bench [355], CompCap [356], CapQA [250],
        Ksavir-VQA-x1 [357], MMRB [358], MMESGBench [359], GUIDE [282], SMIR [360],
        CII-Bench [361], MAGEBench [362], PunchBench [363], MV-CoRe [364],
        JourneyBench [365], VisuRiddles [366].
      </td>
    </tr>
  </tbody>
</table>




### <a id="bench-52-causal--verifiable-reasoning"></a>5.2 Causal & Verifiable Reasoning 

| Date | Name | Title | Paper | Github |
|:-:|:-:|:-|:-:|:-:|
| 2025-08 | `Intern-S1` | Intern-S1: A Scientific Multimodal Foundation Model | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2508.15763v1) | [![GitHub Stars](https://img.shields.io/github/stars/InternLM/Intern-S1?style=social&label=Star)](https://github.com/InternLM/Intern-S1) |


### <a id="bench-53-temporal--planning-reasoning"></a>5.3 Temporal & Planning Reasoning

| Date | Name | Title | Paper | Github |
|:-:|:-:|:-|:-:|:-:|
| 2025-08 | `Intern-S1` | Intern-S1: A Scientific Multimodal Foundation Model | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2508.15763v1) | [![GitHub Stars](https://img.shields.io/github/stars/InternLM/Intern-S1?style=social&label=Star)](https://github.com/InternLM/Intern-S1) |

### <a id="bench-54-tool-enhanced--embodied-reasoning"></a>5.4 Tool-Enhanced & Embodied Reasoning

| Date | Name | Title | Paper | Github |
|:-:|:-:|:-|:-:|:-:|
| 2025-08 | `Intern-S1` | Intern-S1: A Scientific Multimodal Foundation Model | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2508.15763v1) | [![GitHub Stars](https://img.shields.io/github/stars/InternLM/Intern-S1?style=social&label=Star)](https://github.com/InternLM/Intern-S1) |


### <a id="bench-55-self-reflection-reasoning"></a>5.5 Self-Reflection Reasoning

| Date | Name | Title | Paper | Github |
|:-:|:-:|:-|:-:|:-:|
| 2025-08 | `Intern-S1` | Intern-S1: A Scientific Multimodal Foundation Model | [![Paper](https://img.shields.io/badge/arXiv-b31b1b.svg)](https://arxiv.org/abs/2508.15763v1) | [![GitHub Stars](https://img.shields.io/github/stars/InternLM/Intern-S1?style=social&label=Star)](https://github.com/InternLM/Intern-S1) |


---


## Citation


```bibtex
@article{Key,
  title={...},
  author={...},
  journal={...},
  year={2025}
}
