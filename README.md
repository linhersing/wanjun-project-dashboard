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

主要看板：

https://linhersing.github.io/wanjun-project-dashboard/project-dashboard/

## 2026-07-05 到 2026-07-06 摘要

- F 硬碟：穩定冷凍線，目前不碰。
- H 硬碟：H-wide Explorer 實驗驗收候選版。
- private repo：`wanjun-internal-system-runtime`，保存程式、測試、文件、版本紀錄，不放正式資料。
- public dashboard repo：`wanjun-project-dashboard`，保存 GitHub-safe 專案報告，供手機與 Gemini 查看。
- main：尚未合併 H-wide Explorer。
- VERSION：仍為 `v2026.07.01-18`。
- F/H 原始資料同步：未做。
- H 正式根目錄 BAT：尚未整合 H-wide Explorer。
- Word / Excel / PowerPoint 真實視窗開啟：仍待人工驗收。

H-wide Explorer 參考 commit：

`936d5081c917a91549f6cc2893fd9ea63c6862f5`

機械驗證摘要：

`PASS 46 / FAIL 0 / PENDING_MANUAL 3 / NOT_IN_SCOPE 0`

## 更新規則

之後只要使用者更新需求、修正資訊、調整風險、改變驗收狀態或新增重要指令，Codex 必須同步更新本看板，不需使用者另外提醒。

每次更新仍必須遵守 GitHub-safe 規則，不得加入正式資料、真實 driveId、完整本機路徑、secrets、SQLite、logs、runtime 或未遮蔽截圖。

## F/H 狀態偵測原則

手機上的 GitHub Pages 網站不能直接偵測本機 USB 硬碟，不能讀取 F/H、driveId、磁碟路徑或本機檔案。未來若要自動顯示 F/H 狀態，應由 Windows 本機工具產生 GitHub-safe 摘要，再更新本 repo。

允許公開的摘要只能包含遮蔽後狀態，例如：

- F 是否維持冷凍穩定基準
- H 是否仍為實驗硬碟
- 程式版本與分支
- 索引 generation 或最後更新時間的安全摘要
- PASS / FAIL / PENDING_MANUAL / NOT_IN_SCOPE 統計

不得公開真實 driveId、完整本機路徑、SQLite、logs、runtime、原始資料內容或未遮蔽截圖。
