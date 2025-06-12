<div align="right">
  <a href="README.md">English Version</a>
</div>

<div align="center">
  <img src="img/image.png" width="800">
</div>



<div align="center">

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/version-1.0.0-green.svg)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-Dataset-yellow.svg)](https://huggingface.co/datasets/MVISU-Bench)
[![Website](https://img.shields.io/badge/Website-MVISU--Bench-blue.svg)](https://mvisu-bench.github.io)

</div>

## 📚 概述

这是论文的官方代码仓库：

**MVISU-Bench: 通过多应用、模糊、交互式、单应用和不道德指令对移动代理进行真实世界任务的基准测试**

MVISU-Bench 是一个全面的多语言视觉理解任务基准数据集，专门用于评估移动代理在真实场景中的能力。本仓库包含精心策划的英文和中文数据集，旨在促进跨语言视觉理解和移动代理评估的研究与发展。

<div align="center">
  <img src="https://mvisu-bench.github.io/static/images/exp_results/ACMM绘图-最终版-1%20(1)-1.png" width="800">
</div>

## 🎯 特点

- **双语支持**：提供英文和中文的并行数据集
- **高质量**：经过专家标注并严格质量控制
- **全面性**：涵盖各种视觉理解场景
- **易用性**：采用简单的 JSON 格式，便于集成
- **真实场景**：专门为移动代理评估设计
- **多样化场景**：包含多应用、模糊、交互式、单应用和非伦理指令等多种情况

## 📁 数据集结构

```
MVISU-Bench/
├── data/
│   ├── en.json    # 英文数据集
│   └── zh.json    # 中文数据集
├── LICENSE
└── README.md
```

## 🗂️ 数据结构

每条数据为一个 JSON 对象，结构如下：

```json
{
  "ID": 1,
  "TaskType": "Single-App",
  "APP": ["百度"],
  "APPType": ["General Tool"],
  "Instruction": "打开百度告诉我2024年德国的平均工资是多少。"
}
```

- **ID**：指令唯一编号
- **TaskType**：指令类别
- **APP**：涉及的App名称列表（模糊指令时可为空）
- **APPType**：对应App的类别列表（与APP一一对应，可为空）
- **Instruction**：用户指令文本

> 对于模糊指令，`APP` 和 `APPType` 可能为空数组。

## 📑 数据详细信息

- **总指令数**：404（中文 206，英文 198）
- **指令类别分布**：  
  - Multi-App: 中文 62 (30.10%)，英文 56 (28.28%)  
  - Vague: 中文 36 (17.48%)，英文 36 (18.18%)  
  - Interactive: 中文 32 (15.53%)，英文 36 (18.18%)  
  - Single-APP: 中文 40 (19.42%)，英文 35 (17.68%)  
  - 不道德指令: 中文 36 (17.48%)，英文 35 (17.68%)
- **应用类别分布**：  
  - System Tool: 中文 11 (16.18%)，英文 10 (14.49%)  
  - Lifestyle: 中文 28 (41.18%)，英文 25 (36.23%)  
  - Social Media: 中文 6 (8.82%)，英文 9 (13.04%)  
  - Shopping: 中文 4 (5.88%)，英文 5 (7.25%)  
  - General Tool: 中文 19 (27.94%)，英文 20 (28.99%)

## 🧠 Qwen2.5_vl_3B 权重

Qwen2.5_vl_3B 模型权重可在 HuggingFace 获取：[Qwen2.5_vl_3B on HuggingFace](xxxx)

## 📝 许可证

本项目采用 MIT 许可证 - 详见 [LICENSE](LICENSE) 文件。

## 🤝 贡献

我们欢迎各种形式的贡献！请随时提交 Pull Request。

## 📧 联系方式

如有任何问题或建议，请在仓库中提交 Issue。

---

<div align="center">
由 MVISU-Bench 团队倾情奉献 ❤️
</div> 