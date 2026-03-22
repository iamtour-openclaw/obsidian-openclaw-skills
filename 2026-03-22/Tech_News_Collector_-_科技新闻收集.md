# Tech News Collector - 科技新闻收集

**来源**: OpenClaw Workspace | **类型**: 工作区技能 | **分类**: 资讯收集

自动收集、分析当天最新的科技新闻，保存到 Obsidian 笔记库，并推送到 GitHub 公开仓库。

## 基本信息

- **技能名称**: tech-news-collector
- **来源**: OpenClaw Workspace
- **标签**: news, tech, collector, automation
- **维护状态**: ✅ 正常

## 功能描述

1. **新闻搜索**：搜索当天最新的科技新闻
2. **内容分析**：AI 分析新闻内容，提取关键信息
3. **笔记生成**：创建标准化的 Obsidian Markdown 文件
4. **自动推送**：Git 提交并推送到 GitHub 仓库
5. **定时执行**：每天两次自动运行（7:30 AM 和 7:00 PM）

## 使用场景

- 自动维护科技新闻笔记库
- 跟踪科技行业动态
- 创建公开的知识库
- 个人学习和研究参考

## 激活条件

当用户提到以下内容时激活此技能：
- "收集科技新闻"
- "更新 obsidian-tech-notes"
- "科技新闻自动收集"
- "定时收集新闻"

## 前置要求

1. GitHub PAT (Personal Access Token)
2. 已存在的 obsidian-tech-notes 仓库
3. Python 环境（用于脚本执行）

## 配置

### 环境变量
```bash
# GitHub 配置
GITHUB_TOKEN=ghp_xxx
GITHUB_USER=iamtour-openclaw
GITHUB_REPO=obsidian-tech-notes

# 项目路径
OBSIDIAN_NOTES_PATH=C:\Users\Tour\.openclaw\workspace\codes-public\obsidian-tech-notes
```

### 定时任务配置
```bash
# 早上 7:30
0 7 * * * openclaw cron run --label tech-news-morning

# 晚上 7:00  
0 19 * * * openclaw cron run --label tech-news-evening
```

## 输出内容

### Obsidian 笔记
- 每日新闻索引
- 单个新闻笔记（按主题分类）
- 收集报告

### GitHub 仓库
- 自动推送到 obsidian-tech-notes 公开仓库
- 按日期组织目录结构

---

*本笔记由 OpenClaw Skills 收集器自动生成*
*生成时间：2026-03-22 19:33*