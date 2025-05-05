# Gitea 部署實驗記錄（手動部署 v1）

## 🧪 環境資訊

- 裝置：Raspberry Pi 4
- 架構：aarch64
- 系統：Debian 11 (Raspberry Pi OS 64-bit Lite)
- 日期：2025-05-05

---

## ✅ 實作流程紀錄

1. 安裝相依套件（`git`, `wget`, `sqlite3`）
2. 建立 `gitea` 專用使用者與資料夾
3. 下載並安裝 Gitea 執行檔
4. 建立 systemd 啟動服務
5. 成功啟動並開啟瀏覽器介面

---

## ❌ 錯誤紀錄

### ❌ 下載錯誤

```bash
wget -O gitea https://dl.gitea.io/gitea/1.21.4/gitea-1.21.4-linux-arm-7
