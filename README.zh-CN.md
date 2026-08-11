> 🌐 Language / 语言：[English](./README.md) | **[简体中文](./README.zh-CN.md)**

# Viral Video Cloner Pro

> 面向电商短视频策划的开源 Codex Skill 工作流。

Viral Video Cloner Pro 是一套用于结构化电商视频策划的自托管 Codex Skill 定义集合。该仓库目前仅提供工作流说明和 Codex 元数据，**不包含**可运行的视频生成应用或服务商推理集成。

## 项目状态

### 当前已实现

当前仓库包含两个 Codex Skills：

| Skill | Codex 调用方式 | 当前范围 |
|---|---|---|
| 爆款视频分析与改编工作流 | `$ecommerce-viral-video-clone-hybrid` | 指导参考素材分析、叙事改编、镜头规划、提示词准备、合规审查、质量检查和交付整理。 |
| 原创电商视频策划工作流 | `$ecommerce-video-original-pure` | 指导原创概念开发、脚本策划、镜头设计、提示词准备、音频与字幕策划、合规审查和交付整理。 |

当前已实现的内容是声明式 `SKILL.md` 指令和 `agents/openai.yaml` 元数据。它们帮助 Codex 组织需要人工审核的策划流程；不会调用视频模型，也不会渲染媒体。

### 尚未实现

当前代码库中**不存在**以下能力：

- Python 应用代码
- FastAPI 服务或 HTTP 端点
- OpenCV 处理
- Image2-Storyboard 处理
- Seedance 2.0 API 或模型适配器
- 自动化图像或视频推理
- 批量渲染或最终视频导出
- 可部署的本地视频生成服务

这些项目仅列于下方的路线图中。

## 仓库结构

```text
viral-video-cloner-pro/
├── ecommerce-viral-video-clone-hybrid/
│   ├── SKILL.md
│   └── agents/
│       └── openai.yaml
├── ecommerce-video-original-pure/
│   ├── SKILL.md
│   └── agents/
│       └── openai.yaml
├── LICENSE
├── README.md
└── requirements.txt
```

`requirements.txt` 是仅用于路线图规划的文档，并不是可运行 Python 应用的安装清单。

## 安装

克隆仓库，并将其中一个或两个 Skill 目录复制到本地 Codex Skills 目录：

```bash
git clone https://github.com/binn8888/viral-video-cloner-pro.git
mkdir -p ~/.codex/skills
cp -R viral-video-cloner-pro/ecommerce-viral-video-clone-hybrid ~/.codex/skills/
cp -R viral-video-cloner-pro/ecommerce-video-original-pure ~/.codex/skills/
```

重新启动 Codex 或开始一个新任务，以便刷新 Skill 列表。

## 使用方法

在 Codex 中调用一个 Skill：

```text
$ecommerce-viral-video-clone-hybrid
```

或者：

```text
$ecommerce-video-original-pure
```

然后根据所选工作流的要求，提供项目简报、产品信息、受众、平台、目标时长以及任何已获得授权的参考素材。

这些 Skills 会提供策划指导和结构化制作说明。任何外部媒体生成步骤都需要单独的工具、账户、授权和人工确认。

## 负责任地使用

本仓库中的“复刻”是指分析并改编高层次的叙事结构、节奏和镜头功能。它不授权复制受保护的视频素材、完整脚本、个人肖像、商标或其他第三方资产。

用户有责任：

- 获得所有输入和参考素材的使用权；
- 审查广告、平台以及目标地区的合规要求；
- 在使用外部工具前验证生成的提示词和制作计划；以及
- 在发布任何媒体内容前完成人工审核。

## 路线图（Roadmap）

以下项目是规划提案，并非已实现功能：

1. **Image2-Storyboard 规范** — 定义用于解析单张叙事故事板画布的输入契约。
2. **Seedance 2.0 适配器设计** — 研究与服务商无关的适配器边界和配置模型。
3. **Python 项目基础** — 评估类型化模型、验证、测试和命令行工具。
4. **FastAPI 服务原型** — 在数据契约通过评审后探索本地 API 边界。
5. **OpenCV 工具** — 评估可选的故事板检查和媒体验证辅助工具。
6. **参数调优模块** — 定义可复现的配置方案和可审查的参数变更。
7. **本地部署文档** — 仅在可运行实现存在后记录安装和运行方式。
8. **批量渲染与导出** — 仅在服务商集成、安全控制和测试具备后进行研究。

路线图工作将通过公开 Issue 跟踪。在代码、测试和文档合并进仓库之前，任何路线图项目都不会被视为已实现。

## Codex API 使用声明

通过 Codex for Open Source 计划获得的任何 Codex 或 OpenAI API 额度，都将仅用于维护这个公开的开源仓库。符合条件的维护工作包括：

- 迭代 Codex Skill YAML 元数据和工作流定义；
- 分类处理并回复仓库 Issue；
- 编写和审查文档；
- 审查配置变更；以及
- 支持 Pull Request、版本发布及其他核心仓库维护工作流。

额度**不会**用于商业视频生成、视频模型推理、最终媒体制作、付费客户工作或运营商业内容生成服务。

本声明反映该仓库当前的公开范围，并旨在与 Codex for Open Source 申请保持一致。

## 维护

`binn8888` 是仓库所有者和主要维护者。维护工作包括 Issue 分类、聚焦的 Skill 与 YAML 更新、文档审查、配置审查，以及在变更准备就绪后进行版本化发布。

贡献内容应准确描述当前行为，明确区分已实现能力和路线图提案，并避免无法通过公开仓库验证的声明。

## 贡献

1. 创建 Issue 说明拟议变更。
2. 将变更集中于 Codex Skill 工作流、元数据、文档或明确标注的路线图设计工作。
3. 提交前验证编辑过的 YAML。
4. 说明变更如何保持当前功能与未来规划之间的边界。
5. 提交 Pull Request 供维护者审查。

## License

This project is licensed under the [MIT License](LICENSE).
