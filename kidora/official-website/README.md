# Kidora 官方網站

Kidora 一頁式行銷網頁，支援中英文雙語版本。

## 檔案結構

```
kidora-website/
├── index.html          # 中文版首頁
├── index-en.html       # 英文版首頁
├── css/
│   └── style.css      # 樣式檔案
├── js/
│   └── main.js        # 互動腳本
└── images/
    ├── icon.png       # App Icon
    ├── decorations/   # 裝飾元素（SVG）
    ├── hero/          # Hero 區塊圖片
    ├── screenshots/   # 應用程式截圖
    ├── app-store-badge.svg    # App Store 下載按鈕
    └── google-play-badge.svg  # Google Play 下載按鈕
```

## 功能特色

- ✅ 響應式設計（RWD）
- ✅ 中英文雙語版本
- ✅ 平滑滾動動畫
- ✅ 互動式元素
- ✅ SEO 優化
- ✅ 使用 Kidora 品牌色彩

## 部署到 GitHub Pages

### 步驟 1：上傳到 GitHub 倉庫

1. 將 `kidora-website` 目錄的內容上傳到 `lutech-co-ltd.github.io` 倉庫的 `kidora/` 目錄

2. 或使用 Git 命令：
```bash
cd kidora-website
git init
git add .
git commit -m "Add Kidora website"
git remote add origin https://github.com/lutech-co-ltd/lutech-co-ltd.github.io.git
git push -u origin main
```

### 步驟 2：設定 GitHub Pages

1. 前往 GitHub 倉庫設定頁面
2. 在 "Pages" 設定中選擇分支和資料夾
3. 如果放在 `kidora/` 子目錄，需要設定正確的路徑

### 步驟 3：訪問網站

- 中文版：`https://lutech-co-ltd.github.io/kidora/`
- 英文版：`https://lutech-co-ltd.github.io/kidora/index-en.html`

## 自訂域名設定（可選）

如果需要使用自訂域名（如 `kidora.com`）：

1. 在 GitHub 倉庫設定中添加自訂域名
2. 在域名註冊商設定 DNS 記錄
3. 等待 DNS 生效（24-48 小時）

## 品牌色彩

- 珊瑚橘: `#f3a683`
- 蜜桃奶油: `#f8c291`
- 童趣藍: `#546de5`
- 粉嫩紅: `#ffb8b8`
- 主背景: `#fffaf6`
- 次要背景: `#fdf1e7`

## 更新內容

### 更新截圖
將新的截圖放在 `images/screenshots/` 目錄，並更新 HTML 中的圖片路徑。

### 更新文字
直接編輯 `index.html`（中文）或 `index-en.html`（英文）。

### 更新樣式
編輯 `css/style.css` 檔案。

## 注意事項

- 確保所有圖片路徑正確
- 測試響應式設計在不同裝置上的顯示
- 檢查中英文版本的連結是否正確
- 確認下載按鈕連結正確

## 聯絡資訊

- Email: lutech.co.ltd@gmail.com
- 開發者: Lutech Co., Ltd.

