# Gitea 安裝與部署筆記

## 模組功能說明
Gitea 是一套輕量級 Git 伺服器，部署於本機作為所有原始碼與筆記的集中管理中心。使用 Web UI 介面管理專案與使用者。

---

## 📚 參考資料

- Gitea 官方文件：https://docs.gitea.io/en-us/
- Raspberry Pi 上部署 Gitea 教學（Community）：[連結 1]
- systemd 服務設定參考：https://docs.gitea.io/en-us/linux-service/
- 安裝腳本參考（shell script）：[連結 2]
- GitHub 倉庫（gitea/gitea）：https://github.com/go-gitea/gitea

> 補註：之後所有模組都會維護這樣一份「參考與實作記錄」，作為系統信賴性的基礎

---

## 📝 待辦事項（尚未實作）

- [ ] 新增 Gitea 使用者與資料夾
- [ ] 撰寫安裝流程腳本（install_gitea.sh）
- [ ] 測試 systemd 自動啟動與服務穩定性
- [ ] 撰寫備份與資料遷移說明
- [ ] 進行首次 Web 設定並初始化 repo 結構
