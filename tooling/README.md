# 工具與引擎（Tooling）

VN 開發相關的工具、引擎、框架整理。本目錄涵蓋從創作到發行的各種工具選項。

---

## 這裡收錄什麼

- 遊戲引擎
- VN 專用框架
- 美術工具與素材資源
- 音效 / 音樂工具與資源
- 劇本寫作與分支管理
- 版本控制與協作
- 發行與打包工具

---

## 遊戲引擎

### Ren'Py

**詳見：[renpy-ecosystem.md](./renpy-ecosystem.md)**

- 開源、免費（MIT 授權）
- Python-based 腳本，學習曲線平緩
- 獨立 VN 開發的事實標準
- 跨平台：Windows / macOS / Linux / Android / iOS / Web
- 官網：https://www.renpy.org/
- GitHub：https://github.com/renpy/renpy

### TyranoBuilder / TyranoScript

- **TyranoBuilder**：視覺化拖放編輯器（付費，Steam 販售）
- **TyranoScript**：底層腳本引擎（免費）
- 日本開發，介面風格接近傳統 VN 工具
- 較少需要寫程式碼
- 英語社群較 Ren'Py 小
- 官網：https://tyranobuilder.com/
- TyranoScript 文件：https://tyrano.jp/

### Visual Novel Maker (Degica)

- RPG Maker 開發商推出
- 視覺化編輯器
- Steam 整合佳
- 社群規模較小，更新頻率低
- 長期支援狀況不明
- Steam：搜尋 "Visual Novel Maker"

### Unity + VN 框架

**詳見：[unity-vn-ecosystem.md](./unity-vn-ecosystem.md)**

**Naninovel**
- 商業級 VN 框架（付費，$158+）
- 功能完整：劇本語言、角色系統、存檔、本地化
- 可與 Unity 其他功能整合（3D、小遊戲）
- 適合需要混合類型的專案
- 官網：https://naninovel.com/
- Asset Store：搜尋 "Naninovel"

**Fungus**
- 免費開源
- 視覺化流程圖編輯
- 功能較 Naninovel 簡單
- 適合快速原型或簡單專案
- GitHub：https://github.com/snozbot/fungus

**Ink + Unity**
- Inkle 開發的敘事腳本語言
- 專注於分支對話，不含視覺系統
- 需要自行處理 UI 與演出
- 官網：https://www.inklestudios.com/ink/

### Godot + 插件

**詳見：[godot-ecosystem.md](./godot-ecosystem.md)**

- 開源、免費的完整遊戲引擎
- VN 專用插件生態發展中：
  - **Dialogic**：主流 VN 對話插件（https://github.com/dialogic-godot/dialogic）
  - **Rakugo**：較完整的 VN 框架
  - **Dialogue Manager**：腳本式對話系統
- 需要更多設定，但引擎本身功能強大
- 適合需要混合玩法的專案
- 官網：https://godotengine.org/

### RPG Maker（VN 模式）

- 內建簡單對話系統
- 有 VN-style 插件可用
- 如果需要結合 RPG 元素可考慮
- 純 VN 不推薦（過度複雜）

### 其他 / 小眾

- **Monogatari**：Web-based VN 引擎（https://monogatari.io/）
- **KiriKiri / 吉里吉里**：日本傳統引擎，中文圈有使用
- **NScripter**：老牌日本引擎，已較少使用
- **Belle**：Electron-based，較新但社群小
- **Twine**：超文本故事工具，可視為 VN 前身，適合規劃用

---

## 美術工具

### 繪圖軟體

| 軟體 | 價格 | 平台 | 備註 |
|------|------|------|------|
| Clip Studio Paint | $50+ 買斷 / 訂閱 | Win/Mac/iPad | 漫畫插畫首選，立繪製作常用 |
| Photoshop | 訂閱制 | Win/Mac/iPad | 業界標準，功能全面 |
| Procreate | $13 買斷 | iPad only | iPad 繪圖首選 |
| Krita | 免費開源 | Win/Mac/Linux | 功能完整的免費選項 |
| SAI / SAI2 | ~$50 | Windows | 輕量、適合線稿與上色 |
| MediBang Paint | 免費 | 跨平台 | 雲端協作功能 |
| FireAlpaca | 免費 | Win/Mac | 輕量簡單 |

