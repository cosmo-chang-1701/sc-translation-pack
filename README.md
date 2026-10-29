# 🚀《星際公民》台灣繁體中文化語言包 (Star Citizen Traditional Chinese Pack)

![Latest Release](https://img.shields.io/github/v/release/cosmo-chang-1701/sc-translation-pack?color=blue&label=Latest%20Version)
![License](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)
![Languages](https://img.shields.io/badge/Languages-ZH--TW-orange)

本專案是一個由 AI 驅動（LLM Powered）的《星際公民》(Star Citizen) 台灣繁體中文化語言套件與發布平台，致力於為繁體中文玩家提供最即時、高品質的遊戲內容翻譯。透過大型語言模型進行上下文理解與自動化管線編譯，緊跟官方版本快速產出原生相容的繁體中文語言檔案，讓玩家都能無障礙地體驗寰宇生活。

---

## 🌐 支援語系 (Supported Languages)

目前專案提供以下語系支援，並持續更新中：
- **繁體中文 (Traditional Chinese)** - `chinese_(traditional)`
- **(More languages in progress...)**

---

## 🚀 特色 (Features)
- **即時更新**：緊跟遊戲版本更新，第一時間產出新內容翻譯。
- **AI 優化**：利用 LLM 進行語境理解，提供比傳統機械翻譯更自然的語句。
- **純淨無毒**：僅包含純文字翻譯檔，不修改遊戲核心執行程式。

---

## 📥 安裝說明

### 方式一：手動安裝 (推薦一般玩家)
1. 前往 [Releases](https://github.com/cosmo-chang-1701/sc-translation-pack/releases) 頁面下載最新版本的語系壓縮包（`.zip` 檔案）。
2. 解壓縮檔案，將 `chinese_(traditional)` 資料夾放入遊戲的語系目錄（若無 `Localization` 資料夾請手動建立）：
   `Program Files\Roberts Space Industries\StarCitizen\LIVE\data\Localization\`
   *(請確認完整路徑為：`.../data/Localization/chinese_(traditional)/global.ini`)*
3. 新增或修改 `Program Files\Roberts Space Industries\StarCitizen\LIVE\user.cfg` 以載入語系檔（以繁體中文為例）：
```ini
g_language = chinese_(traditional)
```

### 方式二：Git 同步 (推薦進階玩家)
如果您熟悉 Git，可以直接 Clone 本專案至 `Program Files\Roberts Space Industries\StarCitizen\LIVE\data\Localization\` 目錄下，未來僅需執行 `git pull` 即可快速完成增量更新。

---

## ❓ 常見問題 (FAQ)

<details>
<summary><b>Q1: 使用此中文化會被官方判定作弊或封鎖 (Ban) 嗎？</b></summary>

不會。本專案僅使用 CIG 官方預留的原生語系機制（透過 `data/Localization/` 目錄與 `user.cfg` 中的 `g_language` 參數指定），完全沒有修改遊戲核心執行程式（`.exe`）、記憶體或資料包（`data.p4k`），亦不會干擾 Easy Anti-Cheat (EAC) 反作弊系統，請安心使用。

</details>

<details>
<summary><b>Q2: 安裝後進入遊戲仍然是英文，該如何排除？</b></summary>

請依照下列步驟依序檢查：
1. **路徑結構是否正確**：確認翻譯檔案位置為 `StarCitizen\LIVE\data\Localization\chinese_(traditional)\global.ini`（請注意大小寫與資料夾階層，切勿多包一層資料夾）。
2. **user.cfg 設定與副檔名**：請確認 `user.cfg` 放置於 `StarCitizen\LIVE\` 根目錄，且檔案副檔名確實為 `.cfg`（避免 Windows 預設隱藏已知副檔名而誤存為 `user.cfg.txt`）。
3. **設定檔內容**：確認 `user.cfg` 內包含 `g_language = chinese_(traditional)` 且無贅字或拼寫錯誤。
4. **檔案編碼**：若手動編輯 `user.cfg`，建議以 UTF-8 或 ANSI 編碼儲存。

</details>

<details>
<summary><b>Q3: 遊戲版本更新後，翻譯失效了怎麼辦？</b></summary>

每次遊戲發佈版本更新（例如 3.24.x 或季更新）時：
1. 官方更新程式可能覆蓋或移除 `user.cfg`，請先至遊戲目錄確認並重新設定 `g_language = chinese_(traditional)`。
2. 遊戲版本更新後往往伴隨新文字或鍵值異動，舊版語系可能出現部分缺漏。請至本專案的 [Releases](https://github.com/cosmo-chang-1701/sc-translation-pack/releases) 下載對應最新遊戲版本的語系包，或使用 Git 執行 `git pull` 進行同步更新。

</details>

<details>
<summary><b>Q4: 為什麼部分太空站、介面或終端機仍顯示英文？</b></summary>

《星際公民》部分介面（如建築內部看板、特定 ASOP 終端機或早期 Building Blocks UI）之文本為寫死（Hardcoded）在底層資產或由伺服器動態下發，尚未串接 CIG 的客戶端在地化字典檔中。此為遊戲引擎現階段架構限制，需待官方後續更新逐步開放本地化支援。

</details>

<details>
<summary><b>Q5: 如何暫時或切換回官方預設英文？</b></summary>

若您需要暫時切換回英文（例如回報官方 Issue Council 錯誤或參與英文社群活動）：
- **方法一（暫時停用）**：使用文字編輯器開啟 `user.cfg`，在該行前方加上分號或井號註解（例如 `;g_language = chinese_(traditional)`），或直接將該行暫時刪除。
- **方法二（指定英文）**：將 `user.cfg` 內容修改為：
  ```ini
  g_language = english
  ```
存檔後重新啟動遊戲即可恢復官方預設英文介面。

</details>

<details>
<summary><b>Q6: 發現翻譯錯誤、錯別字或有翻譯建議，該如何回報？</b></summary>

非常歡迎社群共同協作完善在地化品質！您可以：
1. 截圖記錄問題發生位置（包含英文原文或目前中文字幕）。
2. 至專案的 [GitHub Issues](https://github.com/cosmo-chang-1701/sc-translation-pack/issues) 提交回報，請詳細說明「目前翻譯」、「建議翻譯」及「所在場景/任務/物品名稱」。
3. 亦可加入 [Star Netrunners](https://discord.gg/2H8X3dq83n) Discord 頻道與社群翻譯成員即時交流討論。

</details>

---

## ⚠️ 免責聲明 (Disclaimer)
1. **官方關聯**：本專案為非官方粉絲自製內容，與 Cloud Imperium Games (CIG) 無官方關聯。所有遊戲內資源與商標版權均歸原公司所有。
2. **翻譯準確性**：翻譯內容由 AI 生成並經過初步校對，但不保證 100% 準確，僅供遊戲參考。

---

## 📜 授權條款 (License)

本專案之翻譯文本採用 **[創用 CC 姓名標示-非商業性-相同方式分享 4.0 國際授權條款](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.zh_TW)** 進行授權。

![CC BY-NC-SA](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/by-nc-sa.svg)

- **姓名標示**：您必須指名原作者（Cosmo Chang）。
- **非商業性**：您不得將本翻譯內容用於商業目的。
- **相同方式分享**：如果您更動、轉換本作品，必須採用與原作品相同或類似的授權條款。

---
*願你在繁星之間飛行愉快。 See you in the verse!*