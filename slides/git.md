---
marp: true
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

# **認識 GIT 與常用指令**

---

# What is GIT?

Git 是一個分散式版本控制系統，廣泛應用於軟體開發中。它能夠管理程式碼的變更記錄，提供方便的協作機制。

最早的版本控制就是反覆複製資料夾，並以資料夾命名來記錄不同的程式碼狀態。後來就發展出版本控制系統，並分為集中式版本控制系統和分散式版本控制系統。

集中式版本控制系統對中央伺服器的依賴，單點故障風險高，且協作效率較低。Git 的分散式架構解決了這些問題，每個使用者都有完整的儲存庫，可以在本地進行操作，無需中央伺服器的持續連線。

---

# GIT 相關名詞解釋

版本控制系統：版本控制系統用於追蹤文件或程式碼的變更歷史。

分散式版本控制系統：每個使用者都擁有一個完整的儲存庫，可以在本地進行操作，無需依賴中央伺服器。

工作區、暫存區和儲存庫：工作區是您當前工作目錄，暫存區是將要提交的變更暫存區域，儲存庫是包含所有歷史記錄的地方。

---

# GIT 基本指令

```bash
# 初始化儲存庫
$ git init
# 從遠端儲存庫複製
$ git clone
# 儲存目前工作的變更
$ git add
# 提交變更至儲存庫
$ git commit
# 從遠端儲存庫更新本地儲存庫
$ git pull
# 上傳本地變更至遠端儲存庫
$ git push
```

---

# GIT 的分支管理

```bash
# 創建分支
$ git branch

# 切換分支
$ git checkout

# 合併分支
$ git merge
```

---

# GIT SSH 金鑰操作步驟

1. 產生 SSH 金鑰
```
$ ssh-keygen -t ed25519 -C "yourname@email.com"
```
2. 印出公鑰資訊
```
$ cd ~/.ssh
$ cat id_ed25519.pub
```
3. 將公鑰資訊貼到 GitHub 網站

---

# 設定 GTI 基本設定

為了讓你建立的 git commit 會是記錄正確的名稱和 Email，要進行全域的設定變更

```bash
$ git config --global user.name "Your Name"
$ git config --global user.email "yourname@email.com"
```