### 立繪管理工具

- **Live2D Cubism**：讓立繪有呼吸、眨眼等動態
  - Editor：免費版可用，Pro 版訂閱
  - SDK：商業使用需授權
  - https://www.live2d.com/
- **Spine**：2D 骨骼動畫，較少用於 VN 但可行
- **差分管理**：通常用 Photoshop 圖層 + 命名規範處理

### AI 輔助工具（現況與爭議）

- **Stable Diffusion / Midjourney / NovelAI**：可生成背景、概念圖
- **使用限制**：
  - 商業發行需注意平台政策（Steam 已有審核）
  - 部分社群對 AI 素材反感
  - 揭露要求因地區與平台而異
- **常見用法**：
  - 背景生成 + 後製修飾
  - 概念設計與參考
  - 占位素材（開發中使用）
- **不建議**：直接使用 AI 角色立繪作為最終素材（風格一致性問題）

---

## 免費素材資源

### 角色立繪

- **Lemma Soft Forums - Resources**
  - https://lemmasoft.renai.us/forums/viewforum.php?f=52
  - 大量社群製作的免費立繪
  - 授權條件不一，需逐項確認
- **itch.io**
  - 搜尋 "visual novel sprites" / "character assets"
  - 有免費與付費選項
  - 授權通常清楚標示
- **OpenGameArt**
  - https://opengameart.org/
  - CC 授權為主
  - VN 專用較少，但可找到通用素材

### 背景圖

- **Noraneko Games**
  - https://noranekogames.itch.io/
  - 免費與付費 VN 背景
  - 風格統一，品質佳
- **Uncle Mugen**
  - Lemma Soft 知名背景製作者
  - 照片改繪風格
- **itch.io 背景包**
  - 搜尋 "visual novel backgrounds"
  - 價格從免費到數十美元不等
- **Unsplash / Pexels**
  - 免費照片
  - 需要後製才能融入 VN 風格

### UI / GUI 模板

- **Lemma Soft GUI 區**
  - 各種風格的 UI 主題
  - Ren'Py 專用為主
- **itch.io UI packs**
  - 搜尋 "visual novel UI" / "GUI"

---

## 音效與音樂

### 音樂製作軟體

| 軟體 | 價格 | 備註 |
|------|------|------|
| FL Studio | $99+ | 電子音樂常用 |
| Ableton Live | $99+ | 專業 DAW |
| Logic Pro | $200 | macOS 專用 |
| Reaper | $60 | 便宜但功能完整 |
| LMMS | 免費 | 開源 DAW |
| GarageBand | 免費 | macOS/iOS，入門適用 |

### 免費音樂資源

- **Incompetech (Kevin MacLeod)**
  - https://incompetech.com/
  - 大量免費音樂，需署名
- **FreePD**
  - https://freepd.com/
  - 公共領域音樂
- **dova-syndrome**
  - https://dova-s.jp/
  - 日本免費音樂庫
  - 使用條款需確認
- **魔王魂**
  - https://maou.audio/
  - 日本免費素材站
  - VN / RPG 風格音樂多
- **甘茶の音楽工房**
  - https://amachamusic.chagasi.com/
  - 日本免費音樂
- **MusMus**
  - https://musmus.main.jp/
  - 免費，商用需署名

### 音效資源

- **Freesound**
  - https://freesound.org/
  - 社群上傳的音效
  - 授權各異，需確認
- **Zapsplat**
  - https://www.zapsplat.com/
  - 免費帳號可用
- **効果音ラボ**
  - https://soundeffect-lab.info/
  - 日本免費音效
- **On-Jin ～音人～**
  - https://on-jin.com/
  - 日本音效素材

### 配音相關

