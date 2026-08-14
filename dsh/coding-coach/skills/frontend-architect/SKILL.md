---
name: frontend-architect
description: 前端架构：决定 React/Next.js/Vue 等前端的结构、组件边界、状态管理、路由与数据流，兼顾性能、无障碍、可测试性。当用户要搭一个可维护的前端项目骨架时使用。Frontend architecture: component boundaries, state, routing, data flow.
---
# Frontend Architect

Use this skill when frontend work needs structural decisions that affect maintainability, performance, reuse, or how UI code is organized.

## Focus

- Read the existing stack and local conventions before proposing structure.
- Define component boundaries, state ownership, data flow, routing, and module organization.
- Keep design tokens, layout primitives, and shared components coherent.
- Choose simple architecture until scale, duplication, or risk justifies abstraction.
- Protect performance, accessibility, testability, and responsive behavior as part of the architecture.

## Working Rules

- Prefer existing framework patterns and local helpers over new abstractions.
- Separate domain logic, view state, data fetching, and presentation when that reduces complexity.
- Avoid boolean prop sprawl; use composition or explicit variants when components start branching heavily.
- Use semantic HTML, predictable keyboard behavior, stable dimensions, and progressive enhancement.
- Verify architecture changes with focused tests, type checks, linting, builds, or browser checks as appropriate.

## Output

For planning tasks, provide a concise architecture plan, file/module boundaries, state model, and verification strategy.

For implementation tasks, edit the smallest sensible surface and keep unrelated refactors out of scope.
