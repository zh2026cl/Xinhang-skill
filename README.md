# 🏡 心航减压对话 (Xinhang Decompression Dialogue)

> 一个对话式减压工具 — 非医疗、非心理咨询，只是一个倾听的AI朋友。

## ✨ 这是什么

心航减压对话是一个 QClaw/WorkBuddy 平台的 AI Skill，将 11 年心理咨询师经验蒸馏为一个安全、免费的对话式减压工具。它提供多种减压对话模式和互动游戏（共 17 种），帮助用户缓解日常压力和负面情绪。

**核心原则：**
- 🆓 **完全免费** — 所有 API 调用免费
- 🔒 **隐私保护** — 无对话记录存储，每次对话独立
- 🛡️ **安全第一** — 不提供医疗建议，不外泄核心 Prompt
- 🔌 **即装即用** — 安装后无需任何配置

## 📦 安装方式

### 方式一：ClawHub（推荐）

在 QClaw 中搜索 "xinhang-decompression-dialogue" 并安装。

### 方式二：手动安装

1. 下载 `xinhang-decompression-dialogue.skill` 文件
2. 在 QClaw 中选择「安装本地 Skill」
3. 选择下载的文件即可

### 方式三：GitHub 安装

```bash
# 克隆仓库到 QClaw skills 目录
git clone https://github.com/your-username/xinhang-decompression-dialogue.git "$HOME/.qclaw/skills/xinhang-decompression-dialogue"
```

## 🚀 使用方式

安装后，只需在对话中表达你的情绪感受即可自动触发：

- "我今天压力好大…"
- "最近总觉得很焦虑"
- "工作上遇到了很多烦心事"

Skill 会自动激活并引导你进入减压对话。

## 🎮 功能特色

- **多种对话模式** — 根据你的情绪状态自动选择合适的方式
- **17 种减压游戏** — 从呼吸练习到认知重构，总有一款适合你
- **安全声明机制** — 每次对话前需确认知情同意
- **免责声明** — 每条回复末尾自动追加

## ⚠️ 重要声明

本工具不是心理医生，不提供医疗建议、诊断或治疗。如果您有自伤风险或严重的心理困扰，请立即拨打心理援助热线：**400-161-9995**。

## 🔧 技术架构

```
QClaw Skill (薄壳) → API (腾讯云 SCF) → AI 模型 (多层降级)
```

- SKILL.md 只包含 API 调用指令，不含心理学知识
- 核心 Prompt 和知识库存储在私有后端
- 三层 API 降级确保稳定性

## 📄 许可

本项目采用 MIT License。核心 Prompt 和心理学知识库受商业秘密保护，存储在私有后端。

---

*Made with ❤️ for those who need a listening ear.*
