# MkDocs 筆記系統整合流程紀錄（hot-server-blueprint）

## 🎯 任務目標

在 Raspberry Pi 上整合 MkDocs 作為本地筆記站，支援瀏覽器查看、版本控管與未來擴充自動部署。

---

## ✅ 系統資訊

| 項目 | 值 |
|------|----|
| 作業系統 | Debian 12 |
| 裝置 | Raspberry Pi |
| 使用者 | luu |
| 安裝方式 | Python venv 虛擬環境 |

---

## 📦 安裝流程

### 1. 安裝必要套件

```bash
sudo apt update
sudo apt install -y python3-full python3-venv
```

## 建立虛擬環境

```bash
mkdir -p ~/venvs
python3 -m venv ~/venvs/mkdocs-env
```
## 啟動虛擬環境並安裝 MkDocs

```bash
source ~/venvs/mkdocs-env/bin/activate
pip install --upgrade pip
pip install mkdocs
```
## 初始化站點
```bash
mkdocs new ~/mkdocs_site
cd ~/mkdocs_site
```
## 啟動測試伺服器（允許區網存取）
```bash
mkdocs serve --dev-addr=0.0.0.0:8000
```
## 瀏覽網址

```bash
http://<RaspberryPi-IP>:8000
```

