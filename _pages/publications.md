---
layout: page
permalink: /projects/
title: Projects
description: Overview of my software development projects, demonstrating expertise in distributed systems, microservices, and full-stack development.
nav: true
---

### [Distributed Trading System](https://github.com/Yuxuan-Li295/trade-release)

In this project, I engineered a scalable distributed trading system using **Spring Boot** and **Spring Cloud** within a microservice architecture, focusing on efficiency and reliability.

#### Challenges and Solutions:
1. **Search Performance and Accuracy**: Implemented goods search functionality using **ElasticSearch + Kibana**, enhancing performance and accuracy under massive data requests, including support for Chinese search with IK Segmenter.
2. **Unique ID Generation**: Utilized the SnowFlake algorithm for reliable ID generation in distributed environments.
3. **Message Queue Handling**: Integrated **RabbitMQ** to maintain data consistency through delayed messages and handle order generation asynchronously in concurrent scenarios.
4. **Inventory Management**: Improved inventory and data consistency by splitting inventory deduction into lockout, write-off, and rollback phases using **Redis + Lua** scripts.
5. **System Stress Testing**: Employed **JMeter** to simulate high volumes of concurrent requests, verifying system accuracy and robustness.
6. **Performance Optimization**: Used Redis for 'limit purchase' processing and cache warming to enhance page access performance.
7. **Static Content Management**: Implemented **Thymeleaf** template engine to generate static web pages, reducing backend load and improving response times.
8. **Security Enhancements**: Implemented a blacklisting model with data stored in Redis to intercept malicious requests efficiently.
9. **Service Discovery and RPC**: Used **SpringCloud** with **Consul** for service registry and **OpenFeign** for RPC service invocation.
10. **Database Scaling**: Applied database sharding with **Shardingsphere-JDBC** to enhance data storage capacity and query performance.
11. **Fault Tolerance**: Integrated **Hystrix** for current limiting strategies among sub-projects, with overall configuration managed in AWS Cloud.

### [Course Enrollment System](https://github.com/Yuxuan-Li295/COURSE-ENROLLEMNT)

Developed a responsive web-based course enrollment system that allows students to manage their academic courses effectively.

#### Key Features:
- **User Interface**: Built with **React.js** and **Material-UI** for a dynamic and accessible user experience.
- **Backend Services**: Utilized **Node.js** and **Express** for robust API services.
- **Data Handling**: Employed **MongoDB** for flexible and efficient data management.
- **Authentication**: Implemented JWT-based authentication to secure user sessions and data.
- **Real-time Data Processing**: Leveraged **Socket.IO** for real-time communication between clients and servers.


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
