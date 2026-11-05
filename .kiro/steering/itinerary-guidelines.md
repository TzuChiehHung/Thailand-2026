---
inclusion: fileMatch
fileMatchPattern: 'src/itinerary/**'
---

# 每日行程撰寫準則

本文件適用於 `src/itinerary/` 下的每日行程模組（`day_1.html` ~ `day_9.html`）。

## 1. 標籤化與動態分支系統（Tag & Branch System）

### 色系規範

- 主線行程（Amber）：色系變數為琥珀金。
- 特色／分流行程（Rose）：色系變數為玫瑰紅（分流標籤色彩）。

### 時間軸活動點（`timeline-item-xxx`）

- 活動點必須使用 `.timeline-item-amber`（主線）或 `.timeline-item-rose`（分流）。
- 每個節點內需放置 `.timeline-dot`，呈現「實線」與「彩色發光圓點」。
- 這類節點在「摺疊交通模式」下**不會被隱藏**，以確保旅程脈絡完整。

### 交通／中轉節點（`timeline-item-transfer`）

- 統一使用 `.timeline-item-transfer`，圓點使用 `.timeline-dot-transfer`。
- 視覺特徵為「灰色虛線」與「灰色無影點」。
- 由 `app.js` 的交通開關（`#transfer-toggle`）控制：開關開啟時，透過 `.hidden` 將這類節點完全摺疊。

## 2. 重要資訊備註盒（Note-Box System）

- **結構標準**：必須為 `Icon + 標題：內容` 格式，以 `.note-box` 容器包裹一個 `<i>` 圖示與一個內容 `<div>`。
- **分流配色**：若備註屬於分流內容，使用既有修飾類別 `.note-box-rose` 或 `.note-box-emerald`，不可自行內聯指定背景色。
- **圖示規範（Semantic Icons）**：
  - 不再強制統一為驚嘆號，應選用與內容情境相關的圖示。
  - 範例：門票相關（`fa-ticket`）、服裝規定（`fa-shirt`）、預訂提醒（`fa-calendar-check`）、嚴格禁止（`fa-camera-slash` / `fa-phone-slash`）。

## 3. Google Maps 地圖聯動

- **連結格式**：統一使用搜尋 API：
  `https://www.google.com/maps/search/?api=1&query=地點名稱+城市`
- **圖示規範**：`fa-location-dot` 連結置於地點名稱右側。若名稱後方已有連結圖示，名稱內禁止出現 Emoji。
- **色彩統一**：超連結（`<a>`）樣式須跟隨該項目主題色，優先使用 `theme.css` 既有工具類別：
  - 主線行程：`map-link-amber`（等同 `text-amber-500 hover:text-amber-700 transition-colors`）。
  - 分流行程：`map-link-rose`。

---

*本準則由 senior 規劃師（Antigravity）維護，請嚴格遵守以確保網頁品質一致。*
