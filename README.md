# Viral Video Cloner Pro

> 低 Token 的 Codex 电商爆款复刻与原创视频工作流

面向电商短视频创作者的 Codex Skills 合集，支持爆款叙事结构复刻和纯原创带货视频创作，覆盖项目简报、脚本、分镜、视觉提示词、音频字幕、合规预检、分段质检与交付归档。

## 包含的 Skills

| Skill | Codex 调用方式 | 用途 |
|---|---|---|
| 2.5 爆款复刻 | `$ecommerce-viral-video-clone-hybrid` | 分析参考视频的叙事节奏，生成新的带货脚本、分镜和提示词；不搬运原视频画面或完整台词 |
| 3.0 原创视频 | `$ecommerce-video-original-pure` | 从产品资料、脚本、九宫格或人物参考出发，完成纯原创电商视频策划流程 |

## 核心能力

- 爆款叙事结构复刻与纯原创创意双路线
- 串行阶段控制和人工确认节点
- 产品、人物与场景一致性基准
- 长视频自动分段和首尾帧衔接规划
- 音频、字幕、合规预检与成片 QA 规范
- 适配 Pika、可灵 AI、即梦 Seedance 和 LibTV 的提示词方案
- 通过索引复用与全局视觉基准减少重复上下文

## 安装

```bash
git clone https://github.com/binn8888/viral-video-cloner-pro.git
mkdir -p ~/.codex/skills
cp -R viral-video-cloner-pro/ecommerce-viral-video-clone-hybrid ~/.codex/skills/
cp -R viral-video-cloner-pro/ecommerce-video-original-pure ~/.codex/skills/
```

安装后重新启动 Codex 或新建任务，让 Skills 列表刷新。

## 使用

在 Codex 对话中输入：

```text
$ecommerce-viral-video-clone-hybrid
```

或：

```text
$ecommerce-video-original-pure
```

然后按照 Skill 提示提交产品、平台、受众、时长、参考素材等信息。

## 重要说明

- 本仓库提供的是 Codex 工作流 Skills，不包含 Pika、可灵、Seedance 或 LibTV 的账号、额度和 API 密钥。
- “复刻”指叙事结构、节奏和镜头功能的重新创作，不代表复制原视频画面、人物、商标或完整台词。
- 生成或发布广告前，请自行确认素材授权、平台规则和投放地区的广告法规。
- 这些 Skills 可作为其他智能体平台的改写基础，但当前目录结构与调用方式以 Codex 为准。

## License

[MIT License](LICENSE)