- **Fiverr / 配音員募集**：小規模專案常見方式
- **CastingCall.Club**：英語配音員募集平台
- **VOCALOID / Synthesizer V**：合成歌聲（歌曲用）
- **VOICEVOX / COEIROINK**：日語 TTS，可用於原型或特定風格

---

## 劇本寫作工具

### 寫作軟體

| 軟體 | 價格 | 特點 |
|------|------|------|
| Scrivener | $49 | 長文管理、大綱、角色卡 |
| Obsidian | 免費 | Markdown、雙向連結、插件生態 |
| Notion | 免費/付費 | 協作、資料庫功能 |
| Google Docs | 免費 | 簡單協作 |
| VS Code | 免費 | 程式編輯器，搭配 Markdown |
| Final Draft | $250 | 劇本專用，VN 較少用 |

### 分支管理 / 流程圖

- **Twine**
  - https://twinery.org/
  - 互動小說引擎，但常用於規劃 VN 分支
  - 視覺化節點編輯
- **Miro / FigJam**
  - 線上白板工具
  - 適合團隊腦力激盪
- **draw.io (diagrams.net)**
  - 免費流程圖工具
- **Articy:draft**
  - https://www.articy.com/
  - 專業敘事設計工具（貴）
- **Yarn Spinner**
  - https://yarnspinner.dev/
  - 對話系統工具，有視覺化編輯器

---

## 版本控制與協作

### Git

- **GitHub / GitLab / Bitbucket**：程式碼與文字檔案管理
- **Git LFS**：大型檔案（圖片、音樂）需使用 LFS
- **注意事項**：
  - 圖片檔案頻繁修改會讓 repo 膨脹
  - 建議素材與程式碼分開管理或使用 LFS

### 其他協作工具

- **Notion / Trello / Asana**：專案管理
- **Discord / Slack**：團隊溝通
- **Google Drive / Dropbox**：大檔案同步（非版本控制）

---

## 發行工具

### 平台 SDK / 工具

- **Steamworks**：Steam 上架必備（https://partner.steamgames.com/）
- **itch.io butler**：itch.io 自動上傳工具（https://itch.io/docs/butler/）
- **GOG Galaxy SDK**：GOG 上架用

### 打包與建置

- Ren'Py：內建 Launcher 可打包各平台
- Unity：Player Settings → Build
- Godot：Export Templates

### 本地化工具

- **Ren'Py**：內建翻譯檔案提取（`renpy.po`）
- **POEdit**：編輯 `.po` 翻譯檔案（https://poedit.net/）
- **Crowdin / Weblate**：翻譯管理平台

---

## 相關連結

### 綜合資源

- [Lemma Soft Forums](https://lemmasoft.renai.us/forums/) - Ren'Py 社群與資源
- [itch.io Game Assets](https://itch.io/game-assets) - 獨立素材市場
- [r/visualnovels](https://www.reddit.com/r/visualnovels/) - Reddit 討論區
- [r/vndevs](https://www.reddit.com/r/vndevs/) - VN 開發者 Reddit

### 教學入口

- [Ren'Py Documentation](https://www.renpy.org/doc/html/)
- [Naninovel Guide](https://naninovel.com/guide/)
- [Zeil Learnings (YouTube)](https://www.youtube.com/@ZeilLearnings) - Ren'Py 教學
- [Visual Novel Design](https://visualnoveldesign.com/) - VN 設計資源

---

## 待研究問題

- 各引擎的詳細功能比較表
- 團隊規模與工具選擇的對應
- 中文 VN 開發常用的工具組合
- Live2D 整合的成本效益分析

---

## 相關目錄

| 目錄 | 關聯 |
|------|------|
| [monetization/](../monetization/) | 發行平台與上架工具 |
| [localization/](../localization/) | 本地化工具與翻譯流程 |
| [industry-ecology/](../industry-ecology/) | 開發團隊規模與工具選擇 |
| [failure-modes/](../failure-modes/) | 技術問題與工具限制 |
| [emerging-frontiers/](../emerging-frontiers/) | AI 工具與新興技術 |

---

*狀態：初步填充，持續累積中*
