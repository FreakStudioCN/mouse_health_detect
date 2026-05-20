# 豚宝保 — 宠物豚鼠智能健康监测终端

全球首款专为豚鼠设计的多模态智能健康监测终端，以 K230 边缘芯片为核心，通过视觉 + 听觉融合感知实现运动量统计、脚垫卡脚识别、疾病早期预警及每日健康报告推送。

[![演示文稿](https://img.shields.io/badge/📊_演示文稿-GitHub_Pages-ff6b9d?style=for-the-badge)](https://freakstudiocn.github.io/mouse_health_detect/presentation.html)
[![备用链接](https://img.shields.io/badge/备用-htmlpreview-555555?style=for-the-badge)](https://htmlpreview.github.io/?https://github.com/FreakStudioCN/mouse_health_detect/blob/main/presentation.html)
[![License](https://img.shields.io/badge/License-MIT-00ff88?style=for-the-badge)](LICENSE)
[![Status](https://img.shields.io/badge/状态-原型研发中-ffd700?style=for-the-badge)]()

---

## 目录

- [项目简介](#项目简介)
- [核心功能](#核心功能)
- [技术架构](#技术架构)
- [市场背景](#市场背景)
- [项目结构](#项目结构)
- [团队介绍](#团队介绍)
- [路线图](#路线图)

---

## 项目简介

<a name="项目简介"></a>

当前宠物健康监测市场存在显著空白：**科研级设备价格数万元、体积庞大，家用不现实；消费级设备 90% 为猫狗专用，豚鼠体型与行为模式完全不适配。**

豚宝保项目依托团队在计算机视觉与动物行为分析领域的深厚积累（**4 项软件著作权、5 项发明专利及多篇核心期刊论文**），打造全球首款专为豚鼠设计的消费级智能健康监测终端，精准填补「科研级没法用、消费级用不了」的市场空白。

---

## 核心功能

<a name="核心功能"></a>

| 功能模块 | 描述 |
|---|---|
| 🏃 **运动量统计** | 实时追踪豚鼠活动轨迹，统计每日运动量，生成健康报告 |
| 🦶 **脚垫卡脚识别** | 视觉算法识别脚垫卡脚异常，第一时间推送预警 |
| 🫁 **疾病早期预警** | 融合视觉 + 听觉信号，识别呼吸道疾病等早期症状 |
| 📊 **每日健康报告** | 自动汇总行为数据，生成结构化健康报告推送给主人 |
| 🌐 **远程监控** | 主人外出也能实时查看豚鼠状态 |

---

## 技术架构

<a name="技术架构"></a>

- **核心芯片**：嘉楠 K230（边缘 AI 芯片，内置 NPU）
- **感知方式**：视觉 + 听觉多模态融合
- **算法框架**：轻量化目标追踪 + 行为分类模型，支持边缘端实时推理
- **开发生态**：基于团队 MicroPython 全生态，复用 100+ 款驱动模块

> 代码持续整理中，敬请期待。

---

## 市场背景

<a name="市场背景"></a>

- 📈 2024 年我国小宠异宠市场规模 **111.06 亿元**，同比增长超 10%
- 👥 异宠饲养人群超 **1707 万**，啮齿类占比持续提升
- 💰 豚鼠饲养者月均核心消费 **600-800 元**，付费意愿强
- 🚫 针对豚鼠的专业智能监测设备目前**几乎为零**

---

## 项目结构

<a name="项目结构"></a>

```
mouse_health_detect/
├── presentation.html        # 项目演示文稿（GitHub Pages 入口）
├── README.md
└── docs/
    └── static/              # 演示文稿所用图片资源
        ├── product_main.png
        ├── device_professional.png
        ├── device_consumer.png
        ├── algorithm_demo.png
        └── ...
```

> 硬件设计、算法代码、固件代码将在原型验证完成后陆续开源。

---

## 团队介绍

<a name="团队介绍"></a>

| 成员 | 角色 | 核心能力 |
|---|---|---|
| **李子圣** | 技术负责人 | K230边缘AI · 计算机视觉 · 嵌入式硬件 · 5项发明专利 |
| **辛瑞莉** | 运营/销售/宣传 | 市场推广 · 用户运营 · 多项国家级竞赛奖项 |
| **李琪震** | 嵌入式开发（实习） | STM32 · IoT · 全国电子设计竞赛省一 |
| **刘嘉乐** | 算法开发（实习） | 多传感器融合 · 生物医学工程大赛国二 |
| **Ali** | 海外开发者 | ESP32 · MicroPython · 东南亚市场 |

团队依托 **太原青禾之道科技有限公司** 及 **中北大学多模多源智能感知实验室** 展开研发。

---

## 路线图

<a name="路线图"></a>

- [x] 项目立项 & 技术方案确定
- [x] 核心算法原型验证（目标追踪 · 行为分类）
- [ ] **M1-2**：硬件原型优化，完成 K230 多模态感知集成
- [ ] **M3-5**：小批量试产（50-100 台），核心社群内测
- [ ] **M6-9**：量产上市，拼多多/抖音/闲鱼渠道铺设
- [ ] **Long Term**：品类拓展（仓鼠·龙猫），东南亚/欧美市场

---

<div align="center">
  <sub>让每一只豚鼠都能健康快乐地陪伴左右 🐹</sub><br>
  <sub><a href="https://freakstudio.cn">freakstudio.cn</a> · <a href="https://github.com/FreakStudioCN">github.com/FreakStudioCN</a> · <a href="https://upypi.net">upypi.net</a></sub>
</div>
