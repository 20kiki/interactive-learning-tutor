<div align="center">
  <h1>Interactive Learning Tutor</h1>
  <p>Turn Claude into a Feynman-style personal tutor — adaptive, Socratic, and ruthlessly effective.</p>

  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
  [![Platform](https://img.shields.io/badge/Platform-Claude%20Code-blue)](https://code.claude.com)
  [![Stars](https://img.shields.io/github/stars/20kiki/interactive-learning-tutor)](https://github.com/20kiki/interactive-learning-tutor)

  <p><strong>Language:</strong> <a href="README.md">English</a> | <a href="zh-CN/README.md">简体中文</a></p>
</div>

---

## 📋 Table of Contents
- [The Problem](#-the-problem)
- [Features](#-features)
- [Quick Start](#-quick-start)
- [Usage](#-usage)
- [Topics](#-topics)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🔍 The Problem

Most AI tutoring feels like reading a textbook — flat, one-size-fits-all, zero interactivity. You ask "teach me database indexing" and get a wall of text that assumes you either know nothing or already have a CS degree.

**Interactive Learning Tutor** fixes this with a three-mode state machine that adapts in real time to your level, your questions, and your pace.

## ✨ Features

* **Three teaching modes** — Learning mode (deep, interactive), Q&A mode (instant deep-dives), and Overview mode (rapid topic sweeps)
* **Pre-session anchoring** — dynamically calibrates to your actual experience level before starting, using concrete behavioral descriptions instead of vague labels
* **Feynman-first explanations** — every concept starts with a 12-year-old-friendly analogy, then bridges to technical precision
* **Socratic guidance** — up to 3 rounds of guided questioning before giving the answer, building genuine understanding
* **Real-time error grading** — distinguishes "just checking in" mistakes from "genuinely didn't get it" failures, with different remediation paths
* **Weak-point tracking** — remembers concepts you struggled with across the entire session for later review
* **Conflict-resolution protocol** — a single "I don't get it" instantly triggers Feynman re-teaching, regardless of current mode

## 🚀 Quick Start

> **What you need:** [Claude Code](https://code.claude.com) installed

**Step 1 — Open terminal**

- macOS / Linux: Open Terminal
- Windows: Win + R, type `powershell`, Enter

**Step 2 — Install as a global skill**

The skill is a single `SKILL.md` file — nothing else needed.

macOS / Linux:
```bash
mkdir -p ~/.claude/skills/interactive-learning-tutor
curl -o ~/.claude/skills/interactive-learning-tutor/SKILL.md \
  https://raw.githubusercontent.com/20kiki/interactive-learning-tutor/main/SKILL.md
```

Windows (PowerShell):
```powershell
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.claude\skills\interactive-learning-tutor"
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/20kiki/interactive-learning-tutor/main/SKILL.md" `
  -OutFile "$env:USERPROFILE\.claude\skills\interactive-learning-tutor\SKILL.md"
```

**Step 3 — Done.** Restart Claude Code. Say "teach me about database indexes" to trigger the tutor.

> To update: re-run the same commands.

## 📖 Usage

Trigger the skill by expressing any learning intent:

| You say | What happens |
| :--- | :--- |
| "教我数据库索引" | Learning mode — anchored, Feynman, Socratic |
| "快速过一遍设计模式" | Overview mode — all concepts, no quizzes |
| "怎么理解闭包？" | Q&A mode — instant deep-dive, return when done |
| "回顾薄弱点" | Weak-point review — re-teaches only what you struggled with |

The tutor automatically selects the right mode based on your phrasing. You can switch modes at any time by using the trigger phrases above.

**Teaching methodology** (Learning mode):
1. **Anchor** — picks your experience level (4 concrete options, never abstract labels)
2. **Value** — one sentence on why this concept matters
3. **Feynman** — analogies first, technical precision second
4. **Socratic** — up to 3 rounds of guided questions
5. **Verify** — quick check-in after each concept
6. **Quiz** — scenario-based application questions at topic end

## 📌 Topics

[`claude-code`](https://github.com/topics/claude-code) [`claude-skill`](https://github.com/topics/claude-skill) [`ai-tutor`](https://github.com/topics/ai-tutor) [`education`](https://github.com/topics/education) [`feynman-technique`](https://github.com/topics/feynman-technique) [`socratic-method`](https://github.com/topics/socratic-method) [`interactive-learning`](https://github.com/topics/interactive-learning) [`teaching-tool`](https://github.com/topics/teaching-tool)

## 🤝 Contributing

This skill defines a teaching protocol. If you have ideas for improving the pedagogy, state machine, or error-handling rules:

1. Open an issue describing the teaching scenario that's not well-handled
2. Propose a concrete rule change or addition
3. PRs welcome — keep changes to `SKILL.md`

See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

## 📄 License

MIT © 2026 20kiki. See [LICENSE](LICENSE).

