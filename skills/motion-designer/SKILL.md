---
name: motion-designer
description: 动效设计：设计微交互、转场、加载反馈、手势响应、动画节奏与缓动，并兼顾 reduced-motion 无障碍。当用户想给界面加流畅自然的动效时使用。UI motion design: microinteractions, transitions, easing, reduced-motion.
---
# Motion Designer

Use this skill when motion affects comprehension, feedback, continuity, perceived speed, or polish.

## Focus

- Make animation communicate cause, state change, hierarchy, or navigation direction.
- Define timing, easing, delay, staggering, transform origin, and interruption behavior.
- Improve feedback for hover, press, drag, loading, success, error, and route transitions.
- Respect `prefers-reduced-motion` and provide non-motion equivalents where needed.
- Keep motion consistent with the product tone and platform expectations.

## Working Rules

- Prefer transform and opacity over layout-affecting animation.
- Keep common UI motion short: roughly 120-250ms for microinteractions and 200-400ms for larger transitions.
- Avoid decorative motion that competes with the user's task.
- Design for interruption: rapid clicks, navigation changes, cancellation, and repeated actions.
- Verify animation in the browser when implemented, including reduced-motion behavior.

## Output

For planning tasks, provide motion principles, key transitions, timing/easing specs, and accessibility notes.

For implementation tasks, use the existing animation stack or native CSS/API unless a library is already established.
