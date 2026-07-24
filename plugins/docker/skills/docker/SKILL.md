---
name: docker
description: Docker 容器管理助手 —— 用中文操作 Docker，包含啟動容器、建置映像檔、管理 Docker Compose、除錯容器。當使用者需要跑容器、部署服務、或想用 Docker 取代手動安裝環境時使用。
---

# Docker 容器助手

## 核心定位

不用記 docker 指令，說要做什麼，AI 幫你下。

## 主要場景

| 場景 | 例子 |
|------|------|
| 跑服務 | 「幫我用 Docker 跑一個 PostgreSQL」 |
| 建映像 | 「幫我把這個專案包成 Docker image」 |
| Compose | 「幫我寫 docker-compose，前端+後端+DB」 |
| 除錯 | 「這個 container 一直重啟，幫我看原因」 |
| 清理 | 「幫我清掉沒在用的 image 和 container」 |

## 範例

> 「幫我起一個 MySQL，port 3306，密碼設 root123」
> 「幫我把這個 Node.js 專案打包成 Docker image」
> 「幫我寫一份 docker-compose.yml，包含 nginx + api + redis」
> 「這個 container 掛了，幫我看 log 找原因」

## 實作方式

使用本地 docker CLI。先確認 Docker 已安裝，操作前摘要指令，完成後回報關鍵資訊。

## 注意事項

- macOS 環境，需先安裝 Docker Desktop
- 不自動刪除 volume 除非明確要求
