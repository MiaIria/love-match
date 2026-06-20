# Love Match · 恋爱匹配分析 Skill

> 通过对话或问卷分析用户在亲密关系中的性格特征、相处模式和适配伴侣类型。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Claude%20Code-purple)](https://claude.ai/code)

---

## 🎯 这是什么

`love-match` 是一个面向亲密关系自我理解的 Codex Skill。它支持两种使用方式：

- **对话模式**：通过开放式问题收集性格、价值观、冲突处理和关系期待。
- **问卷模式**：通过结构化问题快速形成基础画像。

输出结果包括：

- 用户性格画像
- 适配伴侣类型推荐
- 为什么匹配
- 潜在挑战
- 具体相处建议
- 后续反馈和修正问题

它不是心理诊断，也不是“命定伴侣”预测，而是一个帮助用户更清楚理解自己关系模式的轻量工具。

---

## 📦 目录结构

```text
love-match/
├── SKILL.md                         # Codex Skill 入口
├── assets/
│   └── love-match-test.html          # 18 题 H5 测评 Demo
└── references/
    ├── README.md
    ├── questionnaire-design.md       # 问卷结构和题目设计原则
    ├── scoring-and-rules.md          # 维度、评分和洞察规则
    ├── report-framework.md           # 报告结构和表达边界
    └── barnum-effect-avoidance.md    # 巴纳姆效应规避
```

---

## 🚀 使用方式

在 Codex / Claude Code 中调用：

```text
/love-match
```

指定问卷模式：

```text
/love-match questionnaire
```

指定对话模式：

```text
/love-match conversation
```

---

## 🧠 设计重点

### 1. 先理解自己，再谈匹配

报告不直接告诉用户“你适合谁”，而是先分析用户自己的关系模式，再给出适配类型。

### 2. 避免绝对化判断

输出中使用“可能”“倾向于”“通常”等表达，避免把用户固定成某种标签。

### 3. 用 references 支撑产品逻辑

`references/` 里沉淀了问卷设计、评分维度、洞察规则、报告结构和巴纳姆效应规避方法，方便维护和面试讲解。

### 4. H5 Demo 展示完整体验

`assets/love-match-test.html` 是一个本地可打开的 18 题 H5 Demo，包含题目、阶段推进、分析引擎和结果页。

---

## 🛡️ 输出边界

必须做到：

- 温和、客观、有同理心
- 使用简体中文
- 给出具体相处建议
- 强调结果仅供参考

避免：

- 心理诊断式结论
- 宿命论或玄学判断
- “你一定适合/不适合某类人”
- 过度泛化的巴纳姆式描述

---

## License

MIT © MiaIria
