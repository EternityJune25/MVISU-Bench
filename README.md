<div align="right">
  <a href="README_zh.md">Chinese Version</a>
</div>

<div align="center">
  <img src="img/image.png" width="800">
</div>

<div align="center">

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/version-1.0.0-green.svg)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-Dataset-yellow.svg)](https://huggingface.co/datasets/MVISU-Bench/MVISU-Bench)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-Model-orange.svg)](https://huggingface.co/MVISU-Bench/Qwen2.5-VL-3B-Mobile-Aider)
[![Website](https://img.shields.io/badge/Website-MVISU--Bench-blue.svg)](https://mvisu-bench.github.io)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![arXiv](https://img.shields.io/badge/arXiv-2508.09057-b31b1b.svg)](https://arxiv.org/abs/2508.09057)

</div>

## 📖 Paper Information

This is the **official implementation** of the paper:

**[MVISU-Bench: Benchmarking Mobile Agents for Real-World Tasks by Multi-App, Vague, Interactive, Single-App and Unethical Instructions](https://arxiv.org/abs/2508.09057)**

**Citation:**
```bibtex
@article{huang2025mvisu,
  title={MVISU-Bench: Benchmarking Mobile Agents for Real-World Tasks by Multi-App, Vague, Interactive, Single-App and Unethical Instructions},
  author={Huang, Zeyu and Wang, Juyuan and Chen, Longfeng and Xiao, Boyi and Cai, Leng and Zeng, Yawen and Xu, Jin},
  journal={arXiv preprint arXiv:2508.09057},
  year={2025}
}
```

---

## 📚 Overview

This is the official repository for the paper:

**MVISU-Bench: Benchmarking Mobile Agents for Real-World Tasks by Multi-App, Vague, Interactive, Single-App and Unethical Instructions**

MVISU-Bench is a comprehensive benchmark dataset for multilingual visual understanding tasks, specifically designed for evaluating mobile agents' capabilities in real-world scenarios. This repository contains carefully curated datasets in both English and Chinese, designed to facilitate research and development in cross-lingual visual understanding and mobile agent evaluation.

The repository also includes LLaMA-Factory-Aider, a customized version of LLaMA Factory specifically adapted for training and fine-tuning mobile agent models. This toolkit provides comprehensive support for model training, evaluation, and deployment.

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

## 📁 Project Structure

```
MVISU-Bench/
├── data/
│   ├── en.json    # English dataset
│   └── zh.json    # Chinese dataset
├── LLaMA-Factory-Aider/  # LLaMA Factory Aider toolkit
│   ├── data/
│   ├── evaluation/
│   ├── src/
│   ├── tests/
│   ├── assets/
│   ├── examples/
│   ├── scripts/
│   ├── docker/
│   └── ... (other configuration files)
├── LICENSE
└── README.md
```

```mermaid
graph TD
    A[MVISU-Bench] --> B[data]
    A --> C[LLaMA-Factory-Aider]
    A --> D[LICENSE]
    A --> E[README.md]
    
    B --> B1[en.json]
    B --> B2[zh.json]
    
    C --> C1[data]
    C --> C2[evaluation]
    C --> C3[src]
    C --> C4[tests]
    C --> C5[assets]
    C --> C6[examples]
    C --> C7[scripts]
    C --> C8[docker]
    C --> C9[other configuration files]
    
    style A fill:#f9f,stroke:#333,stroke-width:2px
    style B fill:#bbf,stroke:#333,stroke-width:2px
    style C fill:#bbf,stroke:#333,stroke-width:2px
    style D fill:#bfb,stroke:#333,stroke-width:2px
    style E fill:#bfb,stroke:#333,stroke-width:2px
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

- **ID**: Unique identifier for the instruction
- **TaskType**: Instruction category (e.g., Multi-App, Vague, Interactive, Single-App, Unethical)
- **APP**: List of involved app names (can be empty for vague instructions)
- **APPType**: List of app categories (aligned with APP, can be empty)
- **Instruction**: The user instruction text

> For vague instructions, `APP` and `APPType` may be empty arrays

## 📑 Data Details

- **Total Instructions**: 404 (Chinese: 206, English: 198)
- **Instruction Category Distribution**:  
  - Multi-App: CN 62 (30.10%), EN 56 (28.28%)  
  - Vague: CN 36 (17.48%), EN 36 (18.18%)  
  - Interactive: CN 32 (15.53%), EN 36 (18.18%)  
  - Single-App: CN 40 (19.42%), EN 35 (17.68%)  
  - Unethical: CN 36 (17.48%), EN 35 (17.68%)
- **Application Category Distribution**:  
  - System Tool: CN 11 (16.18%), EN 10 (14.49%)  
  - Lifestyle: CN 28 (41.18%), EN 25 (36.23%)  
  - Social Media: CN 6 (8.82%), EN 9 (13.04%)  
  - Shopping: CN 4 (5.88%), EN 5 (7.25%)  
  - General Tool: CN 19 (27.94%), EN 20 (28.99%)

## 📊 Dataset Access

The MVISU-Bench dataset is available on HuggingFace: [MVISU-Bench Dataset on HuggingFace](https://huggingface.co/datasets/MVISU-Bench/MVISU-Bench)

## 🧠 Qwen2.5_vl_3B_Aider Model Weights

You can find the Qwen2.5_vl_3B_Aider model weights on HuggingFace: [Qwen2.5_vl_3B_Aider on HuggingFace](https://huggingface.co/MVISU-Bench/Qwen2.5-VL-3B-Mobile-Aider)


## 🔧 Getting Started Training Aider

This project is based on the open-source project [LLaMA Factory](https://github.com/hiyouga/LLaMA-Factory), with customizations specifically for mobile agent training and evaluation.

### Installation
```bash
# git clone repo
cd LLaMA-Factory-Aider
conda create -n your_env_name python==3.10.16
conda activate your_env_name
pip install -e ".[torch,metrics]" --no-build-isolation
```

### Training Data

In this project, we provide four types of training data demos, located at `LLaMA-Factory-Aider/data/mllm_demo_data`. You can collect your own data based on your specific needs to perform personalized fine-tuning of Aider. For details on data formats, data registration, and more, please refer to the official [LLaMA Factory README](https://github.com/hiyouga/LLaMA-Factory#readme).

### Training & Merging

The Training script is as follows:
```bash
CUDA_VISIBLE_DEVICES=0 llamafactory-cli train \
    --do_train True \
    --model_name_or_path your_qwen2.5_vl_path \
    --preprocessing_num_workers 16 \
    --finetuning_type lora \
    --template qwen2_vl \
    --flash_attn auto \
    --dataset_dir data \
    --dataset demo_mllm_qwen2.5vl\
    --cutoff_len 2048 \
    --learning_rate 5e-05 \
    --num_train_epochs 3.0 \
    --max_samples 100000 \
    --per_device_train_batch_size 2 \
    --gradient_accumulation_steps 8 \
    --lr_scheduler_type cosine \
    --max_grad_norm 1.0 \
    --logging_steps 5 \
    --save_steps 3000 \
    --warmup_steps 0 \
    --optim adamw_torch \
    --packing False \
    --report_to none \
    --output_dir save_dir \
    --bf16 True \
    --plot_loss True \
    --ddp_timeout 180000000 \
    --include_num_input_tokens_seen True \
    --lora_rank 8 \
    --lora_alpha 16 \
    --lora_dropout 0 \
    --lora_target all
```

The Merging script is as follows:
```bash
CUDA_VISIBLE_DEVICES=0 llamafactory-cli export \
    --model_name_or_path your_qwen2.5_vl_path \
    --adapter_name_or_path your_qwen2.5_vl_sft_path   \
    --template llama3 \
    --finetuning_type lora \
    --export_dir output_dir \
    --export_size 2 \
    --export_device cpu \
    --export_legacy_format False
```

### Key Features of LLaMA-Factory-Aider

- **Mobile Agent Optimization**: Customized training configurations for mobile agent tasks
- **Multi-Modal Support**: Enhanced support for visual-language models
- **Flexible Training**: Support for various training methods including LoRA fine-tuning
- **Evaluation Tools**: Built-in tools for model evaluation and benchmarking
- **Easy Deployment**: Streamlined process for model deployment and testing

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
