# Skill Vetter - 技能审核

**来源**: OpenClaw Workspace | **类型**: 工作区技能 | **分类**: 安全工具

Security-first skill vetting for AI agents.

## 基本信息

- **技能名称**: skill-vetter
- **来源**: openclaw-workspace
- **路径**: ~\.openclaw\workspace\skills\skill-vetter-1-0-0\SKILL.md
- **标签**: security, vetting, audit, skill
- **维护状态**: ✅ Ready

## 功能描述

在从 ClawdHub、GitHub 或其他来源安装任何技能之前使用。检查危险信号、权限范围和可疑模式。

## 使用场景

✅ **使用此技能的场景:**
- 安装来自第三方来源的技能之前
- 审查未知技能的权限范围
- 检测可疑的技能行为
- 审计现有技能的安全性

❌ **不使用此技能的场景:**
- 安装官方认证的技能
- 已经过安全审计的技能

## 安全检查项目

### 1. 危险信号检测
- 可疑的网络请求
- 异常的权限请求
- 隐藏的代码行为

### 2. 权限范围分析
- 文件系统访问权限
- 命令执行权限
- 网络通信权限

### 3. 可疑模式识别
- 数据外发迹象
- 凭证收集行为
- 持久化机制

## 使用方法

```bash
# 使用 skill-vetter 检查技能
# 在安装技能前运行安全审核
```

## 相关链接

- [ClawHub](https://clawhub.com)
- [OpenClaw 安全文档](https://docs.openclaw.ai/security)

---

*本笔记由 OpenClaw Skills 收集器自动生成*
*生成时间：2026-03-22 19:33*