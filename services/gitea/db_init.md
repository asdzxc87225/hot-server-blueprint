# MariaDB 初始化與 Gitea 資料庫設定紀錄

## 🧰 系統環境

- 裝置：Raspberry Pi 4
- 系統架構：aarch64
- 作業系統：Debian 12 (64-bit Lite)
- 日期：2025-05-05
- 用途：Gitea 版本控制系統資料庫

---

## 📦 安裝 MariaDB Server

```bash
sudo apt install -y mariadb-server
sudo systemctl enable mariadb
sudo systemctl start mariadb
sudo mysql_secure_installation
```
| 問題                              | 回答           |
| ------------------------------- | ------------ |
| Enter current password for root | 直接按 Enter    |
| Set root password?              | Y            |
| New password                    | \*\*\*\*（已設） |
| Remove anonymous users?         | Y            |
| Disallow root login remotely?   | Y            |
| Remove test database?           | Y            |
| Reload privilege tables now?    | Y            |
