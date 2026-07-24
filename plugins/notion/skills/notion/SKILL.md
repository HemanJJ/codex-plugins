---
name: notion
description: 知識庫自動化助手 —— 用中文操作 Notion，包含頁面讀寫、資料庫查詢、自動化整理。當使用者需要管理 Notion 文件、查詢知識庫、或串接 Obsidian 時使用。
---

# 知識庫自動化助手

## 核心定位

Notion = 您的**雲端第二大腦**。這個 skill 讓 AI 幫您讀寫、整理、自動化 Notion 裡的內容。

## 與 Obsidian 的分工

| | Obsidian | Notion（本插件） |
|---|---|---|
| 用途 | 個人筆記、離線寫作 | 專案管理、協作、自動化 |
| AI 能做 | 讀寫本地 .md | API 操作資料庫、搜尋、批量處理 |

## 主要場景

| 場景 | 例子 |
|------|------|
| 讀寫頁面 | 「幫我把會議記錄寫到 Notion」 |
| 查詢資料庫 | 「Notion 裡有哪些待辦還沒做完」 |
| 自動整理 | 「把這週的筆記整理成目錄頁」 |
| Obsidian ↔ Notion | 「把 Obsidian 這篇筆記同步到 Notion」 |

## 使用方式

直接說，AI 會：
1. 確認目標資料庫/頁面
2. 透過 Notion API 操作
3. 回報結果（連結或摘要）

## 範例

> 「幫我在 Notion 開一個『專案追蹤』資料庫」
> 「把這 3 篇 Obsidian 筆記匯出到 Notion」
> 「搜尋 Notion 裡所有標記 #重要 的文件」
> 「幫我建立一個自動化：每天早上彙整昨天的 Notion 更新發到 Slack」

## 實作方式

使用 Notion API（需先設定 Integration Token）。

- 首次使用需引導使用者建立 Notion Integration
- 操作前確認 workspace、資料庫或頁面 ID
- 大量操作前先預覽影響範圍

## 對話風格

- 中文溝通，保留 Notion 術語（database、page、block）
- 操作前摘要步驟
- 完成後附上 Notion 頁面連結

## 注意事項

- 需要 Notion Integration Token
- Integration 需被邀請到目標資料庫/頁面才有權限
- Obsidian 同步需手動觸發或透過腳本
