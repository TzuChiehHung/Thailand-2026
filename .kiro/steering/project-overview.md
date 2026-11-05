---
inclusion: always
---

# 專案總覽與資料分流準則（2026 泰國天燈節專案）

本文件為全域基礎認知，適用於所有開發情境。撰寫或修改任何檔案前，請先理解專案架構與資料分流原則。

## 專案背景

- 這是一個 **2026 泰國天燈節 9 天 8 夜旅遊行程網站**，純靜態前端。
- 技術棧：HTML + Tailwind CSS（CDN）+ FontAwesome + 原生 JavaScript，無建置流程。
- `index.html` 為外層殼層，透過 `assets/js/app.js` 以 `fetch` 動態載入各模組。
- 以 `localStorage` 記住使用者狀態（目前天數、交通摺疊開關、費用展開狀態）。

## 檔案結構

- `index.html`：殼層、Hero、主頁籤導覽、動態載入容器。
- `assets/js/app.js`：頁籤／天數切換、模組 fetch 與快取、交通摺疊、私人備忘入口。
- `assets/css/theme.css`：全站共用主題樣式與工具類別（配色、時間軸、備註盒、地圖連結、Highlight）。
- `src/views/`：分頁視圖 —— 總覽 `overview.html`、行程 `itinerary.html`、費用 `costs.html`、私人備忘 `private.html`。
- `src/itinerary/`：每日行程模組 `day_1.html` ~ `day_9.html`。

## 開發通則

- 優先使用 `theme.css` 既有工具類別，避免 ad-hoc 內聯樣式。
- 內容以繁體中文為主。

## 資訊主權與分流（Data Governance）

- **行程頁面（`src/itinerary/`）**：專注於「時序」與「體驗」。
  - ❌ 禁止：標註住宿價格、早餐含否、交通明細費用。
  - ✅ 允許：轉機美食推薦、防宰指南、通關應變。
- **費用頁面（`src/views/costs.html`）**：統一管理「預算」與「房型細節」。
  - 所有報價、均分邏輯、含餐狀況與 VILLA 規格均定義於此。

---

*本準則由 senior 規劃師（Antigravity）維護，請嚴格遵守以確保網頁品質一致。*
