# 本预设内置的技能（Skills）

这些技能改编自 [mattpocock/skills](https://github.com/mattpocock/skills)
（Copyright (c) 2026 Matt Pocock，MIT License）。
原文为面向工程人员的英文指令；本预设保留了原始流程，仅改写 frontmatter 描述为双语，
并新增了面向非开发人员的路由技能 `ask-matt`（原路由技能的本地化改写）。

## 技能清单

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

## 原始仓库

- https://github.com/mattpocock/skills （MIT License）
- 本目录仅保留对非开发人员最有用的子集，删除了 `agents/`（Claude Code / Codex 配置）
  与面向专业工程师的进阶技能（wayfinder、triage、wizard、resolving-merge-conflicts 等）。
