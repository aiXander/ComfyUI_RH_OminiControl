# ComfyUI_RH_OminiControl

**ComfyUI_RH_OminiControl** 是一个 **ComfyUI** 的插件，基于 **OminiControl**，旨在通过分拆 pipeline 加载优化性能，使该项目能够高效运行于 **NVIDIA RTX 4090** 上。同时，使用 **schnell** 模型生成的 **spatial** 和 **fill**，减少采样步数，从而提高计算效率。

**ComfyUI_RH_OminiControl** 提供了一种更加高效且易于集成的方式来使用 **OminiControl** 模型。

## 功能概述 / Features

- **高效计算 / Efficient Computation**: 通过分拆 pipeline 加载优化性能。
- **schnell 模型支持 / Schnell Model Support**: 使用更少的采样步数以提高效率。
- **ComfyUI 插件集成 / ComfyUI Plugin Integration**: 与 **ComfyUI** 集成，简化使用流程。
- **FluxPipeline 支持 / FluxPipeline Support**: 与 **diffusers** 库配合使用，支持 **FluxPipeline** 格式。

## 安装要求 / Installation Requirements

大部分所需的库为 **ComfyUI** 常用库，因此无需额外安装其他依赖。但以下库可能需要安装：

- **diffusers** 版本：0.31.0（支持 FluxPipeline）

```bash
pip install diffusers==0.31.0

## 项目目录结构 / Project Directory Structure

模型文件路径位于 {comfyui_dir}/models/flux/，以下是项目的目录结构：
{comfyui_dir}/models/flux/
├── FLUX.1-schnell/                # diffusers 格式的 Flux 模型
│   └── 下载地址：https://huggingface.co/black-forest-labs/FLUX.1-schnell
│
├── ComfyUI_RH_OminiControl/        # ComfyUI_RH_OminiControl 插件的模型目录
│   ├── depth-anything-small-hf/    # 用于深度识别的模型
│   │   └── 下载地址：https://huggingface.co/LiheYoung/depth-anything-small-hf/tree/main
│   ├── experimental/              # 实验性模型
│   │   └── 下载地址：https://huggingface.co/Yuanshi/OminiControl/tree/main/experimental
│   └── omini/                     # OminiControl 主模型
│       └── 下载地址：https://huggingface.co/Yuanshi/OminiControl/tree/main/omini


![image](https://github.com/user-attachments/assets/c1535de8-5c8d-40e6-aa7e-aac935eb73e9)

![image](https://github.com/user-attachments/assets/e1200a4d-f483-45de-bec7-0d5f82245dbc)

![image](https://github.com/user-attachments/assets/4fc66b28-ea82-4507-98b8-2e4320beaf52)
