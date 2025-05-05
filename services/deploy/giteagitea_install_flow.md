# Gitea 安裝與部署流程紀錄（hot-server-blueprint）

## 📌 系統資訊

| 項目         | 值                         |
|--------------|----------------------------|
| 裝置         | Raspberry Pi               |
| 系統版本     | Debian 12 (Bookworm) 64bit |
| 架構         | aarch64                    |
| Gitea 版本   | 1.23.7                     |
| 執行方式     | systemd                    |
| Gitea 使用者 | `gitea`                    |

---

## 📦 軟體安裝步驟

### 1. 安裝 MariaDB

```bash
sudo apt update
sudo apt install -y mariadb-server
sudo systemctl enable mariadb
sudo systemctl start mariadb
sudo mysql_secure_installation
```
```
CREATE DATABASE gitea CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
CREATE USER 'gitea'@'localhost' IDENTIFIED BY 'YourSuperPassword';
GRANT ALL PRIVILEGES ON gitea.* TO 'gitea'@'localhost';
FLUSH PRIVILEGES;
```
```
wget -O gitea https://dl.gitea.com/gitea/1.23.7/gitea-1.23.7-linux-arm64
chmod +x gitea
sudo mv gitea /usr/local/bin/

