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

## 2026-07-05 到 2026-07-07 摘要

- F 硬碟：穩定冷凍線，目前不碰。
- H 硬碟：H-wide Explorer 實驗成果存在，但 2026-07-07 實機入口驗收未通過。
- private repo：`wanjun-internal-system-runtime`，保存程式、測試、文件、版本紀錄，不放正式資料。
- public dashboard repo：`wanjun-project-dashboard`，保存 GitHub-safe 專案報告，供手機與 Gemini 查看。
- main：尚未合併 H-wide Explorer。
- VERSION：仍為 `v2026.07.01-18`。
- F/H 原始資料同步：未做。
- H 正式根目錄 BAT / 實機入口：尚未整合 H-wide Explorer；使用者目前開到的是正式照片年會頁。
- Word / Excel / PowerPoint 真實視窗開啟：仍待人工驗收。

H-wide Explorer 參考 commit：

`936d5081c917a91549f6cc2893fd9ea63c6862f5`

機械驗證摘要：

`PASS 46 / FAIL 0 / PENDING_MANUAL 3 / NOT_IN_SCOPE 0`

2026-07-07 實機校正：

- 使用者在公司電腦以 H 硬碟測試時，瀏覽器顯示的是正式「萬軍照片資料庫」年會頁。
- 該頁沒有新增資料夾、重新命名、複製、剪下、貼上等 H-wide Explorer 操作。
- 唯讀檢查顯示照片年會頁可開，但 `/__wanjun/h-explorer` 回 404。
- 因此 H-wide Explorer 目前仍應標示為「實驗線成果尚未接到使用者手上的 H 實機入口」，不能宣稱正式可用。
- 下一步應先做 H-only 入口或部署校正，再重新進行實機驗收。

2026-07-07 後續修正 commit：

`fdb49f9`

- 修正刪除照片後仍留下破圖卡片的問題：若 SQLite 還標示 active 但實體檔案已不存在，feature 分支會標記 removed 並從結果排除。
- 圖片載入失敗時會移除卡片，不再留下破損圖片格。
- H-wide Explorer 啟動設定改為只在 `driveRole=backup` 時自動啟用，並在資料中心首頁顯示入口。
- 實機診斷仍顯示 H 角色設定為 `unknown`，因此尚未宣稱 H-wide Explorer 正式可用；下一步需先受控確認 H 角色與入口部署。

## 更新規則

之後只要使用者更新需求、修正資訊、調整風險、改變驗收狀態或新增重要指令，Codex 必須同步更新本看板，不需使用者另外提醒。

每次更新仍必須遵守 GitHub-safe 規則，不得加入正式資料、真實 driveId、完整本機路徑、secrets、SQLite、logs、runtime 或未遮蔽截圖。

## 2026-07-24 最新狀態

- H 照片後台與前台的一致性缺陷已修正並完成 H 實機頁面檢查。
- 上架資料夾會索引子項目；重新命名會移除舊路徑並建立新路徑；移到安全回收區後，前台項目與沒有內容的分類卡會一起消失。
- 尼泊爾 2026 實機結果只保留有內容的 01 月；空白 07 月與錯誤的待確認月份卡已消失。
- 「一個檔案看起來有兩個格子」已修正：月份／相簿改為段落導覽，實際檔案才顯示內容卡；H 實機確認指定檔案卡 1、重複相對路徑 0。
- 後台最近上架成功紀錄預設顯示 5 筆，可展開最近 32 筆，避免資料增加後頁面無限制拉長。
- 同版號更新時，啟動器會確認目前服務是否真的載入新程式，避免重新點入口後仍看到舊畫面。
- runtime feature commits：`51c6a0f`、`869105b`、`aa9a14b`。
- 窗口行政正式前台仍未完成全站動態整合，整套後台尚不可宣稱正式完成。
- F 未碰、main 未合併、VERSION 仍為 `v2026.07.01-18`、未做 F/H 或其他硬碟的原始資料同步。任何整碟複製前必須先核對永久硬碟身分、來源／目的與唯讀差異清單，再取得人工批准。

## F/H 狀態偵測原則

手機上的 GitHub Pages 網站不能直接偵測本機 USB 硬碟，不能讀取 F/H、driveId、磁碟路徑或本機檔案。未來若要自動顯示 F/H 狀態，應由 Windows 本機工具產生 GitHub-safe 摘要，再更新本 repo。

允許公開的摘要只能包含遮蔽後狀態，例如：

- F 是否維持冷凍穩定基準
- H 是否仍為實驗硬碟
- 程式版本與分支
- 索引 generation 或最後更新時間的安全摘要
- PASS / FAIL / PENDING_MANUAL / NOT_IN_SCOPE 統計

不得公開真實 driveId、完整本機路徑、SQLite、logs、runtime、原始資料內容或未遮蔽截圖。
