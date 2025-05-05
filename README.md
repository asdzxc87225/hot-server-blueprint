# hot-server-blueprint

## 專案簡介
這是一個架設於 Raspberry Pi 上的個人 Hot Server 系統，目的是提供一個內網中可控、可擴展的專案管理中心。它整合 Git Server、筆記平台與自動化備份模組，解決私人資料無法放上公有平台、檔案過大難以同步等問題。

## 背後動機

我希望這個系統能同時實現以下目標：

- 用來集中管理所有私人專案與技術資料
- 當作練習 Linux 系統維運與服務部署的平台
- 解決外部平台難以支援大型檔案與私密內容的限制
- 長期培養 DevOps 能力與自我紀錄的習慣


## 系統功能架構

- ✅ Git Server（使用 Gitea 管理所有原始碼與筆記）
- 🔧 筆記系統（預計使用 MkDocs / Obsidian Git）
- ⏳ 檔案管理模組（考慮使用 File Browser）
- ⏳ 未來模組：
  - API 任務控制台
  - 模型訓練日誌與視覺化分析器
  - 風險分級自動備份模組


## 使用技術與工具
- 作業系統：Debian on Raspberry Pi
- 開源工具：Gitea, MkDocs, Tailscale...
- 語言：Bash, Python, Markdown, YAML

## 目標時程

- 第一週：完成 Gitea 安裝與 Web UI 初始設定
- 第二週：整合 MkDocs 並部署一份筆記網站
- 第三週：建立自動備份腳本並測試多種觸發條件（ex: git push / 定時）
- 第四週：回顧系統運作狀況，整理初步筆記與維運紀錄


## License
MIT License – 詳見 LICENSE 檔案
