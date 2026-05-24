<div align="center">
  <h1>交互式学习导师</h1>
  <p>让 Claude 变身费曼式私人导师 — 自适应、苏格拉底式、真正有效的互动学习。</p>

  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](../LICENSE)
  [![Platform](https://img.shields.io/badge/Platform-Claude%20Code-blue)](https://code.claude.com)
  [![Stars](https://img.shields.io/github/stars/20kiki/interactive-learning-tutor)](https://github.com/20kiki/interactive-learning-tutor)
</div>

---

## 📋 目录
- [问题](#-问题)
- [特性](#-特性)
- [快速开始](#-快速开始)
- [使用方式](#-使用方式)
- [主题标签](#-主题标签)
- [参与贡献](#-参与贡献)
- [许可证](#-许可证)

---

## 🔍 问题

大多数 AI 教学就像读教科书 — 扁平、一刀切、毫无互动。你说"教我数据库索引"，得到的是一堵文字墙，要么假设你什么都不懂，要么假设你已经有个计算机学位。

**交互式学习导师** 用三模式状态机解决了这个问题，根据你的水平、你的问题和你的节奏实时调整教学方式。

## ✨ 特性

* **三种教学模式** — 学习模式（深度互动）、答疑模式（即时深挖）、速览模式（快速扫完主题）
* **前置锚定** — 开讲前用具体行为描述动态校准你的真实水平，拒绝"入门/进阶"这种抽象标签
* **费曼优先** — 每个概念先用 12 岁能懂的生活例子引入，再过渡到技术精度
* **苏格拉底引导** — 最多 3 轮引导提问才给答案，建立真正的理解
* **实时错误分级** — 区分"随口确认"和"真没懂"，走不同补救路径
* **薄弱点追踪** — 全程记住你挣扎过的概念，随时可回顾复习
* **冲突处理协议** — 一句"没懂"立即触发费曼重讲，无视当前模式

## 🚀 快速开始

> **你需要：** 已安装 [Claude Code](https://code.claude.com)

**第 1 步 — 打开终端**

- macOS / Linux：打开终端
- Windows：Win + R，输入 `powershell`，回车

**第 2 步 — 安装为全局 skill**

这个 skill 只有一个 `SKILL.md` 文件，无其他依赖。

macOS / Linux：
```bash
mkdir -p ~/.claude/skills/interactive-learning-tutor
curl -o ~/.claude/skills/interactive-learning-tutor/SKILL.md \
  https://raw.githubusercontent.com/20kiki/interactive-learning-tutor/main/SKILL.md
```

Windows (PowerShell)：
```powershell
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.claude\skills\interactive-learning-tutor"
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/20kiki/interactive-learning-tutor/main/SKILL.md" `
  -OutFile "$env:USERPROFILE\.claude\skills\interactive-learning-tutor\SKILL.md"
```

**第 3 步 — 完成。** 重启 Claude Code，说一句"教我数据库索引"即可触发。

> 更新方式：重新执行以上命令即可。

## 📖 使用方式

表达学习意图即可触发：

| 你说 | 触发模式 |
| :--- | :--- |
| "教我数据库索引" | 学习模式 — 锚定 → 费曼 → 苏格拉底 → 验证 → 小测 |
| "快速过一遍设计模式" | 速览模式 — 一口气讲完全部概念 |
| "怎么理解闭包？" | 答疑模式 — 深挖此问题，结束回到学习模式 |
| "回顾薄弱点" | 薄弱点复习 — 只重讲你之前挣扎过的概念 |

导师会根据你的措辞自动选择模式，你也可以随时用上述短语切换。

**学习模式教学流程：**
1. **前置锚定** — 4 个具体水平选项（不用抽象标签）
2. **价值先行** — 一句话说明这个概念解决什么问题
3. **费曼引入** — 先用类比，再过渡到技术概念
4. **苏格拉底引导** — 最多 3 轮提问引导你自己推导
5. **随堂验证** — 每个概念讲完立刻确认是否跟上
6. **小测巩固** — 主题结束时用场景应用题检验迁移能力

## 📌 主题标签

[`claude-code`](https://github.com/topics/claude-code) [`claude-skill`](https://github.com/topics/claude-skill) [`ai-tutor`](https://github.com/topics/ai-tutor) [`education`](https://github.com/topics/education) [`feynman-technique`](https://github.com/topics/feynman-technique) [`socratic-method`](https://github.com/topics/socratic-method) [`interactive-learning`](https://github.com/topics/interactive-learning) [`teaching-tool`](https://github.com/topics/teaching-tool)

## 🤝 参与贡献

这个 skill 定义了一套教学协议。如果你有改进教学法、状态机或错误处理规则的想法：

1. 开一个 Issue，描述哪个教学场景没有被处理好
2. 提出具体的规则修改或新增建议
3. 欢迎 PR — 改动集中在 `SKILL.md`

详见 [CONTRIBUTING.md](../CONTRIBUTING.md)。

## 📄 许可证

MIT © 2026 20kiki。详见 [LICENSE](../LICENSE)。

---

<div align="center">
  <p><strong>Language:</strong> <a href="../README.md">English</a> | <a href="README.md">简体中文</a></p>
</div>
