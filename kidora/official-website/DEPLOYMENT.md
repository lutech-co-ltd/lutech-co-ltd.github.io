# Kidora 網站部署指南

## 部署到 GitHub Pages

### 方法 1：直接上傳到 GitHub 倉庫

1. **準備 GitHub 倉庫**
   - 確保您有 `lutech-co-ltd/lutech-co-ltd.github.io` 倉庫的存取權限

2. **上傳檔案**
   - 在 GitHub 倉庫中建立 `kidora/` 目錄
   - 將 `kidora-website/` 目錄中的所有檔案上傳到 `kidora/` 目錄

3. **設定 GitHub Pages**
   - 前往倉庫 Settings → Pages
   - Source 選擇 `main` 分支
   - 網站將自動發布在 `https://lutech-co-ltd.github.io/kidora/`

### 方法 2：使用 Git 命令

```bash
# 1. 克隆倉庫（如果還沒有）
git clone https://github.com/lutech-co-ltd/lutech-co-ltd.github.io.git
cd lutech-co-ltd.github.io

# 2. 建立 kidora 目錄並複製檔案
mkdir -p kidora
cp -r /path/to/kidora-website/* kidora/

# 3. 提交並推送
git add kidora/
git commit -m "Add Kidora website"
git push origin main
```

## 訪問網站

部署完成後，網站將可在以下網址訪問：

- **中文版**: https://lutech-co-ltd.github.io/kidora/
- **英文版**: https://lutech-co-ltd.github.io/kidora/index-en.html

## 檔案檢查清單

部署前請確認以下檔案存在：

- [ ] `index.html` - 中文版首頁
- [ ] `index-en.html` - 英文版首頁
- [ ] `css/style.css` - 樣式檔案
- [ ] `js/main.js` - JavaScript 檔案
- [ ] `images/icon.png` - App Icon
- [ ] `images/hero/hero_area.png` - Hero 圖片
- [ ] `images/screenshots/` - 應用程式截圖（至少 3 張）
- [ ] `images/decorations/` - 裝飾元素（9 個 SVG）
- [ ] `images/app-store-badge.svg` - App Store 按鈕
- [ ] `images/google-play-badge.svg` - Google Play 按鈕

## 測試檢查

部署後請測試：

- [ ] 中文版頁面正常顯示
- [ ] 英文版頁面正常顯示
- [ ] 語言切換功能正常
- [ ] 所有圖片正常載入
- [ ] 下載按鈕連結正確
- [ ] 響應式設計在手機/平板/桌面正常顯示
- [ ] 所有連結正常運作

## 更新內容

### 更新截圖
1. 將新截圖放在 `images/screenshots/` 目錄
2. 更新 HTML 中的圖片路徑
3. 提交並推送變更

### 更新文字
1. 編輯 `index.html`（中文）或 `index-en.html`（英文）
2. 提交並推送變更

### 更新樣式
1. 編輯 `css/style.css`
2. 提交並推送變更

## 自訂域名（可選）

如果需要使用自訂域名（如 `kidora.com`）：

1. **在 GitHub 設定**
   - 前往倉庫 Settings → Pages
   - 在 Custom domain 輸入您的域名
   - 點擊 Save

2. **設定 DNS 記錄**
   - 在域名註冊商設定以下 DNS 記錄：
   
   **選項 A：根域名**
   ```
   A 記錄: kidora.com → 185.199.108.153
   A 記錄: kidora.com → 185.199.109.153
   A 記錄: kidora.com → 185.199.110.153
   A 記錄: kidora.com → 185.199.111.153
   ```
   
   **選項 B：子域名**
   ```
   CNAME 記錄: www.kidora.com → lutech-co-ltd.github.io
   ```

3. **等待生效**
   - DNS 變更通常需要 24-48 小時生效
   - GitHub 會自動提供 HTTPS 憑證

## 疑難排解

### 圖片無法顯示
- 檢查圖片路徑是否正確
- 確認圖片檔案已上傳
- 檢查檔案名稱大小寫是否正確

### 樣式無法載入
- 檢查 `css/style.css` 路徑是否正確
- 確認檔案已上傳
- 清除瀏覽器快取

### 語言切換不工作
- 檢查 `index.html` 和 `index-en.html` 的連結是否正確
- 確認兩個檔案都存在

## 支援

如有問題，請聯絡：
- Email: lutech.co.ltd@gmail.com

