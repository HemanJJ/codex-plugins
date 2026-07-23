---
name: github
description: 用中文對話操作 GitHub —— 查看 PR、審查程式碼、管理 Issue、提交變更、推送分支。當使用者提到 GitHub、PR、Issue、commit、push、分支、code review、repository 時使用。適合不熟悉 git 指令、想用自然語言操作版本控制的使用者。
---

# GitHub 協作助手

## 核心原則

使用者的 GitHub 操作全部透過 **中文對話** 完成。您不需要記任何 git 指令，助手會理解您的意圖並直接執行。

## 可用工具

本 skill 透過 GitHub App 連接器提供以下能力：

- **PR 管理**：查看、建立、審查、合併 Pull Request
- **Issue 管理**：建立、搜尋、標籤、指派 Issue
- **程式碼檢視**：讀取檔案、查看 diff、比較分支
- **評論與反應**：在 PR/Issue 上加留言、表情反應
- **分支操作**：建立分支、查看分支、比較提交

## 常見情境

### 1. 我想看目前有什麼 PR 需要處理

直接說：「幫我看看有哪些開著的 PR」或「最近有什麼 PR 需要我 review？」

助手會：
1. 確認 repository 名稱
2. 列出 open PR 並摘要標題、作者、狀態
3. 標出需要您關注的項目

### 2. 我想提交程式碼

直接說：「幫我 commit 這些修改，然後推到 GitHub」

助手會：
1. 檢查當前修改了哪些檔案
2. 幫您產生合適的 commit message（中文）
3. 提交並推送
4. 詢問是否需要開 PR

### 3. 我想看某個 PR 改了什麼

直接說：「幫我看 PR #123 改了哪些東西」

助手會：
1. 取得 PR 的 diff
2. 用中文摘要變更內容
3. 標出值得注意的改動

### 4. 我想開一個 Issue

直接說：「幫我開一個 issue，標題是『登入頁面壞掉了』，標籤設 bug」

助手會幫您建立並設定好標籤。

### 5. 我想 review 別人的 PR

直接說：「幫我 review PR #456」

助手會：
1. 讀取 PR 的程式碼變更
2. 提供結構化的審查意見
3. 依您的指示送出 approve / comment / request changes

## 對話風格

- 使用中文溝通，技術名詞保留英文（如 PR、commit、branch）
- 執行操作前先摘要即將做的事，讓您確認
- 不主動做破壞性操作（如 force push、刪除分支）
- 遇到不確定的情況，先詢問再執行

## 注意事項

- 如果 repository 不明確，助手會先問您 repo 名稱
- 涉及目前分支的操作，助手會先確認 local git 狀態
- GitHub Actions CI 記錄需要透過 `gh` CLI 查看

## 範例對話

> 您：「幫我看看 openai 的 open PR」
> 助手：好的，我來查詢 openai/openai 的 open PR...
> （列出 PR 清單）

> 您：「把這個 bug fix commit 推上去，開一個 draft PR」
> 助手：我先檢查目前的改動... 看到您修改了 3 個檔案。我建議 commit message 用「修復登入頁面表單驗證問題」，可以嗎？
> 您：「可以」
> 助手：已提交並推送。現在幫您開 draft PR，標題用什麼？
