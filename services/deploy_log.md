# Gitea 安裝實驗流程紀錄

此文件紀錄 Gitea 在 Raspberry Pi 上的部署過程、反覆測試記錄與流程優化目標，最終將產出一套完整可重現的安裝腳本與維運機制。

---

## 🎯 實驗目標

- 在乾淨的 Debian/Raspberry Pi OS 上部署 Gitea
- 透過腳本實現一鍵部署
- 測試 systemd 啟動穩定性與權限設定
- 評估備份與資料遷移機制

---

## 📦 作業系統環境

- OS: Raspberry Pi OS Lite (32-bit)
- 版本: 2025-04-01 版
- 燒錄方式: Raspberry Pi Imager
- 使用者帳號：`pi` / root

---

## 📚 參考資料

- [Gitea 官方文件](https://docs.gitea.io/en-us/)
- [systemd 設定教學](https://docs.gitea.io/en-us/linux-service/)
- [腳本參考來源](https://github.com/go-gitea/gitea)

---

## 🛠️ 安裝流程（手動實測紀錄）

### Step 1：安裝必要相依套件

```bash
sudo apt update
sudo apt install -y git wget sqlite3 unzip
