# 🎱 六合彩號碼產生器 (Mark Six Random Generator)

一個簡單、純前端的網頁應用程式，用於隨機生成香港六合彩 (Mark Six) 風格的號碼組合。本項目僅作 **網頁編程練習** 及 **娛樂用途**。

🌟 **即刻試玩 (Live Demo)：** [https://erictamhk.github.io/marksix-random-gen/](https://erictamhk.github.io/marksix-random-gen/)

## ⚠️ 免責聲明 (Disclaimer) - 重要！

在使用本程式前，請務必閱讀以下條款：

1.  **非官方應用**：本程式與 **香港賽馬會 (HKJC)** 無任何關係。
2.  **僅供娛樂**：本程式生成的號碼純屬隨機（Random），**絕無任何預測功能**，亦無科學根據保證中獎。
3.  **非投注建議**：本程式不構成任何賭博或投資建議。請勿依賴本程式進行真實金錢投注。
4.  **責任豁免**：作者不對因使用本程式而導致的任何損失（包括金錢損失）承擔法律責任。賭博有風險，請量力而為。
5.  **版權說明**：「六合彩」及相關波色規則參照公開資訊，相關商標歸香港賽馬會所有。

---

## 🚀 點樣用 (How to Use)

最快嘅方法，無需下載任何嘢，直接點擊以下連結即開即用：
👉 **[按此打開網頁版](https://erictamhk.github.io/marksix-random-gen/)**

如果你想下載源代碼自己研究或修改（無需安裝任何伺服器或依賴庫）：

1.  **下載代碼**：
    使用 Git Clone 這個 repo：
    ```bash
    git clone git@github.com:erictamhk/marksix-random-gen.git
    ```
2.  **開啟網頁**：
    在下載的文件夾內找到 `index.html`，雙擊用任何瀏覽器（Chrome, Safari, Edge 等）打開。
3.  **產生號碼**：
    點擊畫面中間的 **「🎲 攪珠！」** 按鈕，程式便會模擬攪珠過程並顯示一組號碼。

## 🛠️ 原理 (How it Works)

本程式完全使用 **HTML, CSS, JavaScript** 製作，並採用了比一般網頁更強的隨機數生成技術：

*   **密碼學安全隨機數 (CSPRNG)**：揚棄了傳統易被預測的 `Math.random()`，改用瀏覽器內建的 Web Crypto API `window.crypto.getRandomValues()` 獲取環境熵值 (Entropy) 來產生高質量的隨機數。
*   **拒絕採樣 (Rejection Sampling)**：在轉換整數時採用了拒絕採樣演算法，徹底消除了「模偏差 (Modulo Bias)」，確保 1 至 49 每一個數字出現的機率完全平等。
*   **洗牌演算法**：配合 **Fisher-Yates Shuffle** 算法，將 1 至 49 的陣列徹底打亂，然後抽出前 6 個作為「主號碼」，第 7 個作為「特別號碼」，確保號碼不會重複。
*   **波色邏輯**：內置官方波色對照表，根據生成的數字自動配對紅、藍、綠波樣式。
*   **視覺效果**：使用 CSS 動畫 (`animation` & `transform`) 製作球體滾動、彈出效果及星空背景。

## 📝 檔案結構

*   `index.html`: 包含所有結構、樣式 (CSS) 和 邏輯 (JS) 的單一檔案，方便攜帶和分享。

---

*切記：小賭怡情，大賭傷身。沉迷賭博，倒錢落海。*
