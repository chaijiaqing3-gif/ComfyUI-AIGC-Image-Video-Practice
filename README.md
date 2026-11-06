# ComfyUI AIGC Image & Video Generation Practice

> 基于 ComfyUI 的本地 AIGC 图片与视频生成实践，围绕商业产品视觉设计、Prompt 优化、工作流搭建及生成效果评估展开。

## 1. 项目简介

本项目记录使用 ComfyUI 在本地环境中完成 AIGC 图片与视频生成的实践过程。

以高端香水商业广告为主题，完成从静态产品图片生成到动态广告视频生成的探索，实践不同生成任务中的模型使用、工作流配置、提示词设计与效果优化。

**项目目标：**
- 熟悉 ComfyUI 节点式工作流的基本原理与操作方式。
- 探索文生图（Text-to-Image）和文生视频（Text-to-Video）的实现流程。
- 通过 Prompt 设计控制画面构图、光影、材质和镜头运动。
- 结合本地硬件条件，探索模型运行与生成效果之间的平衡。
- 沉淀可复用的工作流、提示词和实践文档。

## 2. 项目环境

| 项目 | 配置 |
|---|---|
| 操作系统 | Windows |
| 显卡 | NVIDIA GeForce RTX 4070 |
| 工作流平台 | ComfyUI |
| 图片生成方向 | Text-to-Image |
| 视频生成方向 | Text-to-Video |
| 视频模型 | Wan 2.1 |

说明：具体模型权重、显存容量、精度、采样参数及节点配置以实际环境和工作流文件为准。

## 3. 项目内容

### 3.1 AI 图片生成

以高端香水产品广告为主题，设计黑金色商业视觉风格。

**设计要点：**
- 透明玻璃香水瓶与琥珀色液体。
- 金色瓶盖与黑色大理石展示台。
- 暖金色光线、玻璃反射与折射效果。
- 暗色背景及电影感光影。
- 商业产品摄影构图与质感表现。

**实践重点：**
- 编写和优化正向提示词。
- 通过负向提示词减少画面异常。
- 调整视觉元素、光照及构图描述。
- 观察不同提示词对生成结果的影响。

### 3.2 AI 视频生成

使用 Wan 2.1 完成纯文生视频（Text-to-Video，T2V）实践。

以香水产品广告为主要场景，将静态商业视觉延伸为动态镜头。

**视频设计方向：**
- 香水瓶作为画面主体。
- 镜头缓慢推进。
- 暖金色光线在玻璃瓶表面移动。
- 展现液体、玻璃反射及光影变化。
- 营造高端商业广告氛围。

**实践重点：**
- 理解文生视频工作流的基本节点结构。
- 设计包含主体、场景、动作和镜头运动的提示词。
- 调整视频生成参数，观察生成时长与画面效果。
- 完成视频生成、预览及 MP4 文件导出。

## 4. 项目目录

```text
ComfyUI-AIGC-Image-Video-Practice/
├── README.md
├── .gitignore
├── docs/
│   ├── 实践报告.docx
│   ├── 实践报告.pdf
│   └── 环境配置与技术复盘.md
├── workflows/
│   ├── image-generation.json
│   └── wan2.1-t2v.json
├── prompts/
│   ├── perfume-image-prompt.txt
│   ├── perfume-video-prompt.txt
│   └── negative-prompts.txt
├── outputs/
│   ├── images/
│   └── videos/
└── screenshots/
    ├── image-workflow.png
    ├── video-workflow.png
    └── generation-result.png
