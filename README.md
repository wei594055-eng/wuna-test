# WUNA Portal — Netlify + GitHub 部署指南

## 1) 建立 GitHub Repository
```bash
git init
git add .
git commit -m "chore: initial deploy"
git branch -M main
git remote add origin https://github.com/<你的帳號>/<你的repo>.git
git push -u origin main
```

## 2) 連動 Netlify（Import from Git）
- 到 https://app.netlify.com → "Add new site" → "Import from Git"
- 連接 GitHub，選剛剛的 repo
- Build command 留空；Publish directory 使用根目錄（`.`）
- 點 Deploy

## 3) 之後更新（在 VS Code）
```bash
git add .
git commit -m "feat: 對齊自嘲熊與吉伊卡哇"
git push
```
每次 push，Netlify 都會自動重新部署。

## 4) 常見問題
- 沒看到更新？請硬重新整理（Cmd/Ctrl+Shift+R）。
- 有自訂網域：在 Netlify → "Domains" 綁定網域、設定 DNS（會給你 CNAME）。
- 404 頁面：本專案已附 404.html，找不到頁面會顯示友善畫面。
