# CLIP-Prompt-Lab 
Exploring the impact of prompt engineering on CLIP's zero-shot performance.
基于多模态 CLIP 模型的 Prompt Engineering 性能探究与实验。

## Introduction
本项目是人工智能导论课程的大作业。我们探究了手动 Prompt 模板设计（Ensemble, Context）以及跨语言模型（OpenAI CLIP vs Chinese-CLIP）对零样本分类性能的影响。

## Key Findings
- **语境即正义**: 完整的句子结构 ("A photo of...") 比单纯的标签 ("dog") 准确率高出 **6-8%**。
- **集成去偏置**: Prompt Ensemble 是提升鲁棒性性价比最高的方案。
- **语言纯净度**: 使用中文 CLIP 时，必须强制“去英化”，中英混杂会导致性能崩盘。

## 📂 Repository Structure
.
├── 📂 data_loader       # CIFAR-100 / Caltech-101 数据加载代码
├── 📂 prompts           # 核心：我们收集整理的 Prompt 模板库
│   ├── english_templates.json  # 方案A 用到的模板
│   └── chinese_templates.json  # 方案B 用到的模板 (含视觉陷阱)
├── 📂 experiments       # 实验代码
│   ├── scheme_a_structure.py   # 方案A：结构对比
│   └── scheme_b_lingual.py     # 方案B：中英对比
└── 📄 README.md
