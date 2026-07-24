---
name: obsidian
description: Obsidian 筆記助手 —— 用中文管理 Obsidian vault，包含建立筆記、雙向連結、搜尋、模板、與 Notion 同步。當使用者需要整理 Obsidian 知識庫、自動化筆記流程、或跨平台同步時使用。
---

# Obsidian 筆記助手

## 核心定位

Obsidian = 您的**本地第二大腦**。所有筆記都是 Markdown 檔案，AI 直接讀寫。

## 與 Notion 的分工

| | Obsidian（本插件） | Notion |
|---|---|---|
| 資料 | 本地 .md 檔案 | 雲端資料庫 |
| 強項 | 離線、雙向連結、圖譜 | 協作、API、自動化 |
| AI 操作 | 直接讀寫檔案系統 | API 呼叫 |

## 主要場景

| 場景 | 例子 |
|------|------|
| 建立筆記 | 「幫我開一篇新筆記，標題『Docker 學習筆記』」 |
| 搜尋 | 「找出所有提到 Playwright 的筆記」 |
| 雙向連結 | 「把這篇筆記連結到『專案架構』」 |
| 模板 | 「幫我做一個會議記錄模板」 |
| 同步 Notion | 「把這篇筆記匯出到 Notion」 |

## 範例

> 「幫我整理 vault 裡所有未完成的筆記」
> 「幫我建立每日筆記模板，含代辦清單和日記區塊」
> 「搜尋 vault 中有關 API 設計的筆記並列出來」
> 「把這週的 Obsidian 筆記彙整成一篇週報」

## 實作方式

直接讀寫本地 .md 檔案，使用 Obsidian 相容的 Markdown 語法（`[[雙向連結]]`、frontmatter）。

- 先確認 vault 路徑
- 操作前摘要影響範圍
- 保留既有 frontmatter 和連結結構

## 注意事項

- 需確認 Obsidian vault 路徑
- 筆記格式為標準 Markdown + Obsidian 擴展語法
- 大量批次操作前先預覽
