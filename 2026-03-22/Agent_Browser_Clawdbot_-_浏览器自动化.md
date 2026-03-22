# Agent Browser Clawdbot - 浏览器自动化

**来源**: OpenClaw Workspace | **类型**: 工作区技能 | **分类**: 自动化工具

Headless browser automation CLI optimized for AI agents with accessibility tree snapshots and ref-based element selection.

## 基本信息

- **技能名称**: agent-browser
- **来源**: OpenClaw Workspace
- **标签**: browser, automation, headless, ai
- **维护状态**: ✅ 正常
- **依赖**: agent-browser 命令

## 功能描述

Fast browser automation using accessibility tree snapshots with refs for deterministic element selection. 为 AI 代理优化的无头浏览器自动化 CLI。

## 与内置浏览器的比较

**使用 agent-browser 的场景:**
- 自动化多步骤工作流
- 需要确定性元素选择
- 性能至关重要
- 处理复杂的 SPA
- 需要会话隔离

**使用内置浏览器的场景:**
- 需要截图/PDF 进行分析
- 需要视觉检查
- 需要浏览器扩展集成

## 核心工作流

```bash
# 1. 导航和快照
agent-browser open https://example.com
agent-browser snapshot -i --json

# 2. 从 JSON 解析 refs，然后交互
agent-browser click @e2
agent-browser fill @e3 "text"

# 3. 页面变化后重新快照
agent-browser snapshot -i --json
```

## 关键命令

### 导航
```bash
agent-browser open <url>
agent-browser back | forward | reload | close
```

### 快照 (始终使用 -i --json)
```bash
agent-browser snapshot -i --json          # 交互元素，JSON 输出
```

### 交互
```bash
agent-browser click @<ref>
agent-browser fill @<ref> "<text>"
agent-browser select @<ref> "<option>"
agent-browser press @<ref> <key>
```

### 评估
```bash
agent-browser evaluate "<javascript>"
```

## 相关链接

- [GitHub: vercel-labs/agent-browser](https://github.com/vercel-labs/agent-browser)

---

*本笔记由 OpenClaw Skills 收集器自动生成*
*生成时间：2026-03-22 19:33*