# my-projects

本仓库是个人学习与知识沉淀的工作仓库，当前围绕 **AI 智能体核心概念** 建立了一套"Skill 规范 + 学习资料"体系。

## 仓库用途

1. **沉淀可复用的 Skill**：把"如何生成某类内容"的标准流程固化成项目级 Skill，供 WorkBuddy 智能体在后续会话中直接调用；
2. **积累结构化学习资料**：按 Skill 规范批量生成概念学习资料（HTML 格式，含个人解释、机制、案例、辨析与可核查来源）；
3. **记录人工核查痕迹**：所有 AI 生成内容均保留【人工核查与修改记录】入口，确保"AI 起草 + 人工把关"的协作模式可追溯。

## Skill 的存放路径

项目级 Skill 统一存放在：

```
.workbuddy/skills/<skill-name>/SKILL.md
```

当前已有：

| Skill 名称 | 路径 | 用途 |
|---|---|---|
| 概念学习资料生成 | `.workbuddy/skills/concept-learning/SKILL.md` | 根据任意输入概念，生成含学习目标、核心问题、结构化解释、应用案例、概念辨析、自测问题、参考来源七部分的结构化学习资料 |

Skill 为通用设计，不绑定特定概念；YAML 元数据中 `name: 概念学习资料生成`，`description: 根据用户输入的概念生成结构化学习资料`。

## 如何在 WorkBuddy 中调用

- **对话调用**：在 WorkBuddy 会话中直接说"使用 concept-learning 技能，帮我生成 XX 概念的学习资料"，智能体会加载对应 SKILL.md 并按其中流程执行；
- **手动触发**：告诉智能体按 `.workbuddy/skills/concept-learning/SKILL.md` 的规范执行，并指定输出文件名与目录；
- **补充要求**：调用时可附加输出格式（如 HTML）、目录位置、额外章节等要求，Skill 流程保持不变。

## 已生成的学习资料

均位于 `learning-materials/` 目录：

| 文件 | 主题 | 内容要点 |
|---|---|---|
| `agent.html` | Agent（智能体） | Agent = 大模型 + 循环 + 工具 + 目标；工作流与自主 Agent 之辨；编程智能体实例 |
| `llm-context.html` | 大模型的上下文 | 上下文即模型当前可见的全部输入；注意力预算；压缩/记忆/即时检索策略 |
| `skill.html` | Skill（智能体技能） | SKILL.md 文件夹结构；渐进式披露三层加载；与工具/MCP 的区别 |
| `concept-relationship.html` | 三概念关系图解 | Mermaid 关系图 + 对照表：执行—供给—沉淀闭环；上下文如何影响 Agent；Skill 如何沉淀知识 |

所有资料中的来源链接均经实际核查（OpenAI 文档站等对自动抓取有限制的站点已在资料内注明）。

## 【人工核查与修改记录】

> 本章节由人工填写，用于记录对 AI 生成内容的核查结论与后续修改。

| 日期 | 核查对象 | 核查人 | 核查结论 / 修改内容 |
|---|---|---|---|
| 2026-09-10 | agent.html、llm-context.html、skill.html、concept-relationship.html | [徐志强] | 我已人工阅读全部生成的HTML学习资料，概念解释准确。我亲自点击并核实了所有的参考资料链接（Anthropic官方博客、agentSkills.io等），均真实有效。我对“Skill”的解释进行了个人语言润色，并确认本仓库不包含API Key及个人隐私信息。 |