# Coding Coach（编程教练）

面向**非开发人员**的工程技能包：把 [mattpocock/skills](https://github.com/mattpocock/skills)（MIT）
中 16 个最实用的技能改编为**中文友好**版本，并新增一个路由技能 `ask-matt`——
用户用大白话描述需求，AI 自动路由到「澄清 → 规划 → 实现 → 评审 → 讲解」的正确流程。

> 给非开发人员的体验：不需要懂编程术语。直接说「我想做个记账小工具，帮我一步步来」，
> AI 会先追问澄清（grill-me），再规划（to-spec / to-tickets）、实现（implement + tdd）、
> 检查（code-review），全程用你能听懂的话汇报，并可以随时要求它讲解（teach）或重讲（wait-what）。

## 技能清单（17 个）

| 技能 | 作用（大白话） |
| --- | --- |
| `ask-matt` | 路由：不知道该用哪个流程时先问它 |
| `grill-me` / `grilling` | 追问澄清：把模糊想法问清楚再动手 |
| `to-spec` | 需求转规格：对话整理成需求文档 |
| `to-tickets` | 任务拆解：拆成可一步步完成的小任务 |
| `implement` | 实现：按规格写代码（内部走 tdd，完成后 code-review） |
| `tdd` | 测试驱动开发：先写测试再写实现 |
| `prototype` | 原型：快速做一次性原型验证想法 |
| `diagnosing-bugs` | 诊断：系统化排查报错 / 慢 / 行为不对 |
| `code-review` | 评审：对照规范和需求检查改动质量 |
| `research` | 调研：派后台子代理查一手资料 |
| `domain-modeling` | 领域建模：统一术语、记录决策 |
| `codebase-design` | 代码库设计：深模块设计词汇 |
| `teach` | 教学：系统化教一个新概念 |
| `handoff` | 交接：生成交接文档给另一个 AI / 同事 |
| `to-questionnaire` | 问卷：把缺的信息变成给别人填的问卷 |
| `wait-what` | 重说：用大白话重新讲一遍 |

## 安装方式

### 1. Claude Code 官方插件（推荐）

```bash
claude plugin install xiehuan123/coding-coach
```

或在会话内：`/plugin install xiehuan123/coding-coach`

也可以通过 skills.sh 安装：`npx skills@latest add xiehuan123/coding-coach`

### 2. DeepSeek Harness（DSH）Agent 预设

把本仓库的 `dsh/coding-coach` 目录复制到本机 DSH 预设目录：

```bash
mkdir -p ~/.dsh/.agent-presets
cp -R dsh/coding-coach ~/.dsh/.agent-presets/coding-coach
```

然后在新会话的 Agent 选择器中选中「编程教练」。

### 3. 手动拷贝 skills

直接把 `skills/` 下的任意技能目录拷到你的 agent 技能目录（如 `~/.claude/skills/`、`~/.agents/skills/`）。

## 仓库结构

```
coding-coach/
├── README.md                 # 本文件
├── LICENSE                   # MIT（含 mattpocock/skills 原始版权声明）
├── .claude-plugin/
│   ├── plugin.json           # Claude Code 插件清单（官方格式）
│   └── marketplace.json      # 插件市场清单
├── skills/                   # 17 个改编后的技能（SKILL.md，供插件 / 手动安装）
└── dsh/
    └── coding-coach/         # DSH Agent 预设（agent.cordis.yml + preset.yml + skills/）
```

## 致谢与许可

- 技能内容改编自 [mattpocock/skills](https://github.com/mattpocock/skills)，
  Copyright (c) 2026 Matt Pocock，[MIT License](https://github.com/mattpocock/skills/blob/main/LICENSE)。
- 本仓库：MIT License（见 [LICENSE](./LICENSE)）。
- 改编内容：双语描述、删除 Claude Code / Codex 专属配置（`agents/`、`disable-model-invocation`），
  新增中文路由技能 `ask-matt`（本地化改写）。
