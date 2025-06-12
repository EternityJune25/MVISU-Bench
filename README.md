<div align="right">
  <a href="README_zh.md">中文版</a>
</div>

# <img src="https://mvisu-bench.github.io/static/images/colorPhone.png" width="50" style="vertical-align: middle"> <span style="color:#6BB6CF">M</span><span style="color:#E5CE70">V</span><span style="color:#A77ABF">I</span><span style="color:#49A697">S</span><span style="color:#D85B58">U</span>-Bench

<div align="center">

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/version-1.0.0-green.svg)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-Dataset-yellow.svg)](https://huggingface.co/datasets/MVISU-Bench)
[![Website](https://img.shields.io/badge/Website-MVISU--Bench-blue.svg)](https://mvisu-bench.github.io)

</div>

## 📚 Overview

This is the official repository for the paper:

**MVISU-Bench: Benchmarking Mobile Agents for Real-World Tasks by Multi-App, Vague, Interactive, Single-App and Unethical Instructions**

MVISU-Bench is a comprehensive benchmark dataset for multilingual visual understanding tasks, specifically designed for evaluating mobile agents' capabilities in real-world scenarios. This repository contains carefully curated datasets in both English and Chinese, designed to facilitate research and development in cross-lingual visual understanding and mobile agent evaluation.

<div align="center">
  <img src="https://mvisu-bench.github.io/static/images/exp_results/ACMM绘图-最终版-1%20(1)-1.png" width="800">
</div>

## 🎯 Features

- **Bilingual Support**: Parallel datasets in English and Chinese
- **High Quality**: Expert-annotated data with rigorous quality control
- **Comprehensive**: Covers various visual understanding scenarios
- **Easy to Use**: Simple JSON format for easy integration
- **Real-World Focus**: Specifically designed for mobile agent evaluation
- **Diverse Scenarios**: Includes multi-app, vague, interactive, single-app, and unethical instruction cases

## 📁 Dataset Structure

```
MVISU-Bench/
├── data/
│   ├── en.json    # English dataset
│   └── zh.json    # Chinese dataset
├── LICENSE
└── README.md
```

## 🗂️ Data Structure

Each entry in the dataset is a JSON object with the following fields:

```json
{
  "ID": 1,
  "TaskType": "Single-App",
  "APP": ["Google"],
  "APPType": ["General Tool"],
  "Instruction": "Search on Google to tell me how French fries should be cooked."
}
```

- **ID**: Unique identifier for the instruction.
- **TaskType**: Instruction category (e.g., Multi-App, Vague, Interactive, Single-App, Unethical).
- **APP**: List of involved app names (can be empty for vague instructions).
- **APPType**: List of app categories (aligned with APP, can be empty).
- **Instruction**: The user instruction text.

> For vague instructions, `APP` and `APPType` may be empty arrays.

## 📑 Data Details

- **Total Instructions**: 404 (Chinese: 206, English: 198)
- **Instruction Category Distribution**:  
  - Multi-App: CN 62 (30.10%), EN 56 (28.28%)  
  - Vague: CN 36 (17.48%), EN 36 (18.18%)  
  - Interactive: CN 32 (15.53%), EN 36 (18.18%)  
  - Single-APP: CN 40 (19.42%), EN 35 (17.68%)  
  - Unethical: CN 36 (17.48%), EN 35 (17.68%)
- **Application Category Distribution**:  
  - System Tool: CN 11 (16.18%), EN 10 (14.49%)  
  - Lifestyle: CN 28 (41.18%), EN 25 (36.23%)  
  - Social Media: CN 6 (8.82%), EN 9 (13.04%)  
  - Shopping: CN 4 (5.88%), EN 5 (7.25%)  
  - General Tool: CN 19 (27.94%), EN 20 (28.99%)

## 🧠 Qwen2.5_vl_3B Weights

You can find the Qwen2.5_vl_3B model weights on HuggingFace: [Qwen2.5_vl_3B on HuggingFace](xxxx)

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

We welcome contributions! Please feel free to submit a Pull Request.

## 📧 Contact

For any questions or suggestions, please open an issue in this repository.

---

<div align="center">
Made with ❤️ by the MVISU-Bench Team
</div> 