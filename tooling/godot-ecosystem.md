# Godot VN 開發生態系統

Godot 作為開源遊戲引擎，近年在 VN 開發領域逐漸受到關注。本文整理 Godot 用於 VN 開發的生態系統狀況。

---

## Godot 引擎概述

### 基本資訊

- **官網：** https://godotengine.org/
- **授權：** MIT（完全開源免費）
- **當前版本：** 4.x 系列（2023+）
- **GitHub：** https://github.com/godotengine/godot

### 優勢

**開源免費：**
- 無授權費、無分潤
- 可修改引擎原始碼
- 社群驅動開發

**跨平台：**
- Windows / macOS / Linux
- Android / iOS
- Web (HTML5)
- 主機（透過官方或第三方）

**GDScript：**
- 類 Python 語法，易於學習
- 也支援 C# (Godot Mono)
- 視覺腳本（Godot 4 已移除內建，有插件）

**引擎輕量：**
- 下載約 40-80 MB
- 啟動快、資源佔用少
- 適合小型專案

### 劣勢（相對於 Ren'Py / Unity）

**VN 專用功能需自建或依賴插件：**
- 無內建對話系統
- 無內建存檔 / 讀檔 UI
- 需要更多前期設定

**社群規模較小：**
- VN 專用資源較 Ren'Py 少
- 遇到問題時參考較少

**Godot 4 過渡期：**
- 部分插件尚未更新到 Godot 4
- API 變動造成學習曲線

---

## VN 專用插件

### Dialogic（主流選擇）

**官網 / 文件：** https://dialogic.coppolaemilio.com/  
**GitHub：** https://github.com/dialogic-godot/dialogic  
**支援版本：** Godot 3.x（1.x 版）、Godot 4.x（2.x 版）

**功能概覽：**
- 視覺化對話編輯器
- 角色管理（表情、立繪）
- 分支對話與變數
- 文字特效（打字機效果、BBCode）
- 背景與音樂觸發
- 存檔系統整合

**設計特點：**
- 在 Godot 編輯器內操作
- 時間軸（Timeline）概念
- 主題系統（自訂對話框樣式）

**Dialogic 1.x vs 2.x：**

| 版本 | 引擎支援 | 狀態 |
|------|----------|------|
| 1.x | Godot 3.x | 穩定，不再更新 |
| 2.x | Godot 4.x | 活躍開發中 |

**注意：** Dialogic 2.x 是重寫版本，API 與 1.x 不相容。

