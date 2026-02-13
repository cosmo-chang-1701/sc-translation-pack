# 星際公民多國語系在地化專案 (Star Citizen Multi-language Localization Project)

![Latest Release](https://img.shields.io/github/v/release/cosmo-chang-1701/sc-translation-pack?color=blue&label=Latest%20Version)
![License](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)
![Languages](https://img.shields.io/badge/Languages-ZH--TW-orange)

本專案是一個由 AI 驅動（LLM Powered）的多國語系在地化發佈平台，致力於為《星際公民》(Star Citizen) 玩家提供最即時、高品質的遊戲內容翻譯。透過大型語言模型進行上下文理解，我們能快速將遊戲更新內容轉化為多國在地化語言檔案，讓全球玩家都能無障礙地體驗寰宇生活。

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
1. 請前往 [Releases](https://github.com/cosmo-chang-1701/sc-translation-pack/releases) 頁面下載最新版本的語系壓縮包（例如 `sc-localization-zh-TW-v4.6.0-v1.zip`）。
2. 將檔案解壓縮至您的遊戲安裝目錄。請確保 `global.ini` 位於正確的資料夾層級：
`Program Files\Roberts Space Industries\StarCitizen\LIVE\data\Localization\`
3. 修改 `user.cfg` 以載入語系檔 (以繁體中文為例)
```
g_language = chinese_(traditional)
```

### 方式二：Git 同步 (推薦進階玩家)
如果您熟悉 Git，可以直接 Clone 本專案至遊戲目錄，未來僅需執行 `git pull` 即可快速完成增量更新。

---

## 🐛 已知問題 (Known Issues)
- **Grim HEX 終端機顯示原文**：目前在六角灣 (Grim HEX) 的 Dumper's Depot 商店中，購買載具組件的終端機介面尚未套用翻譯，因此仍會顯示英文原文。

---

## ⚠️ 免責聲明 (Disclaimer)
1. **官方關聯**：本專案為非官方粉絲自製內容，與 Cloud Imperium Games (CIG) 無官方關聯。所有遊戲內資源與商標版權均歸原公司所有。
2. **翻譯準確性**：翻譯內容由 AI 生成並經過初步校對，但不保證 100% 準確，僅供遊戲參考。

---

## 📜 授權條款 (License)

本專案之翻譯文本採用 **[創用 CC 姓名標示-非商業性-相同方式分享 4.0 國際授權條款](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.zh_TW)** 進行授權。

![CC BY-NC-SA](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/by-nc-sa.svg)

- **姓名標示**：您必須指名原作者（[你的名字或代號]）。
- **非商業性**：您不得將本翻譯內容用於商業目的。
- **相同方式分享**：如果您更動、轉換本作品，必須採用與原作品相同或類似的授權條款。

---

## 🛠️ 開發與回報
本專案的翻譯引擎由 [star-citizen-trans-engine](https://github.com/cosmo-chang-1701/star-citizen-trans-engine) 驅動。
如果您發現任何翻譯錯誤、語句不通順或顯示問題，歡迎透過以下方式回報：
- 開啟 GitHub [Issues](https://github.com/cosmo-chang-1701/sc-translation-pack/issues)
- 加入 [Star Netrunners](https://discord.gg/2H8X3dq83n) Discord

---
*願你在繁星之間飛行愉快。 See you in the verse!*