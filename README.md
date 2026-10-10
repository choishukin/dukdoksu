# 讀數獨數

香港中學數學教學網站（靜態站，適合 GitHub Pages）。

- **顯示名稱**：讀數獨數  
- **資料夾／建議 repo 名稱**：`dukdoksu`  
- **託管**：GitHub Pages（由 repo **根目錄** 提供靜態檔，無需 build）

## 網站結構

```
dukdoksu/
├── index.html              # 首頁
├── css/style.css
├── teaching/               # 教學內容（分級別 → 課題）
│   ├── index.html
│   └── f2/
│       ├── index.html      # 中二
│       └── exterior-angle/ # 三角形外角
│           ├── index.html
│           ├── notes.pdf
│           ├── demo.html       # 互動示範（自含 KaTeX，可離線）
│           └── problems.html   # 題目逐步示範（自含 KaTeX，可離線）
└── exam/                   # 公開試專區（DSE 必修＋延伸）
    ├── index.html
    ├── compulsory/
    ├── extended/
    └── sample/             # BY TOPIC 介面示例
```

## 本機預覽

無需安裝依賴。任選其一：

```bash
# 進入專案根目錄後
cd dukdoksu
python3 -m http.server 8080
# 瀏覽器開啟 http://localhost:8080/
```

或直接用瀏覽器開啟 `index.html`（部分瀏覽器對本地 `file://` 的 PDF／相對路徑較嚴，建議用本機 HTTP server）。

互動示範 `demo.html`／`problems.html` 已內嵌 KaTeX 字型，**離線亦可開啟**。首頁與課題頁的公式示例使用 jsDelivr CDN 的 KaTeX，需網絡。

## GitHub Pages

1. 建立 repo（建議名稱：`dukdoksu`）。
2. 將本目錄內容推到 `main`（或 `gh-pages`）的**根目錄**。
3. 在 repo Settings → Pages → Source 選該分支、資料夾 `/`（root）。
4. 網站網址約為：`https://<user>.github.io/dukdoksu/`  
   （若 repo 名與 user 名相同的特殊 pages repo，則為 `https://<user>.github.io/`。）

相對連結已按「站點根＝repo 根」編寫；若日後改用 `/docs` 發佈，請把整個站放入 `docs/` 並維持內部相對路徑不變。

## 第一批內容

- **中二 · 三角形外角**：筆記 PDF、撕紙拼角互動示範、題目逐步示範。

## 授權與用途

教學用途。KaTeX（示範內嵌／CDN）為 MIT 授權。
