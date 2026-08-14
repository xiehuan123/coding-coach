# Coding Coach（编程教练）

面向**非开发人员**的「从想法到上线」全流程产品教练：三套技能覆盖**产品 → 界面 → 实现 → 上线**。

> 给非开发人员的体验：不需要懂编程术语。直接说「我想做个记账小工具，帮我一步步来」，
> AI 会先追问澄清（grill-me / product-manager），再设计界面（ui-ux-pro-max）、
> 实现（implement + tdd）、检查（code-review）、上线（deploy-to-vercel），
> 全程用你能听懂的话汇报，并可以随时要求它讲解（teach）或重讲（wait-what）。

## 技能清单（33 个）

### 工程技能（改编自 mattpocock/skills，MIT）

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

### 产品技能（改编自 Codex product agent）

| 技能 | 作用（大白话） |
| --- | --- |
| `product-manager` | 产品经理：需求发现 → PRD → 路线图 → 发布 |
| `product-feedback-synthesizer` | 反馈综合：把用户反馈提炼成改进建议 |
| `product-sprint-prioritizer` | 优先级排序：RICE 框架排需求优先级 |
| `product-trend-researcher` | 趋势研究：判断赛道/方向值不值得做 |
| `product-behavioral-nudge-engine` | 行为助推：提升激活/留存/转化 |

### 界面与上线技能

| 技能 | 作用（大白话） |
| --- | --- |
| `product-designer` | 产品体验设计：用户流程、转化路径、功能取舍 |
| `ui-designer` | 视觉 UI：布局、组件、设计系统、无障碍状态 |
| `ui-ux-pro-max` | UI/UX 设计智能：风格、配色、字体、组件 |
| `design-taste-frontend` | 反模板设计品味：落地页/作品集/改版 |
| `frontend-architect` | 前端架构：组件边界、状态、路由 |
| `motion-designer` | 动效设计：微交互、转场、缓动 |
| `web-design-guidelines` | 界面规范评审：无障碍、可用性 |
| `vercel-react-view-transitions` | 页面切换/过渡动效 |
| `vercel-react-best-practices` | React 前端性能规则 |
| `writing-guidelines` | 文案/文档写作规范评审 |
| `deploy-to-vercel` | 部署到 Vercel 上线 |

## 安装方式

### 1. Claude Code 官方插件（推荐）

```bash
claude plugin install xiehuan123/coding-coach
```

或在会话内：`/plugin install xiehuan123/coding-coach`

也可以通过 skills.sh 安装：`npx skills@latest add xiehuan123/coding-coach`

### 2. DeepSeek Harness（DSH）Agent 预设（推荐给非开发人员）

把本仓库的 `dsh/coding-coach` 目录复制到本机 DSH 预设目录：

```bash
mkdir -p ~/.dsh/.agent-presets
cp -R dsh/coding-coach ~/.dsh/.agent-presets/coding-coach
```

然后在新会话的 Agent 选择器中选中「编程教练」。

### 3. DeepSeek Harness（DSH）profile 插件（bundle）

把 33 个技能装进某个 profile 的全局技能目录，该 profile 下所有 Agent 都能用：

```bash
dsh plugin --profile web add github:xiehuan123/coding-coach
```

> 用 npm 包名安装也可：`dsh plugin --profile web add coding-coach`（需先发布到 npm）。
> 安装后可用 `dsh --profile web --dump-config` 看到新增的 `skill-filesystem-coding-coach` 行。

### 4. 手动拷贝 skills

直接把 `skills/` 下的任意技能目录拷到你的 agent 技能目录（如 `~/.claude/skills/`、`~/.agents/skills/`）。

## 仓库结构

```
coding-coach/
├── README.md                 # 本文件
├── LICENSE                   # MIT（含 mattpocock/skills 原始版权声明）
├── package.json              # DSH bundle 清单（dsh.bundle.patch → cordis.patch.yml）
├── cordis.patch.yml          # DSH bundle patch：插入独立 skill-filesystem 行
├── .claude-plugin/
│   ├── plugin.json           # Claude Code 插件清单（官方格式）
│   └── marketplace.json      # 插件市场清单
├── skills/                   # 33 个技能（SKILL.md，供插件 / 手动安装）
└── dsh/
    └── coding-coach/         # DSH Agent 预设（agent.cordis.yml + preset.yml + skills/）
```

## 致谢与许可

- 工程技能改编自 [mattpocock/skills](https://github.com/mattpocock/skills)，
  Copyright (c) 2026 Matt Pocock，[MIT License](https://github.com/mattpocock/skills/blob/main/LICENSE)。
- 产品技能改编自本机 Codex product agent（`~/.codex/agents/product-*.toml`）。
- 界面/上线技能来自全局 skills（`ui-ux-pro-max`、`web-design-guidelines`、`writing-guidelines`、
  `deploy-to-vercel` 及 Vercel 官方 `vercel-react-*`；其中 `vercel-react-*` 为 MIT）。
- 本仓库：MIT License（见 [LICENSE](./LICENSE)）。
- 改编内容：双语描述、删除 Claude Code / Codex 专属配置，新增中文路由技能 `ask-matt`。
  如需再分发非 MIT 来源的技能，请自行确认其许可条款。
