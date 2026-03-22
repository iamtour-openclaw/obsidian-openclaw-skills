# Self-Improving Agent - 自我改进代理

**来源**: OpenClaw Workspace | **类型**: 工作区技能 | **分类**: 效率工具

Captures learnings, errors, and corrections to enable continuous improvement.

## 基本信息

- **技能名称**: self-improvement
- **来源**: OpenClaw Workspace
- **标签**: learning, improvement, errors, continuous
- **维护状态**: ✅ 正常

## 功能描述

Log learnings and errors to markdown files for continuous improvement. Coding agents can later process these into fixes, and important learnings get promoted to project memory.

## 快速参考

| 场景 | 操作 |
|-----------|--------|
| 命令/操作失败 | 记录到 `.learnings/ERRORS.md` |
| 用户纠正你 | 记录到 `.learnings/LEARNINGS.md`，分类为 `correction` |
| 用户要求不存在的能力 | 记录到 `.learnings/FEATURE_REQUESTS.md` |
| API/外部工具失败 | 记录到 `.learnings/ERRORS.md`，包含集成详情 |
| 知识过时 | 记录到 `.learnings/LEARNINGS.md`，分类为 `knowledge_gap` |
| 发现更好的方法 | 记录到 `.learnings/LEARNINGS.md`，分类为 `best_practice` |
| 与现有条目相似 | 使用 `**See Also**` 链接，考虑提升优先级 |
| 广泛适用的学习 | 提升到 `CLAUDE.md`、`AGENTS.md` 和/或 `.github/copilot-instructions.md` |
| 工作流改进 | 提升到 `AGENTS.md` (OpenClaw workspace) |
| 工具陷阱 | 提升到 `TOOLS.md` (OpenClaw workspace) |
| 行为模式 | 提升到 `SOUL.md` (OpenClaw workspace) |

## 记录位置

### 1. 错误日志 (.learnings/ERRORS.md)
- 命令或操作意外失败
- 外部 API 或工具失败

### 2. 学习日志 (.learnings/LEARNINGS.md)
- 用户纠正 (correction)
- 知识差距 (knowledge_gap)
- 最佳实践 (best_practice)

### 3. 功能请求 (.learnings/FEATURE_REQUESTS.md)
- 用户要求的不存在的能力

## OpenClaw 设置

### 工作区结构

OpenClaw 在每个会话中注入以下文件：

```
~/.openclaw/workspace/
├── AGENTS.md          # Multi-agent workflows, delegation patterns
├── SOUL.md            # Behavioral guidelines, personality, principles
├── TOOLS.md           # Tool capabilities, integration gotchas
├── USER.md            # User context and preferences
├── MEMORY.md          # Long-term memory
└── memory/            # Daily session logs
```

### 提升规则

- **行为模式** → `SOUL.md`
- **工作流改进** → `AGENTS.md`
- **工具陷阱** → `TOOLS.md`

---

*本笔记由 OpenClaw Skills 收集器自动生成*
*生成时间：2026-03-22 19:33*