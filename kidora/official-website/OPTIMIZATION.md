# Kidora 網站優化指南

## 當前檔案大小問題

發現以下大檔案導致載入緩慢：

- `images/hero/hero_area.png`: **2.5MB** ⚠️ 太大
- `images/icon.png`: **1.0MB** ⚠️ 太大
- 截圖檔案: 300-600KB 每個

## 優化建議

### 1. 壓縮圖片（最重要）

#### Hero 圖片優化
- **目標大小**: < 200KB
- **工具**: 
  - [TinyPNG](https://tinypng.com/) - 線上壓縮
  - [Squoosh](https://squoosh.app/) - Google 的圖片壓縮工具
  - [ImageOptim](https://imageoptim.com/) - Mac 應用程式

#### Icon 優化
- **目標大小**: < 50KB
- **建議**: 使用較小的尺寸（256x256 或 512x512）

#### 截圖優化
- **目標大小**: < 150KB 每個
- **建議**: 使用 WebP 格式或壓縮 PNG

### 2. 已完成的優化

✅ 添加圖片懶加載（lazy loading）
✅ 添加關鍵資源預載入（preload）
✅ Hero 圖片使用 eager loading（優先載入）

### 3. 進一步優化建議

#### 使用 WebP 格式
```html
<picture>
  <source srcset="images/hero/hero_area.webp" type="image/webp">
  <img src="images/hero/hero_area.png" alt="Kidora App">
</picture>
```

#### 使用響應式圖片
```html
<img srcset="
  images/hero/hero_area-small.png 480w,
  images/hero/hero_area-medium.png 768w,
  images/hero/hero_area-large.png 1200w
" sizes="(max-width: 768px) 100vw, 50vw"
src="images/hero/hero_area-medium.png" alt="Kidora App">
```

#### 壓縮 CSS 和 JS
- 使用 minified 版本
- 移除未使用的 CSS

## 快速優化步驟

### 步驟 1：壓縮 Hero 圖片
1. 前往 https://tinypng.com/
2. 上傳 `images/hero/hero_area.png`
3. 下載壓縮後的版本
4. 替換原檔案

### 步驟 2：壓縮 Icon
1. 使用 ImageOptim 或 TinyPNG
2. 將 `images/icon.png` 壓縮到 < 50KB
3. 替換原檔案

### 步驟 3：壓縮截圖
1. 批量壓縮所有截圖
2. 目標：每個 < 150KB

## 預期效果

優化後：
- 首屏載入時間：從 5-10 秒 → 1-2 秒
- 總頁面大小：從 ~6MB → ~1MB
- 用戶體驗：大幅提升

## 工具推薦

1. **TinyPNG** - https://tinypng.com/
   - 免費，線上壓縮
   - 支援 PNG 和 JPG

2. **Squoosh** - https://squoosh.app/
   - Google 開發
   - 可調整壓縮品質
   - 支援多種格式

3. **ImageOptim** - https://imageoptim.com/
   - Mac 應用程式
   - 批量處理
   - 免費

