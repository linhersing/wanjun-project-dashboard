# 萬軍專案狀態看板

這個 repository 只保存 GitHub-safe 的專案狀態網站，目的是讓手機可以直接開啟目前進度看板。

正式系統程式仍保存在 private repository：`wanjun-internal-system-runtime`。

## 安全邊界

本 repo 不保存：

- F/H 原始資料、照片、影片、Office、PDF
- 真實 driveId、磁碟代號、完整本機路徑
- SQLite、logs、runtime、cache、temp
- deploy key、token、密碼、secrets
- 未遮蔽的正式資料截圖

## 網站

預期 GitHub Pages 網址：

https://linhersing.github.io/wanjun-project-dashboard/

## 更新規則

之後只要使用者更新需求、修正資訊、調整風險、改變驗收狀態或新增重要指令，Codex 必須同步更新本看板，不需使用者另外提醒。

每次更新仍必須遵守 GitHub-safe 規則，不得加入正式資料、真實 driveId、完整本機路徑、secrets、SQLite、logs、runtime 或未遮蔽截圖。
