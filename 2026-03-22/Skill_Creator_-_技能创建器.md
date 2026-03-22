# Skill Creator - 技能创建器

**来源**: OpenClaw Bundled | **类型**: 官方技能 | **分类**: 开发工具

创建或更新 AgentSkills.

## 基本信息

- **技能名称**: skill-creator
- **来源**: openclaw-bundled
- **路径**: ~\AppData\Roaming\npm\node_modules\openclaw\skills\skill-creator\SKILL.md
- **标签**: skill, create, update, agent
- **维护状态**: ✅ 正常

## 功能描述

创建或更新 AgentSkills。当从头创建新技能或被要求改进、审查、审计、整理或清理现有技能或 SKILL.md 文件时使用。 也适用于编辑或重构技能目录（将文件移动到 references/ 或 scripts/、删除过时内容、针对 AgentSkills 规范进行验证）。

## 触发关键词

- "create a skill"
- "author a skill"
- "tidy up a skill"
- "improve this skill"
- "review the skill"
- "clean up the skill"
- "audit the skill"

## 技能规范

每个 AgentSkill 应包含:
1. **SKILL.md** - 技能定义文件
2. **references/** - 参考文档目录
3. **scripts/** - 可执行脚本目录（可选）

### SKILL.md 结构

```yaml
---
name: skill-name
description: "技能描述"
metadata: { "openclaw": { "emoji": "🎯", "requires": { "bins": ["命令"] } } }
---

# Skill Name

技能详细描述...

## When to Use

✅ **USE this skill when:**
- 具体使用场景...

## When NOT to Use

❌ **DON'T use this skill when:**
- 不适用的场景...

## Commands/Usage

详细使用方法...

## Examples

使用示例...
```

## 相关链接

- [OpenClaw Skills 文档](https://docs.openclaw.ai/skills)
- [AgentSkills 规范](https://github.com/openclaw/openclaw/blob/main/docs/skills.md)

---

*本笔记由 OpenClaw Skills 收集器自动生成*
*生成时间：2026-03-22 19:33*