**教學資源：**
- [Dialogic 官方文件](https://docs.dialogic.pro/)
- [YouTube: Dialogic 教學播放清單](https://www.youtube.com/results?search_query=dialogic+godot+tutorial)
- GitHub 的 examples 資料夾

---

### Rakugo（較完整框架）

**GitHub：** https://github.com/rakugoteam/Rakugo  
**支援版本：** Godot 3.x（部分 4.x 支援進行中）

**功能概覽：**
- 腳本語言（RakuScript）
- 角色與變數系統
- 存檔 / 讀檔
- 歷史回顧
- 跳過 / 自動播放

**特點：**
- 嘗試提供類似 Ren'Py 的完整解決方案
- 有自己的腳本語法
- 更新頻率較 Dialogic 低

**適合對象：**
- 想要更傳統 VN 框架的開發者
- 願意學習特定腳本語法

---

### Say（輕量對話插件）

**GitHub：** 搜尋 "godot say dialogue"  
**特點：**
- 更簡單的對話系統
- 適合只需要基本對話功能的專案
- 低學習曲線

---

### Dialogue Manager

**GitHub：** https://github.com/nathanhoad/godot_dialogue_manager  
**支援版本：** Godot 4.x

**特點：**
- 以文字檔案（`.dialogue`）為基礎
- 類似 Ink / Yarn 的腳本式對話
- 適合程式背景的開發者
- 非視覺化編輯

---

## 其他相關插件

### 存檔系統

| 插件 | 功能 | 連結 |
|------|------|------|
| GDSave | 簡單的存檔序列化 | GitHub 搜尋 |
| Game States | 狀態管理 | Godot Asset Library |

### UI / 美術

| 插件 | 功能 | 備註 |
|------|------|------|
| Theme Editor | 自訂 UI 主題 | 內建功能強化 |
| Aseprite Importer | 導入像素動畫 | 搭配 Aseprite 使用 |

### 音效 / 音樂

| 插件 | 功能 | 連結 |
|------|------|------|
| Music Manager | 音樂淡入淡出、播放清單 | GitHub 搜尋 |
| FMOD / Wwise 整合 | 專業音效中間件 | 需額外授權 |

---

## Godot 製作 VN 的工作流程

### 基本流程

1. **安裝 Godot**
   - 下載 Standard 或 Mono（C#）版本
   - Godot 4.x 建議新專案使用

2. **安裝對話插件**
   - Asset Library 或 GitHub 下載
   - 放入 `addons/` 資料夾
   - 在專案設定啟用插件

3. **設計場景結構**
   - 背景層
   - 角色層
   - 對話框層
   - UI 層

4. **編寫對話**
   - 使用 Dialogic 編輯器
   - 或直接寫 GDScript

5. **整合素材**
   - 導入立繪、背景
   - 設定音樂、音效

6. **測試與打包**
   - 使用 Export 功能
   - 各平台 Export Template

### 與 Ren'Py 的比較

| 面向 | Ren'Py | Godot + Dialogic |
|------|--------|------------------|
| 學習曲線 | VN 專用，快速上手 | 通用引擎，需設定 |
| 腳本語法 | 專用 Ren'Py 腳本 | GDScript 或視覺化 |
| 自訂程度 | 受限於框架 | 高度靈活 |
| 混合玩法 | 較困難 | 容易整合其他遊戲元素 |
| 社群資源 | VN 專用資源豐富 | VN 資源較少 |
| 文件完整度 | 完整 | Dialogic 文件持續改善中 |

---

## 使用 Godot 製作的 VN 案例

### 已發行作品

**商業 / 付費作品：**

- **Helios Rising**
  - itch.io / Steam 上架
  - 使用 Godot 3.x + Dialogic
  - BL 向視覺小說

- **Perfect Tides**
  - https://perfecttides.com/
  - 獨特的像素風格 VN
  - 使用 Godot 引擎
  - 獲得多項獨立遊戲獎項提名

- **Videoverse**
  - 復古社交媒體風格敘事
  - Godot 製作
  - 跨平台發行（Steam、Switch）

**免費 / Game Jam 作品（可參考學習）：**

搜尋入口（大量案例）：
- [itch.io: Godot + Visual Novel 標籤](https://itch.io/games/made-with-godot/tag-visual-novel)
- [Godot Jam 歷屆作品](https://itch.io/jam/godot-wild-jam)
- [Ludum Dare Godot VN 作品](https://ldjam.com/) — 搜尋 "godot visual novel"

**Game Jam 中的 Godot VN 趨勢：**
- Global Game Jam、Ludum Dare 常見 Godot + Dialogic 組合
- 因為快速原型製作能力強
- 許多 48-72 小時內完成的短篇 VN

### 開發中 / 實驗作品

- 許多 Game Jam 作品使用 Godot + Dialogic
- itch.io 上可找到 Godot 製作的免費 VN Demo
- [Godot Asset Library: Dialogue Systems](https://godotengine.org/asset-library/asset?filter=dialogue&category=&godot_version=&cost=&sort=updated) — 可找到更多專案範例

### 尋找案例的資源

| 平台 | 連結 | 備註 |
|------|------|------|
| itch.io | https://itch.io/games/made-with-godot/tag-visual-novel | 最大的獨立 VN 集散地 |
| Godot Showcase | https://godotengine.org/showcase/ | 官方展示，VN 類較少 |
| r/godot | https://www.reddit.com/r/godot/ | 搜尋 "visual novel" |
| Dialogic Discord | https://discord.gg/dialogic | 有作品展示頻道 |

---

## 優缺點總結

### 適合使用 Godot 的情況

✅ **想要混合其他遊戲元素：**
- VN + RPG
- VN + 解謎
- VN + 小遊戲

✅ **需要高度自訂：**
- 非傳統 VN 介面
- 特殊演出效果

✅ **偏好開源工具：**
- 不想依賴單一商業工具
- 想要可控的長期維護性

✅ **已熟悉 Godot：**
- 不想學新引擎
- 已有 Godot 專案經驗

### 不建議使用 Godot 的情況

❌ **純粹 VN、無其他玩法：**
- Ren'Py 更快速

❌ **需要大量現成資源：**
- Ren'Py / Unity 社群資源更多

❌ **團隊非技術背景：**
- 需要更多前期設定

❌ **趕時間的專案：**
- 從零建置比 Ren'Py 慢

---

## 學習資源

### 官方文件

- [Godot 官方文件](https://docs.godotengine.org/)
- [Godot 入門教學](https://docs.godotengine.org/en/stable/getting_started/introduction/index.html)

### Dialogic 專門

- [Dialogic 官方文件](https://docs.dialogic.pro/)
- YouTube 搜尋 "Dialogic 2 tutorial"
- [Dialogic Discord](https://discord.gg/dialogic)

### 社群

- [Godot 官方 Discord](https://discord.gg/godotengine)
- [r/godot](https://www.reddit.com/r/godot/) — Reddit 社群
- [Godot Forum](https://forum.godotengine.org/)

### YouTube 頻道

| 頻道 | 內容 |
|------|------|
| GDQuest | 通用 Godot 教學 |
| Bramwell Williams | 遊戲開發教學 |
| Emilio Coppola | Dialogic 作者 |

---

## 社群討論摘錄

### 選擇 Godot 做 VN 的理由

**典型正面經驗：**

> 「我從 Ren'Py 轉來 Godot 是因為想加入小遊戲。Ren'Py 的限制讓我很難做自己想要的互動。Dialogic 學習曲線較高，但做到一定程度後自由度大很多。」
> — r/godot, 2024

> 「作為程式設計師，我更喜歡 GDScript 的靈活性。Ren'Py 的腳本對非程式背景友善，但對我來說反而是限制。」
> — Godot Discord

> 「我的專案是 VN + 探索元素。Unity 太重，Ren'Py 做不到我要的自由移動。Godot 正好在中間。」
> — itch.io 開發者日誌

**典型負面經驗 / 挑戰：**

> 「存檔系統要自己寫是真的痛苦。Ren'Py 一行搞定的東西，我在 Godot 花了一整天。」
> — r/vndevs

> 「Dialogic 2 的文件還在完善中，有些功能要自己翻原始碼才知道怎麼用。」
> — Dialogic Discord

> 「回顧歷史（backlog）功能我自己寫了 300 行。每次看到 Ren'Py 內建就想哭。」
> — 開發者 Twitter

### Dialogic 1.x vs 2.x 的遷移

**社群觀察：**

> 「Dialogic 2 是完全重寫，不要期待可以直接遷移 1.x 專案。」
> — Dialogic GitHub Issues

> 「2.x 的新架構更強大，但學習曲線也更高。如果你的專案已經在 3.x + Dialogic 1 上跑得好好的，沒必要急著升級。」
> — r/godot

**遷移建議：**
- 新專案直接用 Godot 4 + Dialogic 2
- 舊專案評估是否真的需要 Godot 4 的新功能
- 等 Dialogic 2 穩定再遷移（追蹤 Release Notes）

---

## 進階主題

### 長篇 VN 的考量

**效能：**
- Godot 對大量文字處理效能良好
- 圖片資源管理需注意（預載 vs 動態載入）
- 數百個場景的專案需要良好的資料夾結構

**維護性：**
- Dialogic Timeline 可能變得很長
- 考慮拆分成多個 Timeline
- 使用變數和信號進行模組化

### 主機移植

**Switch / PlayStation / Xbox：**
- Godot 官方無主機 Export
- 需透過第三方移植服務
- 主要選項：
  - **Lone Wolf Technology**（Switch）
  - **Pineapple Works**（多平台）
- 成本數千美元起，視專案複雜度

**手機：**
- Android / iOS 原生支援
- 但 UI 需要針對觸控優化
- 解析度適配需測試

---

## Godot VN 開發 Discord / 社群

| 社群 | 連結 | 特點 |
|------|------|------|
| Godot 官方 Discord | https://discord.gg/godotengine | 大型社群，有專門頻道 |
| Dialogic Discord | https://discord.gg/dialogic | 插件專門，開發者活躍 |
| r/godot | https://www.reddit.com/r/godot/ | Reddit 討論 |
| r/vndevs | https://www.reddit.com/r/vndevs/ | VN 開發通用，有 Godot 討論 |
| Godot Forum | https://forum.godotengine.org/ | 官方論壇 |

---

## 待研究

- Godot 4 + Dialogic 2 的穩定性評估（持續追蹤中）
- 更多使用 Godot 製作的商業 VN 案例收集
- 與 Unity / Naninovel 的詳細比較
- 長篇 VN 在 Godot 中的效能實測
- 主機移植的實際案例與成本

---

## 關鍵字

**英文：** godot visual novel, dialogic tutorial, godot dialogue system, godot vn plugin, godot narrative game

**日文：** Godot ノベルゲーム, Godot ADV, Dialogic チュートリアル

**中文：** Godot 視覺小說, Godot 對話系統, Dialogic 教學

---

*狀態：初稿，Godot VN 生態仍在發展中*
