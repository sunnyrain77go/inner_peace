# 靜心 · 養心 — Inner Peace App

> 一個靜態心靈雞湯網頁應用，選擇你此刻的情緒，獲得來自經典智慧的回應與正念引導。

![Static HTML](https://img.shields.io/badge/Static-HTML%20Only-c8a96e?style=flat-square)
![No Build](https://img.shields.io/badge/Build-None%20Required-4a9e6b?style=flat-square)
![GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-1a1208?style=flat-square)

---

## ✨ 功能特色

- **10 種情緒狀態選擇** — 從焦慮、低落到感恩，涵蓋日常各種心情
- **經典智慧回應** — 引用《金剛經》《了凡四訓》《道德經》及蘇軾、王陽明、曾國藩等名言
- **具體行動建議** — 每種情緒附上 4 個立刻可做的小事
- **引導冥想練習** — 視覺化呼吸圈（4 秒吸氣 · 2 秒停留 · 6 秒呼氣），每次 3 組循環
- **零依賴** — 純 HTML / CSS / JS，無任何框架或套件，無需 build

---

## 🚀 部署到 GitHub Pages（5 分鐘上線）

### 方法一：直接上傳（最簡單）

1. 在 GitHub 建立新 repository（例如命名 `inner-peace`）
2. 點 **Add file → Upload files**
3. 把 `index.html` 拖進去，Commit changes
4. 進入 **Settings → Pages**
5. Source 選 `Deploy from a branch`，Branch 選 `main`，資料夾選 `/ (root)`
6. 儲存後等約 1 分鐘，網址會顯示在頁面上

```
https://<your-username>.github.io/<repo-name>/
```

### 方法二：使用 Git CLI

```bash
git init
git add index.html
git commit -m "init: add inner peace app"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

然後在 GitHub repo 的 **Settings → Pages** 開啟即可。

---

## 📁 檔案結構

```
/
└── index.html    ← 全部功能都在這一個檔案裡
└── README.md
```

這個專案刻意保持單一檔案，方便維護與部署。

---

## 💬 情緒對應內容一覽

| 情緒 | 引用來源 | 冥想類型 |
|------|----------|----------|
| 🌊 焦慮不安 | 《維摩詰經》 | 放下練習 |
| 🌀 心思混亂 | 《金剛經》 | 錨定練習 |
| 🌫 迷失方向 | 《了凡四訓》 | 內在聆聽 |
| 🍂 身心俱疲 | 曾國藩《家書》 | 身體掃描 |
| 🌧 低落悲傷 | 范仲淹《岳陽樓記》 | 慈心冥想 |
| 🔥 憤怒委屈 | 蘇軾《定風波》 | 釋放練習 |
| 🕯 孤單寂寞 | 王陽明 | 連結冥想 |
| 🌸 感恩平靜 | 老子《道德經》 | 感恩擴展 |
| ⛰ 卡關停滯 | 老子《道德經》 | 山的對話 |
| ☀️ 想要改變 | 劉備·告誡劉禪 | 未來自我 |

---

## 🎨 設計理念

- **字體**：Ma Shan Zheng（毛筆感標題）+ Noto Serif TC（正文）
- **色調**：宣紙米白 + 墨色 + 金棕，模擬古籍質感
- **動態**：卡片滑入、呼吸圓擴縮、冥想覆蓋層淡入
- **行動建議**：融入感恩日常（有飯吃、有屋住）、財富思維與自我提升等正向引導

---

## 🛠 客製化

想新增情緒或修改內容，只需編輯 `index.html` 中的 `emotions` 物件：

```javascript
const emotions = {
  your_key: {
    tag: '🌟 你的情緒標籤',
    main: `回應的主要文字，支援 <strong> 等 HTML 標籤`,
    quote: '引用的名言',
    source: '出處',
    actions: [
      '行動建議 1',
      '行動建議 2',
      '行動建議 3',
      '行動建議 4'
    ],
    meditation: '冥想引導詞'
  }
};
```

同時在 HTML 的 `.emotion-grid` 區塊加上對應按鈕即可：

```html
<button class="emotion-btn" data-emotion="your_key" onclick="selectEmotion(this)">
  <span class="icon">🌟</span> 你的情緒標籤
</button>
```

---

## 📜 引用來源

- 《金剛經》· 鳩摩羅什譯
- 《了凡四訓》· 袁黃（了凡）著
- 《道德經》· 老子著
- 《岳陽樓記》· 范仲淹
- 《定風波》· 蘇軾
- 《傳習錄》· 王陽明
- 曾國藩《家書》
- 劉備 · 白帝城遺言
- 《維摩詰經》

---

*願你此刻安好 · 一切都會過去 · 一切都是恩典*
