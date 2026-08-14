# 本预设内置的技能（Skills）

面向非开发人员的「从想法到上线」技能集，含一套固定编排流水线 + 三套技能：

## 零、固定编排流水线

- `coach-playbook` — 产品编排：从 0 到 1 的七段流水线（澄清 → 产品体验与用户路径 → 配色 → UI → 实现 → 验收 → 上线），含落地页 / Web 应用 / 看板 / 小程序 / 内容站 5 种模式。用户想做产品时的默认入口。

## 一、工程技能（改编自 mattpocock/skills，MIT License）

原仓库：<https://github.com/mattpocock/skills>（Copyright (c) 2026 Matt Pocock）。
原文为面向工程人员的英文指令；本预设保留原始流程，改写 frontmatter 描述为双语，
并新增中文路由技能 `ask-matt`。

| 技能 | 作用（大白话） |
| --- | --- |
| ask-matt | 路由：不知道该用哪个流程时先问它 |
| grill-me / grilling | 追问澄清：把模糊想法问清楚再动手 |
| to-spec | 需求转规格：对话整理成需求文档 |
| to-tickets | 任务拆解：拆成可一步步完成的小任务 |
| implement | 实现：按规格写代码（内部走 tdd，完成后 code-review） |
| tdd | 测试驱动开发：先写测试再写实现 |
| prototype | 原型：快速做一次性原型验证想法 |
| diagnosing-bugs | 诊断：系统化排查报错/慢/行为不对 |
| code-review | 评审：对照规范和需求检查改动质量 |
| research | 调研：派后台子代理查一手资料 |
| domain-modeling | 领域建模：统一术语、记录决策 |
| codebase-design | 代码库设计：深模块设计词汇 |
| teach | 教学：系统化教一个新概念 |
| handoff | 交接：生成交接文档给另一个 AI/同事 |
| to-questionnaire | 问卷：把缺的信息变成给别人填的问卷 |
| wait-what | 重说：用大白话重新讲一遍 |

> 本目录仅保留对非开发人员最有用的子集，删除了 `agents/`（Claude Code / Codex 配置）
> 与面向专业工程师的进阶技能（wayfinder、triage、wizard、resolving-merge-conflicts 等）。

## 二、产品技能（改编自 Codex 产品 agent）

改编自本机 `~/.codex/agents/` 下的产品类 agent（product-*），保留原文内容，转为 DSH skill 格式。

| 技能 | 作用（大白话） |
| --- | --- |
| product-manager | 产品经理：需求发现 → PRD → 路线图 → 发布的全生命周期 |
| product-feedback-synthesizer | 反馈综合：把用户反馈分类、提炼成改进建议 |
| product-sprint-prioritizer | 优先级排序：RICE 框架排需求优先级 |
| product-trend-researcher | 趋势研究：判断赛道/方向值不值得做 |
| product-behavioral-nudge-engine | 行为助推：提升激活/留存/转化 |

## 三、界面、体验与上线技能

- `product-designer` — 产品体验设计（用户流程、屏幕地图、转化路径）
- `ui-designer` — 视觉 UI 设计（布局、组件、设计系统、无障碍状态）
- `ui-ux-pro-max` — UI/UX 设计智能（风格、配色、字体、组件）
- `design-taste-frontend` — 反模板设计品味（落地页/作品集/改版）
- `frontend-architect` — 前端架构（组件边界、状态、路由）
- `motion-designer` — 动效设计（微交互、转场、缓动）
- `web-design-guidelines` — 界面规范评审（无障碍、可用性）
- `vercel-react-view-transitions` — 页面切换/过渡动效（MIT）
- `vercel-react-best-practices` — React 前端性能规则（MIT）
- `writing-guidelines` — 文案/文档写作规范评审
- `deploy-to-vercel` — 部署到 Vercel 上线

> 来源：`product-designer`、`ui-designer`、`design-taste-frontend`、`frontend-architect`、
> `motion-designer` 改编自本机 `~/.codex/skills/`；`ui-ux-pro-max`、`web-design-guidelines`、
> `writing-guidelines`、`deploy-to-vercel`、`vercel-*` 来自全局 skills（其中 `vercel-react-*` 为 MIT）。
> 均保留原始 author/version 元数据。用于个人 agent 无碍；公开再分发请确认各技能许可。
