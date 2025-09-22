---
categories: [大模型]
date: 2025-09-21 18:00:00 +0800
last_modified_at: 2025-09-21 18:10:00 +0800
tags: [TQA, COMET]
title: COMET翻译质量评估
pin: false
toc: true
comments: true
image:
  path: /img/COMET-Translation-Quality-Assessment.png
---

周末，基于COMET(https://github.com/Unbabel/COMET)，做了一个智能翻译质量评估系统

**COMET介绍：** COMET 是当前主流的神经网络自动评价指标之一，由 Unbabel 和大学学者合作开发。通常采用基于 XLM-R/BERT 等多语种预训练模型，输入候选译文、参考译文、源句三者，基于三元输入建模，使用人工标注的数据（如 DA scores）进行微调，学习端到端的“好坏”打分。支持多语种，能直接利用源文信息，鲁棒性强，对语义一致性和文体多样性更敏感，公认与人工评价的一致性很高。

**使用说明：** 导入源文本、翻译文本和参考翻译，选择评估模型，点击“获取质量评估报告”，过几分钟就可以得到评估结果，评估结果包含总体质量分数以及每个句段得分，评估结果可以导出为Excel或html格式的报告。

![COMET翻译质量评估](/img/COMET-Translation-Quality-Assessment2.png){: .shadow}

由于三个评估模型太大，所以我通过内网穿透，暂时部署在https://comet.llm.us.kg/上。

** 其他翻译评估指标：**

1. BLEURTBLEURT 由 Google 提出，是基于 BERT 预训练语言模型并经过微调的评估指标。BLEURT 先用大量人工评分的句对进行监督微调，学习如何用上下文语义表征参考译文和候选译文，输出一个相关性分数。能捕捉复杂的语义和语法关系，能判别多样化表达；实验表明与人工评价相关性高，适应多种语言对。

2. MetaMetrics-MTMetaMetrics-MT 是 Meta提出的最新一代自动评价指标，融合了大量人工评分和多种训练目标。在大规模的人工评价数据集上微调强大的 Transformer（如 XLM-RoBERTa）模型，支持多语言、多类型打分（如 adequacy、fluency 等），并对不同评价任务进行“多任务学习”。MetaMetrics-MT在WMT2024的Metric 榜单中，达到SOTA。

**参考资源：**
1. WMT24 QE文章：https://aclanthology.org/2024.wmt-1.3.pdf

2. 译文评分系统：https://qi.unbabel.com/

3. 译文比较系统：https://mtdemo.unbabel.com/

