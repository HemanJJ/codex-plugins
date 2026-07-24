---
name: cloudflare
description: 一鍵上線助手 —— 用 Cloudflare Tunnel 取代 ngrok 暴露本地服務、部署網站、管理 domain 與 DNS。當使用者想把 localhost 公開到網路上、部署前端專案、或需要固定公網網址時使用。
---

# 一鍵上線助手

## 核心定位

**ngrok 的免費替代方案。** 一鍵把 localhost 變成固定公網網址，不用每次重開就換 URL。

## 主要場景

| 場景 | 做法 |
|------|------|
| 暴露本地服務 | `cloudflared tunnel` → 固定網址 |
| 部署靜態網站 | `wrangler pages deploy` → 全球 CDN |
| 寫 API 不求伺服器 | `wrangler dev` → Workers 即時上線 |

## 使用方式

直接說，AI 會：
1. 確認要暴露的本地埠號（如 3000、8080）
2. 檢查/安裝 cloudflared
3. 建立 tunnel → 回傳固定公網網址

## 範例

> 「幫我把 localhost:3000 開到公網，我要給客戶看」
> 「幫我把這個 Next.js 專案部署上線」
> 「我有 domain，幫我設定 HTTPS + 自動續約」
> 「幫我裝 cloudflared，取代 ngrok」

## 實作方式

使用 `cloudflared` CLI 或 `wrangler` CLI。

- 先確認 cloudflared 是否已安裝，若無則引導安裝
- Tunnel 建立後回傳固定網址
- Domain 相關操作需先確認使用者已擁有 domain

## 對話風格

- 中文溝通，工具/指令保留原文
- 操作前確認埠號、專案路徑
- 完成後回傳網址，讓您直接點開測試

## 注意事項

- macOS 環境
- Cloudflare 帳號需先註冊（免費）
- cloudflared 安裝：`brew install cloudflared`
