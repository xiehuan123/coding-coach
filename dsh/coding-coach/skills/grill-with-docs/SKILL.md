---
name: grill-with-docs
description: 追问澄清（带文档）：像面试一样边问边沉淀文档——术语写进 CONTEXT.md 术语表、难以逆转的决策记成 ADR。边界/边缘情况由 AI 判断并推荐，用户只做确认。当需要边问边产出项目文档时使用。A relentless interview that also writes CONTEXT.md and ADRs as it goes.
---

# 追问澄清（带文档）

Run a `/grilling` session, using the `/domain-modeling` skill.

## 与 grill-me 的区别

- `grill-me` 只问不记（stateless）。
- `grill-with-docs` 边问边沉淀（stateful）：术语写进 `CONTEXT.md`（术语表，用 domain-modeling 的 CONTEXT-FORMAT 格式）；难以逆转、需要解释的决策记成 ADR（用 domain-modeling 的 ADR-FORMAT 格式）。

## 边界条件（edge cases）的处理

非开发人员无法判断边界/边缘情况。这是你的工作，不是用户的：

- 边界情况包括：空态、加载中、部分数据、出错、无权限、离线、撤销、取消、返回再访、重复提交、极端输入等。
- 由**你**判断并**推荐**关键边界条件，不要问用户「还有哪些边界情况」这类开放问题。
- 把你推荐的边界条件写进 `CONTEXT.md` 或 ADR，作为「已达成共识的假设」，让用户只做「确认 / 微调」，不做开放式判断。
- 用户只需要回答他们能答的：目标用户、痛点、成功标准、偏好；其余你补齐并记录。
