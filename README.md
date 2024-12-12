# ComfyUI_RH_OminiControl

**ComfyUI_RH_OminiControl** 是一个基于 [OminiControl](https://github.com/Yuanshi9815/OminiControl) 的 ComfyUI 插件。通过分拆 pipeline 加载，该插件能够在 NVIDIA RTX 4090 显卡上高效运行。同时，空间（spatial）及填充（fill）功能也通过 schnell 模型生成，减少采样步数，提高整体效率。

## 特性

- **优化性能**：通过分拆 pipeline 加载，充分利用 RTX 4090 的计算能力。
- **高效生成**：使用 schnell 模型生成 spatial 及 fill，减少采样步数，提升生成效率。
- **易于安装**：依赖 ComfyUI 常用库，通常无需额外安装。
- **灵活配置**：支持自定义模型路径，便于管理和更新模型。

## 安装指南

### 前置条件

- **ComfyUI**：确保已安装并配置好 [ComfyUI](https://github.com/comfyanonymous/ComfyUI)。
- **Python 依赖**：通常不需要额外安装库，但建议安装 `diffusers` 版本 0.31.0 以支持 FluxPipeline。

## 下载插件
克隆本插件仓库到本地：


## 创建模型目录结构：

{comfyui_dir}/models/flux/
    FLUX.1-schnell/
    OminiControl/
        depth-anything-small-hf/
        experimental/
        omini/
### 下载并放置以下模型：

FLUX.1-schnell（diffusers 格式的 flux 模型）：
下载地址：FLUX.1-schnell
depth-anything-small-hf（用于 depth 识别）：
下载地址：depth-anything-small-hf

##致谢
感谢 Yuanshi9815 及其 OminiControl 项目提供的基础支持。
