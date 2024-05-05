---
layout: page
permalink: /publications/
title: Projects
description: 
nav: true
---


#### Distributed Trading System

In this project, I engineered a scalable distributed trading system by employing Spring Boot and Spring Cloud for a microservice architecture, to ensure a efficient and reliable system design. 

Some of the summary of the diffculties in the project:
 1. Implemented goods search part by utilizing ElasticSearch + Kibana, resolve the problem of search performance and search accuracy under massive data requests. At the same time, Support Chinese Search with IK Segmenter.
 2. Unique ID generation for distributed environments by using the SnowFlake algorithm.
 3. Using Rabbitmq as a system business processing MQ to handle inventory deduction data consistency through delayed messages and handle order generation in concurrent scenarios asynchronously. 
 4. Handle inventory and data consistency processing by splitting the inventory deduction step into lockout, write-off and rollback and use Redis + Lua scripting solution.
 5. Use Jmeter to simulate large number of concurrent requests to the system to verify the accuracy fo teh system in concurrent scenarios. 
 6. Use Redis for 'limit purchase' processing and cache warm-up to improve page access performance.
 7. Use Thymeleaf model engine to static web pages, reduce the processing pressure on the back-end services, and improve page access speed. 
 8. Intercepting malicious requests by employing a blacklisting model: in order to improve the response speed of the blacklisting service, the data is stored in the redis. 

- Goods Module


- A Survey on Evaluation of Large Language Models. Yupeng Chang, Xu Wang, Jindong Wang, Yuan Wu, Kaijie Zhu, Hao Chen, Linyi Yang, Xiaoyuan Yi, Cunxiang Wang, Yidong Wang, Wei Ye, Yue Zhang, Yi Chang, Philip S. Yu, Qiang Yang, Xing Xie. [[arxiv](https://arxiv.org/abs/2307.03109)] [[code](https://github.com/MLGroupJLU/LLM-eval-survey)]
- PromptBench: Towards Evaluating the Robustness of Large Language Models on Adversarial Prompts. Kaijie Zhu, Jindong Wang, Jiaheng Zhou, Zichen Wang, Hao Chen, Yidong Wang, Linyi Yang, Wei Ye, Neil Zhenqiang Gong, Yue Zhang, Xing Xie. [[arxiv](https://arxiv.org/abs/2306.04528)] [[code](https://github.com/microsoft/promptbench)]
- PandaLM: An Automatic Evaluation Benchmark for LLM Instruction Tuning Optimization. Yidong Wang, Zhuohao Yu, Zhengran Zeng, Linyi Yang, Cunxiang Wang, Hao Chen, Chaoya Jiang, Rui Xie, Jindong Wang, Xing Xie, Wei Ye, Shikun Zhang, Yue Zhang. [[arxiv](https://arxiv.org/abs/2306.05087)] [[code](https://github.com/WeOpenML/PandaLM)]
- Selective Mixup Helps with Distribution Shifts, But Not (Only) because of Mixup. Damien Teney, Jindong Wang, Ehsan Abbasnejad. [[arxiv](https://arxiv.org/abs/2305.16817)]
- Imprecise Label Learning: A Unified Framework for Learning with Various Imprecise Label Configurations. Hao Chen, Ankit Shah, Jindong Wang, Ran Tao, Yidong Wang, Xing Xie, Masashi Sugiyama, Rita Singh, Bhiksha Raj. [[arxiv](https://arxiv.org/abs/2305.12715)]
- Exploring Vision-Language Models for Imbalanced Learning. Yidong Wang, Zhuohao Yu, **Jindong Wang**, Qiang Heng, Hao Chen, Wei Ye, Rui Xie, Xing Xie, Shikun Zhang. [[arxiv](https://arxiv.org/abs/2304.01457)] [[code](https://github.com/Imbalance-VLM/Imbalance-VLM)]
- An Embarrassingly Simple Baseline for Imbalanced Semi-Supervised Learning. Hao Chen, Yue Fan, Yidong Wang, **Jindong Wang**, Bernt Schiele, Xing Xie, Marios Savvides, Bhiksha Raj. [[arxiv](https://arxiv.org/abs/2211.11086)] 
- FIXED: Frustratingly Easy Domain Generalization with Mixup. Wang Lu, **Jindong Wang**, Han Yu, Lei Huang, Xiang Zhang, Yiqiang Chen, Xing Xie. [[arxiv](https://arxiv.org/abs/2211.05228)]
- Conv-Adapter: Exploring Parameter Efficient Transfer Learning for ConvNets. Hao Chen, Ran Tao, Han Zhang, Yidong Wang, Wei Ye, Jindong Wang, Guosheng Hu, and Marios Savvides. [[arxiv](https://arxiv.org/abs/2208.07463)]
- Equivariant Disentangled Transformation for Domain Generalization under Combination Shift. Yivan Zhang, **Jindong Wang**, Xing Xie, and Masashi Sugiyama. [[arxiv](https://arxiv.org/abs/2208.02011)]
- Boosting Cross-Domain Speech Recognition with Self-Supervision. Han Zhu, Gaofeng Cheng, **Jindong Wang**, Wenxin Hou, Pengyuan Zhang, and Yonghong Yan. [[arxiv](https://arxiv.org/abs/2206.09783)]
- Learning Invariant Representations across Domains and Tasks. **Jindong Wang**, Wenjie Feng, Chang Liu, Chaohui Yu, Mingxuan Du, Renjun Xu, Tao Qin, and Tie-Yan Liu. [[arxiv](https://arxiv.org/abs/2103.05114)]
- Learning to match distributions for domain adaptation. Chaohui Yu, **Jindong Wang**, Chang Liu, Tao Qin, Renjun Xu, Wenjie Feng, Yiqiang Chen, and Tie-Yan Liu. [[arxiv](https://arxiv.org/abs/2007.10791)]

#### Books

<div class="publications">

{% for y in page.years %}
  {% bibliography -f books -q @*[year={{y}}]* %}
{% endfor %}

</div>

#### Papers

<div class="publications">

{% for y in page.years %}
  <div>{{y}}</div>
  {% bibliography -f pubs -q @*[year={{y}}]* %}
{% endfor %}

</div>
