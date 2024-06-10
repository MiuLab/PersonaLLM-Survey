# Two Tales of Persona in LLMs: <br> A Survey of Role-Playing and Personalization

[![Static Badge](https://img.shields.io/badge/arXiv-2406.01171-b31b1b?logo=arXiv)](https://arxiv.org/abs/2406.01171)
![GitHub Repo stars](https://img.shields.io/github/stars/MiuLab/PersonaLLM-Survey?style=flat&logo=GitHub)
![GitHub last commit](https://img.shields.io/github/last-commit/MiuLab/PersonaLLM-Survey?path=README.md&style=flat&logo=GitHub)


<br>
<p align="center">
  <img src="figures/Overview.png" alt="Overview" width="40%" height="auto">
</p>


## Introduction
This is the official repository of the paper ["*Two Tales of Persona in LLMs: A Survey of Role-Playing and Personalization*"](https://arxiv.org/abs/2406.01171).

Recently, methods investigating how to adapt large language models (LLMs) for specific scenarios have gained great attention. Particularly, the concept of *persona*, originally adopted in dialogue literature, has re-surged as a promising avenue. However, the growing research on persona is relatively disorganized, lacking a systematic overview. To close the gap, we present a comprehensive survey to categorize the current state of the field. We identify two lines of research, namely (1) *LLM Role-Playing*, where personas are assigned to LLMs, and (2) *LLM Personalization*, where LLMs take care of user personas. To the best of our knowledge, we present the first survey tailored for LLM role-playing and LLM personalization under the unified view of persona, including taxonomy, current challenges, and potential directions.

To foster future endeavors, we actively maintain this paper collection for the community.


<div style="display: flex; align-items: center;">
<div style="flex: 1;">


## News
- [2024.06.04] :rocket: Our paper is now available on [arXiv](https://arxiv.org/abs/2406.01171) and the reading list on [GitHub](https://github.com/MiuLab/PersonaLLM-Survey).



## Table of Contents
- [🙆‍♀️ LLM Role-Play (Adapt to Environment)](#llm-role-play-adapt-to-environment)
  - [💼 Workshops](#role-playing-workshops)
  - [🌎 Environments](#environments)
    - [💻 Software Development](#software-development)
    - [🌐 Web](#web)
    - [🎮 Game](#game)
    - [🏥 Medical Application](#medical-application)
    - [🧑‍⚖️ LLM as Evaluators](#llm-as-evaluators)
    - [📦 General Framework](#general-framework)
  - [🤖 Agentic Interactions](#agentic-interactions)
    - [📊 Schemas](#schemas)
      - [👤 Single-Agent](#single-agent)
      - [👥 Multi-Agent](#multi-agent)
    - [💡 Emergent Behaviors](#emergent-behaviors)

- [🙆‍♂️ LLM Personalization (Adapt to User)](#llm-personalization-adapt-to-user)
  - [💼 Workshops & Competitions](#personalization-workshops)
  - [📌 Tasks](#tasks)
    - [💬 Personalized Dialogue](#personalized-dialogue)
      - [🔧 ToD Modeling](#tod-modeling)
      - [📝 User Persona Modeling](#user-persona-modeling)
    - [🛒 Recommendation System](#recommendation-system)
    - [🔍 Personalized Search](#personalized-search)
    - [🩺 Personalized Healthcare](#personalized-healthcare)
    - [📚 Personalized Education](#personalized-education)
  - [🛠️ Methods](#methods)
    - [🎛️ Fine-Tuning](#fine-tuning)
    - [🔗 Retrieval Augmentation](#retrieval-augmentation)
    - [✍️ Prompting](#prompting)
      - [📄 Vanilla Personalized Prompt](#vanilla-personalized-prompt)
      - [🔦 Retrieval-Augmented Personalized Prompt](#retrieval-augmented-personalized-prompt)
      - [📂 Profile-Augmented Prompt](#profile-augmented-prompt)

- [🧐 LLM Personality Evaluation](#llm-personality-evaluation)
- [🌱 How to contribute](#how-to-contribute)
- [🔖 Citation](#citation)
- [🖌️ Authors](#authors)




<h2 id="llm-role-play-adapt-to-environment">🙆‍♀️ LLM Role-Play (Adapt to Environment)</h2>

LLMs are tasked to play the assigned personas (i.e., roles) and act accordance to environmental feedback.

The key aspect is *how LLMs adapt to defined environments*.

<br>
<p align="center">
  <a href=".">
    <img src="figures/llm-role-playing.png" alt="LLM role-playing" width="80%" height="auto">
  </a>
</p>


<h3 id="role-playing-workshops">💼 Workshops</h3>

| Date  |  Workshop |                                                            Website Link                                                             |
|:-----:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2405 |   LLMAgent @ ICLR   |  [ICLR 2024 Workshop on Large Language Model (LLM) Agents](https://llmagents.github.io/)   |
| 2405 |   Agent Workshop @ CMU   |  [CMU Agent Workshop 2024](https://cmu-agent-workshop.github.io/)   |



<h3 id="environments">🌎 Environments</h3>

<h4 id="software-development">💻 Software Development</h4>

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2308 |    Hong et al.    |   ICLR    |  [MetaGPT: Meta Programming for Multi-Agent Collaborative Framework](https://arxiv.org/abs/2308.00352)   |
| 2307 |    Qian et al.    |   arXiv   |  [Communicative agents for software development](https://arxiv.org/abs/2307.07924)   |
| 2305 |    Dong et al.    |   TOSEM   |  [Self-collaboration code generation via chatgpt](https://arxiv.org/abs/2304.07590)   |
| 2107 |    Chen et al.    |   arXiv   |  [Evaluating large language models trained on code](https://arxiv.org/abs/2107.03374)   |


<h4 id="web">🌐 Web</h4>


| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2404 |    Liu et al.  |   arXiv   |  [VisualWebBench: How Far Have Multimodal LLMs Evolved in Web Page Understanding and Grounding?](https://arxiv.org/abs/2404.05955v1)   |
| 2401 |    Zheng et al.  |   LLMAgent @ ICLR   |  [GPT-4V(ision) is a Generalist Web Agent, if Grounded](https://arxiv.org/abs/2401.01614)   |
| 2401 |    Koh et al.   |   LLMAgent @ ICLR   |  [VisualWebArena: Evaluating Multimodal Agents on Realistic Visual Web Tasks](https://arxiv.org/abs/2401.13649)   |
| 2401 |    Cheng et al.    |   LLMAgent @ ICLR   |  [SeeClick: Harnessing GUI Grounding for Advanced Visual GUI Agents](https://arxiv.org/abs/2401.10935)   |
| 2312 |    Gur et al.    |   EMNLP   |  [Understanding HTML with Large Language Models](https://aclanthology.org/2023.findings-emnlp.185/)   |
| 2312 |    Hong et al.    |   arXiv   |  [CogAgent: A Visual Language Model for GUI Agents](https://arxiv.org/abs/2312.08914)   |
| 2307 |    Gur et al.    |   ICLR   |  [A Real-World WebAgent with Planning, Long Context Understanding, and Program Synthesis](https://arxiv.org/abs/2307.12856)   |
| 2307 |    Zhou et al.    |   ICLR   |  [WebArena: A Realistic Web Environment for Building Autonomous Agents](https://arxiv.org/abs/2307.13854)   |
| 2306 |    Deng et al.    |   NeurIPS   |  [Mind2web: Towards a generalist agent for the web](https://arxiv.org/abs/2306.06070)   |
| 2303 |    Kim et al.    |   NeurIPS   |  [Language Models can Solve Computer Tasks](https://arxiv.org/abs/2303.17491)   |


<h4 id="game">🎮 Game</h4>

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2310 |    Wang et al.    |   EMNLP   |  [Humanoid Agents: Platform for Simulating Human-like Generative Agents](https://arxiv.org/abs/2310.05418)   |
| 2305 |    Wang et al.    |   TMLR   |  [Voyager: An open-ended embodied agent with large language models](https://arxiv.org/abs/2305.16291)   |
| 2305 |    Fu et al.    |   arXiv   |  [Improving Language Model Negotiation with Self-Play and In-Context Learning from AI Feedback](https://arxiv.org/abs/2305.10142)   |
| 2304 |    Park et al.    |   UIST   |  [Generative agents: Interactive simulacra of human behavior](https://arxiv.org/abs/2304.03442)   |


<h4 id="medical-application">🏥 Medical Application</h4>

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2311 |    Tang et al.    |   arXiv   |  [Medagents: Large language models as collaborators for zero-shot medical reasoning](https://arxiv.org/abs/2311.10537)   |
| 2307 |    Wu et al.    |   ICLR   |  [Large Language Models Perform Diagnostic Reasoning](https://arxiv.org/abs/2307.08922)   |
| 2207 |    Liévin et al.    |   arXiv   |  [Can large language models reason about medical questions?](https://arxiv.org/abs/2207.08143)   |


<h4 id="llm-as-evaluators">🧑‍⚖️ LLM as Evaluators</h4>

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2308 |    Chan et al.    |   ICLR   |  [ChatEval: Towards Better LLM-based Evaluators through Multi-Agent Debate](https://arxiv.org/abs/2308.07201)   |
| 2303 |    Wu et al.    |   NLPCC   |  [Large Language Models are Diverse Role-Players for Summarization Evaluation](https://arxiv.org/abs/2303.15078)   |


<h4 id="general-framework">📦 General Framework</h4>

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2308 |    Chen et al.    |   ICLR   |  [AgentVerse: Facilitating Multi-Agent Collaboration and Exploring Emergent Behaviors](https://arxiv.org/abs/2308.10848)   |
| 2307 |    Wang et al.    |   NAACL   |  [Unleashing the Emergent Cognitive Synergy in Large Language Models: A Task-Solving Agent through Multi-Persona Self-Collaboration](https://arxiv.org/abs/2307.05300)   |
| 2303 |    Li et al.    |   NeurIPS   |  [CAMEL: Communicative Agents for "Mind" Exploration of Large Language Model Society](https://arxiv.org/abs/2303.17760)   |
| 2405  |    Ahn, et al    |   ACL Findings   |  [TimeChara: Evaluating Point-in-Time Character Hallucination of Role-Playing Large Language Models](https://arxiv.org/abs/2405.18027)   |


<h3 id="agentic-interactions">🤖 Interaction & Behaviors</h3>

<h4 id="schemas">📊 Schemas</h4>

<h5 id="single-agent">👤 Single-Agent</h5>

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2401 |    Cheng et al.    |   LLMAgent @ ICLR   |  [SeeClick: Harnessing GUI Grounding for Advanced Visual GUI Agents](https://arxiv.org/abs/2401.10935)   |
| 2401 |    Zheng et al.  |   LLMAgent @ ICLR   |  [GPT-4V(ision) is a Generalist Web Agent, if Grounded](https://arxiv.org/abs/2401.01614)   |
| 2312 |    Hong et al.    |   arXiv   |  [CogAgent: A Visual Language Model for GUI Agents](https://arxiv.org/abs/2312.08914)   |
| 2305 |    Wang et al.    |   TMLR   |  [Voyager: An open-ended embodied agent with large language models](https://arxiv.org/abs/2305.16291)   |


<h5 id="multi-agent">👥 Multi-Agent</h5>


| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2311 |    Tang et al.    |   arXiv   |  [Medagents: Large language models as collaborators for zero-shot medical reasoning](https://arxiv.org/abs/2311.10537)   |
| 2308 |    Chen et al.    |   ICLR   |  [AgentVerse: Facilitating Multi-Agent Collaboration and Exploring Emergent Behaviors](https://arxiv.org/abs/2308.10848)   |
| 2308 |    Hong et al.    |   ICLR    |  [MetaGPT: Meta Programming for Multi-Agent Collaborative Framework](https://arxiv.org/abs/2308.00352)   |
| 2308 |    Chan et al.    |   ICLR   |  [ChatEval: Towards Better LLM-based Evaluators through Multi-Agent Debate](https://arxiv.org/abs/2308.07201)   |
| 2307 |    Qian et al.    |   arXiv   |  [Communicative agents for software development](https://arxiv.org/abs/2307.07924)   |
| 2305 |    Fu et al.    |   arXiv   |  [Improving Language Model Negotiation with Self-Play and In-Context Learning from AI Feedback](https://arxiv.org/abs/2305.10142)   |


<h4 id="emergent-behaviors">💡 Emergent Behaviors</h4>


| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2311 |    Tang et al.    |   arXiv   |  [Medagents: Large language models as collaborators for zero-shot medical reasoning](https://arxiv.org/abs/2311.10537)   |
| 2308 |    Chen et al.    |   ICLR   |  [AgentVerse: Facilitating Multi-Agent Collaboration and Exploring Emergent Behaviors](https://arxiv.org/abs/2308.10848)   |
| 2307 |    Wang et al.    |   NAACL   |  [Unleashing the Emergent Cognitive Synergy in Large Language Models: A Task-Solving Agent through Multi-Persona Self-Collaboration](https://arxiv.org/abs/2307.05300)   |
| 2305 |    Fu et al.    |   arXiv   |  [Improving Language Model Negotiation with Self-Play and In-Context Learning from AI Feedback](https://arxiv.org/abs/2305.10142)   |
| 2303 |    Li et al.    |   NeurIPS   |  [CAMEL: Communicative Agents for "Mind" Exploration of Large Language Model Society](https://arxiv.org/abs/2303.17760)   |



<h2 id="llm-personalization-adapt-to-user">🙆‍♂️ LLM Personalization (Adapt to User)</h2>

LLMs are tasked to take care of users’ personas (e.g., background information, or historical behaviors) to meet customized needs.

The key aspect is *how LLMs adapt to distinct users*.


<p align="center">
  <a href=".">
    <img src="figures/llm-personalization.png" alt="LLM personalization" width="80%" height="auto">
  </a>
</p>



<h3 id="personalization-workshops">💼 Workshops & Competitions</h3>

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2403 |    Deshpande et al.    |   PERSONALIZE @ EACL   |  [Proceedings of the 1st Workshop on Personalization of Generative AI Systems (PERSONALIZE 2024)](https://aclanthology.org/volumes/2024.personalize-1/)   |
| 2310 |    Chen et al.    |   Personalized Generative AI @ CIKM   |  [The First Workshop on Personalized Generative AI @ CIKM 2023: Personalization Meets Large Language Models](https://dl.acm.org/doi/abs/10.1145/3583780.3615314)   |
| 1902 |    Dinan et al.    |   ConvAI2 @ NeurIPS   |  [The Second Conversational Intelligence Challenge (ConvAI2)](https://arxiv.org/abs/1902.00098)   |
| 1808 |    Yusupov et al. |   ConvAI @ NeurIPS   |  [NIPS Conversational Intelligence Challenge 2017 Winner System: Skill-based Conversational Agent with Supervised Dialog Manager](https://aclanthology.org/C18-1312/)   |


<h3 id="tasks">📌 Tasks</h3>


<h4 id="personalized-dialogue">💬 Personalized Dialogue</h4>

<h5 id="tod-modeling">🔧 ToD Modeling</h5>

LLMs Era

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2305 |    Yang et al.    |   EMNLP   |  [RefGPT: Dialogue Generation of GPT, by GPT, and for GPT](https://aclanthology.org/2023.findings-emnlp.165/)   |
| 2302 |    Li et al.    |   NeurIPS   |  [Guiding large language models via directional stimulus prompting](https://arxiv.org/abs/2302.11520)   |
| 2005 |    Hosseini-Asl et al.    |   NeurIPS   |  [A Simple Language Model for Task-Oriented Dialogue](https://arxiv.org/abs/2005.00796)   |


<details>
<summary style="color:#FFB6C1">Comprehensive Paper List</summary>

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2312 |    Xu et al.    |   EMNLP   |  [Baize: An Open-Source Chat Model with Parameter-Efficient Tuning on Self-Chat Data](https://aclanthology.org/2023.emnlp-main.385/)   |
| 2309 |    Hu et al.    |   arXiv   |  [Enhancing Large Language Model Induced Task-Oriented Dialogue Systems Through Look-Forward Motivated Goals](https://arxiv.org/abs/2309.08949)   |
| 2308 |    Wu et al.    |   SIGDIAL   |  [DiactTOD: Learning Generalizable Latent Dialogue Acts for Controllable Task-Oriented Dialogue Systems](https://aclanthology.org/2023.sigdial-1.24.pdf)   |
| 2305 |    Yang et al.    |   EMNLP   |  [RefGPT: Dialogue Generation of GPT, by GPT, and for GPT](https://aclanthology.org/2023.findings-emnlp.165/)   |
| 2305 |    Bang et al.    |   ACL   |  [Task-Optimized Adapters for an End-to-End Task-Oriented Dialogue System](https://aclanthology.org/2023.findings-acl.464/)   |
| 2304 |    Ashby et al.    |   CHI   |  [Personalized Quest and Dialogue Generation in Role-Playing Games: A Knowledge Graph and Language Model-based Approach](https://dl.acm.org/doi/10.1145/3544548.3581441)   |
| 2304 |    Hudevcek et al.    |   SIGDIAL   |  [Are Large Language Models All You Need for Task-Oriented Dialogue?](https://aclanthology.org/2023.sigdial-1.21/)   |
| 2302 |    Li et al.    |   NeurIPS   |  [Guiding large language models via directional stimulus prompting](https://arxiv.org/abs/2302.11520)   |
| 2302 |    Feng et al.    |   ICLR   |  [Fantastic rewards and how to tame them: A case study on reward learning for task-oriented dialogue systems](https://arxiv.org/abs/2302.10342)   |
| 2210 |    Huryn et al.    |   COLING   |  [Automatic Generation of Large-scale Multi-turn Dialogues from Reddit](https://aclanthology.org/2022.coling-1.297/)   |
| 2108 |    Peng et al.    |   TACL   |  [Soloist: Building Task Bots at Scale with Transfer Learning and Machine Teaching](https://aclanthology.org/2021.tacl-1.49/)   |
| 2012 |    Yang et al.    |   AAAI   |  [UBAR: Towards Fully End-to-End Task-Oriented Dialog Systems with GPT-2](https://arxiv.org/abs/2012.03539)   |
| 2008 |    Madotto et al.    |   arXiv   |  [Language models as few-shot learner for task-oriented dialogue systems](https://arxiv.org/abs/2008.06239)   |
| 2005 |    Hosseini-Asl et al.    |   NeurIPS   |  [A Simple Language Model for Task-Oriented Dialogue](https://arxiv.org/abs/2005.00796)   |
</details>

---

Pre-LLMs Era

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2006 |    Jianhong Wang et al.    |   ICLR   |  [Modelling hierarchical structure between dialogue policy and natural language generator with option framework for task-oriented dialogue system](https://arxiv.org/abs/2006.06814)   |
| 1606 |    N. Mrksic et al.    |   ACL   |  [Neural Belief Tracker: Data-Driven Dialogue State Tracking](https://aclanthology.org/P17-1163/)   |
| 1506 |    Alessandro Sordoni et al.    |   NAACL   |  [A Neural Network Approach to Context-Sensitive Generation of Conversational Responses](https://aclanthology.org/N15-1020/)   |

<details>
<summary style="color:#FFB6C1">Comprehensive Paper List</summary>

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2105 |    Sun et al.    |   SIGIR   |  [Simulating user satisfaction for the evaluation of task-oriented dialogue systems](https://arxiv.org/abs/2105.03748)   |
| 2006 |    Wang et al.    |   ICLR   |  [Modelling hierarchical structure between dialogue policy and natural language generator with option framework for task-oriented dialogue system](https://arxiv.org/abs/2006.06814)   |
| 2003 |    Yang et al.    |   IEEE   |  [Multitask Learning and Reinforcement Learning for Personalized Dialog Generation: An Empirical Study](https://ieeexplore.ieee.org/abstract/document/9025776)   |
| 1912 |    Huang    |   AAAI   |  [MALA: Cross-Domain Dialogue Generation with Action Learning](https://arxiv.org/abs/1912.08442)   |
| 1910 |    Zhang et al.    |   *SEM   |  [Find or Classify? Dual Strategy for Slot-Value Predictions on Multi-Domain Dialog State Tracking](https://aclanthology.org/2020.starsem-1.17/)   |
| 1905 |    Wu et al.    |   ACL   |  [Transferable Multi-Domain State Generator for Task-Oriented Dialogue Systems](https://aclanthology.org/P19-1078/)   |
| 1807 |    Lei et al.    |   ACL   |  [Sequicity: Simplifying Task-oriented Dialogue Systems with Single Sequence-to-Sequence Architectures](https://aclanthology.org/P18-1133/)   |
| 1804 |    Liu et al.    |   NAACL   |  [Dialogue Learning with Human Teaching and Feedback in End-to-End Trainable Task-Oriented Dialogue Systems](https://aclanthology.org/N18-1187/)   |
| 1712 |    Rastogi et al.    |   IEEE   |  [Scalable Multi-Domain Dialogue State Tracking](https://arxiv.org/abs/1712.10224)   |
| 1709 |    Wu et al.    |   AAAI   |  [StarSpace: Embed all the things!](https://arxiv.org/abs/1709.03856)   |
| 1606 |    Miller et al.    |   EMNLP   |  [Key-Value Memory Networks for Directly Reading Documents](https://aclanthology.org/D16-1147/)   |
| 1606 |    Mrksic et al.    |   ACL   |  [Neural Belief Tracker: Data-Driven Dialogue State Tracking](https://aclanthology.org/P17-1163/)   |
| 1506 |    Sordoni et al.    |   NAACL   |  [A Neural Network Approach to Context-Sensitive Generation of Conversational Responses](https://aclanthology.org/N15-1020/)   |
</details>


<h5 id="user-persona-modeling">📝 User Persona Modeling</h5>

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2405 |    Han    |   ACL   |  [PSYDIAL: Personality-based Synthetic Dialogue Generation Using Large Language Models](https://aclanthology.org/2024.lrec-main.1166/)   |
| 2307 |    Tang et al.    |   ACL   |  [Enhancing Personalized Dialogue Generation with Contrastive Latent Variables: Combining Sparse and Dense Persona](https://aclanthology.org/2023.acl-long.299/)   |
| 1807 |    Zhang et al.    |   ACL   |  [Personalizing Dialogue Agents: I have a dog, do you have pets too?](https://aclanthology.org/P18-1205/)   |


<details>
<summary style="color:#FFB6C1">Comprehensive Paper List</summary>

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2405 |    Han    |   ACL   |  [PSYDIAL: Personality-based Synthetic Dialogue Generation Using Large Language Models](https://aclanthology.org/2024.lrec-main.1166/)   |
| 2401 |    Lotfi et al.    |   IEEE   |  [PersonalityChat: Conversation Distillation for Personalized Dialog Modeling with Facts and Traits](https://arxiv.org/abs/2401.07363)   |
| 2401 |    Kim et al.    |   EACL   |  [Commonsense-augmented Memory Construction and Management in Long-term Conversations via Context-aware Persona Refinement](https://arxiv.org/abs/2401.14215)   |
| 2308 |    Tu et al.    |   arXiv   |  [CharacterChat: Learning towards Conversational AI with Personalized Social Support](https://arxiv.org/abs/2308.10278)   |
| 2307 |    Tang et al.    |   ACL   |  [Enhancing Personalized Dialogue Generation with Contrastive Latent Variables: Combining Sparse and Dense Persona](https://aclanthology.org/2023.acl-long.299/)   |
| 2011 |    Zhong et al.    |   EMNLP   |  [Towards Persona-Based Empathetic Conversational Models](https://aclanthology.org/2020.emnlp-main.531/)   |
| 2007 |    Wu et al.    |   ACL   |  [Guiding Variational Response Generator to Exploit Persona](https://aclanthology.org/2020.acl-main.7/)   |
| 2007 |    Liu et al.    |   ACL   |  [You Impress Me: Dialogue Generation via Mutual Persona Perception](https://aclanthology.org/2020.acl-main.131/)   |
| 1911 |    Zheng et al.    |   AAAI   |  [A Pre-Training Based Personalized Dialogue Generation Model with Persona-Sparse Data](https://arxiv.org/abs/1911.04700)   |
| 1911 |    Song et al.    |   AAAI   |  [Generating Persona Consistent Dialogues by Exploiting Natural Language Inference](https://arxiv.org/abs/1911.05889)   |
| 1807 |    Zhang et al.    |   ACL   |  [Personalizing Dialogue Agents: I have a dog, do you have pets too?](https://aclanthology.org/P18-1205/)   |
| 2307  |    Ahn, et al    |   ACL   |  [MPCHAT: Towards Multimodal Persona-Grounded Conversation](https://aclanthology.org/2023.acl-long.189/)   |
</details>


<h4 id="recommendation-system">🛒 Recommendation System</h4>

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2305 |    Yang et al.    |   arXiv   |  [PALR: Personalization Aware LLMs for Recommendation](https://arxiv.org/abs/2305.07622)   |
| 2304 |    Wang et al.    |   arXiv   |  [Zero-Shot Next-Item Recommendation using Large Pretrained Language Models](https://arxiv.org/abs/2304.03153)   |
| 2108 |    Li et al.    |   ACL   |  [Personalized Transformer for Explainable Recommendation](https://aclanthology.org/2021.acl-long.383/)   |


<details>
<summary><span style="color:#FFB6C1">Comprehensive Paper List</span></summary>

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2405 |    Hu et al.    |   WWW   |  [Enhancing sequential recommendation via llm-based semantic embedding learning](https://dl.acm.org/doi/abs/10.1145/3589335.3648307)   |
| 2311 |    Chen et al.    |   arXiv   |  [A Survey on Large Language Models for Personalized and Explainable Recommendations](https://arxiv.org/abs/2311.12338)   |
| 2308 |    Wang et al.    |   arXiv   |  [RecMind: Large Language Model Powered Agent For Recommendation](https://arxiv.org/abs/2308.14296)   |
| 2308 |    Chu et al.    |   arXiv   |  [Leveraging Large Language Models for Pre-trained Recommender Systems](https://arxiv.org/abs/2308.10837)   |
| 2306 |    Li et al.    |   arXiv   |  [Prompt Tuning Large Language Models on Personalized Aspect Extraction for Recommendations](https://arxiv.org/abs/2306.01475)   |
| 2305 |    Yang et al.    |   arXiv   |  [PALR: Personalization Aware LLMs for Recommendation](https://arxiv.org/abs/2305.07622)   |
| 2305 |    Zhang et al.    |   arXiv   |  [Recommendation as Instruction Following: A Large Language Model Empowered Recommendation Approach](https://arxiv.org/abs/2305.07001)   |
| 2304 |    Wang et al.    |   arXiv   |  [Zero-Shot Next-Item Recommendation using Large Pretrained Language Models](https://arxiv.org/abs/2304.03153)   |
| 2208 |    Chen et al.    |   KDD   |  [Personalized Chit-Chat Generation for Recommendation Using External Chat Corpora](https://dl.acm.org/doi/abs/10.1145/3534678.3539215)   |
| 2202 |    Li et al.    |   TOIS   |  [Personalized Prompt Learning for Explainable Recommendation](https://arxiv.org/abs/2202.07371)   |
| 2108 |    Li et al.    |   ACL   |  [Personalized Transformer for Explainable Recommendation](https://aclanthology.org/2021.acl-long.383/)   |
</details>


<h4 id="personalized-search">🔍 Personalized Search</h4>

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2405 |    Zhou et al.    |   WWW   |  [Cognitive personalized search integrating large language models with an efficient memory mechanism](https://arxiv.org/abs/2402.10548)   |
| 2405 |    Baek et al.    |   WWW   |  [Knowledge-Augmented Large Language Models for Personalized Contextual Query Suggestion](https://arxiv.org/abs/2311.06318)   |
| 2405 |    Salemi    |   arXiv   |  [Unified ranking for multiple retrieval-augmented large language models](https://arxiv.org/abs/2405.00175)   |
| 2402 |    Sharma et al.    |   CHI   |  [Generative echo chamber? effects of llm-powered search systems on diverse information seeking](https://arxiv.org/abs/2402.05880)   |
| 2307 |    Eleni et al.    |   arXiv   |  [Comparing Traditional and LLM-based Search for Consumer Choice: A Randomized Experiment](https://arxiv.org/abs/2307.03744)   |
| 2307 |    Ziems et al.    |   ACL   |  [Large Language Models are Built-in Autoregressive Search Engines](https://arxiv.org/abs/2305.09612)   |
| 2107 |    Zhou et al.    |   SIGIR   |  [Group based Personalized Search by Integrating Search Behaviour and Friend Network](https://arxiv.org/abs/2111.12618)   |



<h4 id="personalized-healthcare">🩺 Personalized Healthcare</h4>

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2402 |    Abbasian et al.   |   arXiv   |  [Knowledge-Infused LLM-Powered Conversational Health Agent: A Case Study for Diabetes Patients](https://arxiv.org/abs/2402.10153)   |
| 2402 |    Jin et al.    |   arXiv   |  [Health-LLM: Personalized Retrieval-Augmented Disease Prediction System](https://arxiv.org/abs/2402.00746)   |
| 2310 |    Abbasian et al.    |   arXiv   |  [Conversational Health Agents: A Personalized LLM-Powered Agent Framework](https://arxiv.org/abs/2310.02374)   |
| 2309 |    Zhang et al.    |   arXiv   |  [LLM-based Medical Assistant Personalization with Short- and Long-Term Memory Coordination](https://arxiv.org/abs/2309.11696)   |


<h4 id="personalized-education">📚 Personalized Education</h4>

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2403 |    Park et al.    |   CHI   |  [Empowering personalized learning through a conversation-based tutoring system with student modeling](https://arxiv.org/abs/2403.14071)   |
| 2308 |    Dan et al.    |   arXiv   |  [Educhat: A large-scale language model-based chatbot system for intelligent education](https://arxiv.org/abs/2308.02773)   |
| 2307 |    Shehata et al.    |   BEA @ ACL   |  [Enhancing Video-based Learning Using Knowledge Tracing: Personalizing Students’ Learning Experience with ORBITS](https://aclanthology.org/2023.bea-1.8/)   |



<h3 id="methods">🛠️ Methods</h3>

<h4 id="fine-tuning">🎛️ Fine-Tuning</h4>


| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2403 |    Mondal et al.    |   EACL   |  [Presentations by the Humans and For the Humans: Harnessing LLMs for Generating Persona-Aware Slides from Documents](https://aclanthology.org/2024.eacl-long.163/)   |
| 2402 |    Li et al.    |   arXiv   |  [Personalized Language Modeling from Personalized Human Feedback](https://arxiv.org/abs/2402.05133)   |
| 2402 |    Tan et al.    |   arXiv   |  [Democratizing Large Language Models via Personalized Parameter-Efficient Fine-tuning](https://arxiv.org/abs/2402.04401)   |
| 2312 |    Hwang et al.    |   arXiv   |  [Promptable Behaviors: Personalizing Multi-Objective Rewards from Human Preferences](https://arxiv.org/abs/2312.09337)   |
| 2312 |    Shea et al.    |   EMNLP   |  [Building Persona Consistent Dialogue Agents with Offline Reinforcement Learning](https://arxiv.org/abs/2310.10735)   |
| 2311 |    Qin et al.    |   arXiv   |  [Enabling on-device large language model personalization with self-supervised data selection and synthesis](https://arxiv.org/abs/2311.12275)   |
| 2310 |    Jang et al.    |   arXiv   |  [Personalized large language model alignment via post-hoc parameter merging](https://arxiv.org/abs/2310.11564)   |
| 2303 |    Kirk et al.    |   arXiv   |  [Personalisation within bounds: A risk taxonomy and policy framework for the alignment of large language models with personalised feedback](https://arxiv.org/abs/2303.05453)   |

<h4 id="retrieval-augmentation">🔗 Retrieval Augmentation</h4>

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2404 |    Zhang et al.    |   arXiv   |  [Personalized LLM Response Generation with Parameterized Memory Injection](https://arxiv.org/abs/2404.03565)   |
| 2403 |    Zhong et al.    |   AAAI   |  [MemoryBank: Enhancing Large Language Models with Long-Term Memory](https://ojs.aaai.org/index.php/AAAI/article/view/29946)   |
| 2402 |    Sun et al.    |   arXiv   |  [Persona-DB: Efficient Large Language Model Personalization for Response Prediction with Collaborative Data Refinement](https://arxiv.org/abs/2402.11060)   |
| 2402 |    Tan et al.    |   arXiv   |  [Democratizing Large Language Models via Personalized Parameter-Efficient Fine-tuning](https://arxiv.org/abs/2402.04401)   |
| 2205 |    Fu et al.    |   ACL   |  [There Are a Thousand Hamlets in a Thousand People’s Eyes: Enhancing Knowledge-grounded Dialogue with Personal Memory](https://aclanthology.org/2022.acl-long.270/)   |
|  2106 |    Wu et al.    |   NAACL   |  [Personalized Response Generation via Generative Split Memory Network](https://aclanthology.org/2021.naacl-main.157/)   |


<h4 id="prompting">✍️ Prompting</h4>


<h5 id="vanilla-personalized-prompt">📄 Vanilla Personalized Prompt</h5>

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2305 |    Dai et al.    |   RecSys   |  [Uncovering ChatGPT’s Capabilities in Recommender Systems](https://arxiv.org/abs/2305.02182)   |
| 2305 |    Christakopoulou et al.    |   arXiv   |  [Large Language Models for User Interest Journeys](https://arxiv.org/abs/2305.15498)   |
| 2305 |    Zhiyuli et al.    |   arXiv   |  [BookGPT: A General Framework for Book Recommendation Empowered by Large Language Model](https://arxiv.org/abs/2305.15673)   |


<h5 id="retrieval-augmented-personalized-prompt">🔦 Retrieval-Augmented Personalized Prompt</h5>

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2311 |    Mysore et al.    |   arXiv   |  [PEARL: Personalizing Large Language Model Writing Assistants with Generation-Calibrated Retrievers](https://arxiv.org/abs/2311.09180)   |
| 2308 |    Li et al.    |   arXiv   |  [Teach LLMs to Personalize -- An Approach inspired by Writing Education](https://arxiv.org/abs/2308.07968)   |
| 2304 |    Salemi et al.    |   arXiv   |  [LaMP: When Large Language Models Meet Personalization](https://arxiv.org/abs/2304.11406)   |



<h5 id="profile-augmented-prompt">📂 Profile-Augmented Prompt</h5>

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2405 |    Li et al.    |   WWW   |  [Learning to Rewrite Prompts for Personalized Text Generation](https://dl.acm.org/doi/10.1145/3589334.3645408)   |
| 2310 |    Richardson et al.    |   arXiv   |  [Integrating Summarization and Retrieval for Enhanced Personalization via Large Language Models](https://arxiv.org/abs/2310.20081)   |
| 2305 |    Liu et al.    |   WSDM   |  [ONCE: Boosting Content-based Recommendation with Both Open- and Closed-source Large Language Models](https://arxiv.org/abs/2305.06566)   |


<h2 id="llm-personality-evaluation">🧐 LLM Personality Evaluation</h2>

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2401 |    Huang et al.    |   ICLR   |  [On the Humanity of Conversational AI: Evaluating the Psychological Portrayal of LLMs](https://openreview.net/forum?id=H3UayAQWoE)   |
| 2309 |    Jiang et al.    |   NeurIPS   |  [Evaluating and inducing personality in pre-trained language models](https://arxiv.org/abs/2206.07550)   |
| 2307 |    Fang et al.    |   ACL   |  [On Text-based Personality Computing: Challenges and Future Directions](https://aclanthology.org/2023.findings-acl.691/)   |


<details>
<summary><span style="color:#FFB6C1">Comprehensive Paper List</span></summary>

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 2403 |    Sorokovikova et al.    |   PERSONALIZE @ EACL  |  [LLMs Simulate Big5 Personality Traits: Further Evidence](https://aclanthology.org/2024.personalize-1.7/)   |
| 2403 |    Frisch et al.    |   PERSONALIZE @ EACL   |  [LLM Agents in Interaction: Measuring Personality Consistency and Linguistic Alignment in Interacting Populations of Large Language Models](https://aclanthology.org/2024.personalize-1.9/)   |
| 2402 |    Song et al.    |   arXiv   |  [Identifying Multiple Personalities in Large Language Models with External Evaluation](https://arxiv.org/abs/2402.14805)   |
| 2402 |    Song et al.    |   arXiv   |  [Identifying Multiple Personalities in Large Language Models with External Evaluation](https://arxiv.org/abs/2402.14805)   |
| 2402 |    Yang et al.    |   arXiv   |  [LLM Agents for Psychology: A Study on Gamified Assessments](https://arxiv.org/abs/2402.12326)   |
| 2401 |    Huang et al.    |   ICLR   |  [On the Humanity of Conversational AI: Evaluating the Psychological Portrayal of LLMs](https://openreview.net/forum?id=H3UayAQWoE)   |
| 2312 |    Rao et al.    |   EMNLP   |  [Can ChatGPT Assess Human Personalities? A General Evaluation Framework](https://aclanthology.org/2023.findings-emnlp.84/)   |
| 2311 |    Dorner et al.   |   SoLaR @ NeurIPS   |  [Do personality tests generalize to large language models?](https://arxiv.org/abs/2311.05297)   |
| 2310 |    Wang et al.    |   arXiv   |  [InCharacter: Evaluating Personality Fidelity in Role-Playing Agents through Psychological Interviews](https://arxiv.org/abs/2310.17976)   |
| 2309 |    Jiang et al.    |   NeurIPS   |  [Evaluating and inducing personality in pre-trained language models](https://arxiv.org/abs/2206.07550)   |
| 2307 |    Pan et al.    |   arXiv   |  [Do LLMs Possess a Personality? Making the MBTI Test an Amazing Evaluation for Large Language Models](https://arxiv.org/abs/2307.16180)   |
| 2307 |    Fang et al.    |   ACL   |  [On Text-based Personality Computing: Challenges and Future Directions](https://aclanthology.org/2023.findings-acl.691/)   |
| 2307 |    Ji et al.    |   arXiv   |  [Is ChatGPT a Good Personality Recognizer? A Preliminary Study](https://arxiv.org/abs/2307.03952)   |
| 2305 |    Jiang et al.    |   arXiv   |  [Personallm: Investigating the ability of large language models to express big five personality traits](https://arxiv.org/abs/2305.02547)   |
</details>


<h2 id="how-to-contribute">🌱 How to contribute</h2>

:sparkles: Welcome to contribute to this reading list via :memo: [Issues](https://github.com/MiuLab/PersonaLLM-Survey/issues) using the following format.

| Date  |    Authors    | Venue |                                                            Paper                                                             |
|:-----:|:---------------:|:-----------:|:----------------------------------------------------------------------------------------------------------------------------|
| 1706  |    Vaswani, et al    |   NeurIPS   |  [Attention Is All You Need](https://proceedings.neurips.cc/paper_files/paper/2017/file/3f5ee243547dee91fbd053c1c4a845aa-Paper.pdf)   |

</div>
</div>


<h2 id="citation">🔖 Citation</h2>

📚 If you find our survey beneficial for your research, please kindly cite our paper :-)

```bibtex
@misc{tseng2024tales,
      title={Two Tales of Persona in LLMs: A Survey of Role-Playing and Personalization},
      author={Yu-Min Tseng and Yu-Chao Huang and Teng-Yun Hsiao and Yu-Ching Hsu and Jia-Yin Foo and Chao-Wei Huang and Yun-Nung Chen},
      year={2024},
      eprint={2406.01171},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```


<h2 id="authors">🖌️ Authors</h2>

[Yu-Min Tseng\*](https://github.com/ymntseng), [Yu-Chao Huang\*](https://github.com/Physics-Morris), [Teng-Yun Hsiao\*](), [Yu-Ching Hsu](), [Jia-Yin Foo](), [Chao-Wei Huang](https://github.com/chaoweihuang), [Yun-Nung Chen](https://www.csie.ntu.edu.tw/~yvchen/).

(\* Equal Contribution.)

<p align="center"><img src="figures/ntu-icon.svg" width="60%" /></p>
