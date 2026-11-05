---
inclusion: fileMatch
fileMatchPattern: 'assets/css/**|src/**/*.html'
---

# 視覺與配色準則

本文件適用於所有 HTML 頁面與 `assets/css/` 樣式。撰寫視覺呈現時請嚴格遵守，以維持全站視覺一致性。

## 配色限制

- 統一採用專案定義的**天燈琥珀金（Amber）**主題。
- 所有行程備註盒（`.note-box`）必須維持統一底色與邊框色。
- **禁止 ad-hoc 背景色**：不可為單一區塊臨時內聯指定 Rose（紅）或 Emerald（綠）等自訂背景。分流色系僅能透過既有修飾類別套用。

## `theme.css` 既有工具類別對照

請優先使用以下既定類別，避免重新發明樣式：

### 時間軸

- `.timeline-item-amber` / `.timeline-item-rose`：主線 / 分流活動點（實線、發光圓點，搭配 `.timeline-dot`）。
- `.timeline-item-transfer`：交通中轉（灰色虛線，搭配 `.timeline-dot-transfer`）。

### 備註盒

- `.note-box`：預設天燈金底色與邊框。
- `.note-box-rose` / `.note-box-emerald`：分流色系修飾類別。

### 地圖連結

- `.map-link-amber` / `.map-link-rose` / `.map-link-emerald`：含 hover 過渡的地圖連結樣式。

### 重點文字 Highlight

- `.text-highlight-amber`（主線）/ `.text-highlight-rose`（分流）/ `.text-highlight-emerald` / `.text-highlight-black`。

---

*本準則由 senior 規劃師（Antigravity）維護，請嚴格遵守以確保網頁品質一致。*
