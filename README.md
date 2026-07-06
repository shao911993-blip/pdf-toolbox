# 📄 PDF 小工具箱

一個單檔、純前端的 PDF 工具箱。所有檔案處理都在瀏覽器本機完成，**檔案不會上傳到任何伺服器**。

**線上使用：https://shao911993-blip.github.io/pdf-toolbox/**

## 功能

| 功能 | 說明 |
|---|---|
| 📑 PDF 合併 | 多檔上傳、拖曳排序、合併下載 |
| ✂️ 刪頁／拆分 | 縮圖點選或輸入頁碼（如 `1,3,5-8`），匯出指定頁面 |
| 🖼️ PDF 轉圖片 | PNG／JPG／WebP，96–300 DPI，可逐張或 ZIP 打包下載 |
| 📷 圖片轉 PDF | JPG／PNG／HEIC，A4 或原始尺寸，自動置中縮放 |
| 🗜️ PDF 壓縮 | 深度壓縮（保留文字）或轉圖壓縮（相容模式），顯示前後大小對比 |

其他特色：頁面縮圖預覽、全頁放大檢視器、輸出檔案大小預估、雙渲染引擎自動降級（pdf.js 失敗的頁面自動改用 Ghostscript 重跑）。

## 使用方式

不需要安裝、不需要建置。下載 `index.html` 用瀏覽器開啟即可，或直接使用上方的線上網址。第一次開啟需要網路載入 CDN 套件；深度壓縮功能第一次使用需下載約 16 MB 的引擎（之後由瀏覽器快取）。

## 隱私

所有 PDF 與圖片的讀取、轉換、壓縮都透過 WebAssembly 與 Canvas 在你的裝置上執行，任何檔案內容都不會離開你的瀏覽器。

## 授權

本專案採用 [GNU Affero General Public License v3.0（AGPL-3.0）](LICENSE) 授權。

因為本專案使用了 Ghostscript／ghostscript-wasm，而其授權為 AGPL-3.0，為避免授權標示不一致，整個專案以 AGPL-3.0 釋出，完整原始碼公開於本 repository。

如果要把包含 Ghostscript 的版本用於閉源或商業產品，應另行確認 [Artifex 的商業授權](https://artifex.com/licensing/)。

### 第三方元件

本工具執行時會從 CDN 載入下列第三方元件，各有其授權條款：

| 元件 | 用途 | 授權 |
|---|---|---|
| [pdf-lib](https://pdf-lib.js.org/) | PDF 合併／拆分／產生 | MIT |
| [pdf.js](https://mozilla.github.io/pdf.js/) | PDF 渲染 | Apache-2.0 |
| [JSZip](https://stuk.github.io/jszip/) | ZIP 打包 | MIT |
| [heic2any](https://github.com/alexcorvi/heic2any) | HEIC 圖片轉換 | MIT |
| [Ghostscript（WASM）](https://github.com/jsscheller/ghostscript-wasm) | 深度壓縮／高保真渲染 | **AGPL-3.0** |

⚠️ **商業使用注意**：AGPL-3.0 不禁止商業使用，但要求遵守開源義務。若要將包含 Ghostscript 的版本用於閉源產品，或無法遵守 AGPL-3.0 開源義務的商業情境，請向 [Artifex](https://artifex.com/licensing/) 確認 Ghostscript 商業授權。
