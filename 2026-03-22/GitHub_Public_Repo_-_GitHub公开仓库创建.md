# GitHub Public Repo - GitHub 公开仓库创建

**来源**: OpenClaw Workspace | **类型**: 工作区技能 | **分类**: 开发工具

自動化創建和管理 GitHub 公開倉庫。

## 基本信息

- **技能名称**: github-public-repo
- **来源**: OpenClaw Workspace
- **标签**: github, repo, public, automation
- **维护状态**: ✅ 正常

## 功能描述

本技能提供完整的 GitHub 公開倉庫創建和管理自動化流程。包含權限驗證、倉庫創建、本地 Git 初始化、文件推送和驗證等完整工作流。

## 使用场景

1. 需要為現有項目創建公開 GitHub 倉庫時
2. 需要將本地項目推送到 GitHub 作為公開項目時
3. 需要測試 GitHub API 權限和連接時
4. 需要標準化公開項目創建流程時
5. 特別適用於從 codes-public 目錄創建公開項目

## 基本使用流程

### 1. 準備工作
- 擁有有效的 GitHub Personal Access Token（具有 `repo` 或 `public_repo` 權限）
- 項目目錄已準備好（推薦放在 `codes-public/` 目錄下）
- 確定倉庫名稱和描述

### 2. 基本使用流程
```python
# 1. 測試 GitHub API 連接和權限
python scripts/test_github_api.py <token> <username>

# 2. 創建公開倉庫
python scripts/create_public_repo.py \
    --token "ghp_xxx" \
    --user "iamtour-openclaw" \
    --repo "project-name" \
    --description "項目描述" \
    --project-dir "/path/to/project"
```

### 3. 完整工作流
```
1. 權限驗證 → 2. 倉庫創建 → 3. 本地初始化 → 4. 文件提交 → 5. 推送 → 6. 驗證
```

## 核心功能

### 1. GitHub API 權限驗證
- 測試 Token 有效性
- 檢查權限範圍（`repo` 或 `public_repo`）
- 驗證用戶身份
- 處理常見錯誤（401、403、速率限制）

### 2. 公開倉庫創建
- 通過 GitHub REST API 創建倉庫
- 配置倉庫屬性（名稱、描述、公開/私有）
- 設置倉庫功能（Issues、Projects、Wiki）

### 3. 本地 Git 管理
- 初始化 Git 倉庫
- 配置 Git 用戶信息
- 創建 .gitignore 文件
- 進行初始提交

### 4. 遠程推送
- 添加遠程倉庫
- 推送分支（默認 main）
- 驗證推送結果

---

*本笔记由 OpenClaw Skills 收集器自动生成*
*生成时间：2026-03-22 19:33*