# Unity 視覺小說開發生態深度剖析

Unity 作為最廣泛使用的商業遊戲引擎之一，雖非專為 VN 設計，但透過插件與框架的支援，已成為製作混合型 VN 或商業級作品的重要選項。本文件探討 Unity 在 VN 開發中的角色、主要框架、適用場景與實際考量。

---

## 為何選擇 Unity 做 VN？

### 適合 Unity 的情況

**混合類型需求：**
- VN + RPG 戰鬥系統
- VN + 經營模擬元素
- VN + 小遊戲穿插
- 3D 場景或角色

**商業規模考量：**
- 團隊有 Unity 經驗
- 需要與現有 Unity 專案整合
- 計畫長期維護與擴展
- 多平台發布需求（含主機）

**技術需求：**
- 複雜的畫面演出效果
- 即時 3D 渲染
- 進階 shader 效果
- 高度自訂的 UI 系統

### 不適合 Unity 的情況

- 純文字敘事、選擇導向的傳統 VN
- 小規模或獨立開發，無 Unity 經驗
- 快速原型或 Game Jam
- 預算有限且時間緊迫

**核心權衡：**
> Unity 提供了「做任何事」的能力，但這也意味著需要「自己實作很多事」。

---

## 主要 VN 框架概覽

### Naninovel（商業首選）

**基本資訊：**
- 開發商：Elringus
- 價格：$158（標準）/ $308（專業）
- 授權：每專案授權，非訂閱
- 官網：https://naninovel.com/
- Asset Store：Unity Asset Store 搜尋 "Naninovel"
- 文件：https://naninovel.com/guide/

**核心特色：**

**專用腳本語言（NaniScript）：**
```naninovel
@char Saki.Idle pos:0.5
@bgm MainTheme
Saki: 早安！今天天氣真好。
@choice "一起出去吧" goto:GoOut | "還是待在家" goto:StayHome
```
- 語法簡潔，非程式設計師可閱讀
- 類似 Ren'Py 的設計哲學
- 熱重載：修改腳本後即時預覽

**功能完整度：**
- 對話系統（立繪、表情切換、語音）
- 選擇與分支
- 存讀檔（多槽位、自動、截圖）
- 本地化（多語言支援、翻譯管理）
- 回顧對話（Backlog）
- 自動/跳過模式
- CG 畫廊、音樂鑑賞室
- 劇本熱重載

**Unity 整合優勢：**
- 可與 Unity 任何功能共存
- 支援自訂 C# 擴展
- 可在 VN 段落中觸發 Unity 場景
- 支援 Addressables（資源管理）

**社群與支援：**
- Discord 社群活躍
- 開發者回應快速
- 文件詳細
- 付費用戶支援管道

---

### Fungus（免費開源選項）

**基本資訊：**
- 開發：Snozbot（Chris Gregan）
- 價格：免費（MIT 授權）
- GitHub：https://github.com/snozbot/fungus
- 文件：https://fungusgames.com/

**核心特色：**

**視覺化流程圖：**
- 拖放式節點編輯
- 不需要寫程式碼即可製作基本 VN
- 直覺的分支與條件設定

**功能範圍：**
- 基本對話系統
- 選擇分支
- 變數與條件
- 音效與音樂控制
- 簡單動畫

**適合情境：**
- 教學用途
- 快速原型
- 簡單的互動敘事
- 非程式設計師的入門

**限制：**
- 功能不如 Naninovel 完整
- 複雜專案可能需要大量自訂
- 更新頻率較低
- 大型專案管理較困難

---

### Ink + Unity（敘事專精）

**基本資訊：**
- 開發：Inkle Studios
- 價格：免費（MIT 授權）
- 官網：https://www.inklestudios.com/ink/
- GitHub：https://github.com/inkle/ink
- Unity 整合：https://github.com/inkle/ink-unity-integration

**Ink 的特色：**

**專為分支敘事設計：**
```ink
=== morning ===
你醒來，陽光透過窗簾灑入房間。
* [起床] -> get_up
* [再睡一會] -> sleep_more
* {visited_cafe} [去咖啡店] -> cafe

=== get_up ===
你伸了個懶腰，決定面對新的一天。
-> morning_routine
```

**核心優勢：**
- 極度專注於文字與分支
- 強大的條件與狀態管理
- 支援 knots、stitches、weaves 等結構
- 可處理極複雜的敘事邏輯

**使用模式：**
- Ink 處理所有敘事邏輯
- Unity 處理視覺呈現
- 需要自行建構 UI 系統
- 彈性最大但工作量也最大

**代表作品：**
- 80 Days（Inkle）
- Heaven's Vault（Inkle）
- Sorcery! 系列（Inkle）
- Citizen Sleeper（部分使用）

**適合情境：**
- 文字量極大的作品
- 複雜分支結構
- 已有 Unity 團隊
- 需要完全自訂視覺風格

---

### 其他 Unity VN 工具

**Dialogue System for Unity：**
- https://www.pixelcrushers.com/dialogue-system/
- 通用對話系統，非專為 VN
- 可用於 RPG、冒險遊戲等
- 功能強大但設定複雜

**Visual Novel Toolkit (VNTK)：**
- 較舊的解決方案
- 更新較少
- 功能相對有限

**Yarn Spinner：**
- https://yarnspinner.dev/
- 類似 Ink 的敘事工具
- 有視覺化編輯器
- Night in the Woods 使用

---

## Naninovel 深度剖析

### 功能詳解

**角色系統：**

```naninovel
; 角色定義（Resources/Naninovel/Characters/Saki/）
; 或透過設定面板管理

@char Saki.Happy pos:0.3
@char Yuki.Sad pos:0.7
Saki: 你怎麼了？看起來不太開心。
@char Yuki.Embarrassed
Yuki: 沒...沒什麼。
```

- 支援立繪差分（表情、服裝、姿勢）
- 位置動畫
- 多角色同時顯示
- Live2D 整合（需額外設定）

**場景與背景：**

```naninovel
@back School transition:crossfade time:1
@sfx SchoolBell
@wait 0.5
; 場景已經切換完成
```

- 多層背景
- 轉場效果（內建多種）
- 自訂 shader 支援

**選擇與分支：**

```naninovel
@choice "告白" goto:Confession | "再等等" goto:Wait | "放棄" goto:GiveUp

# Confession
Saki: 我...我喜歡你！
@set affection+=5
@goto SharedEnding

# Wait
Saki: 也許下次吧...
@goto NextDay
```

- 條件顯示選項
- 變數管理
- 跳轉與標籤系統

**存讀檔系統：**
- 自動存檔
- 多槽位存檔
- 存檔截圖
- 雲端存檔整合（自訂）

**本地化：**

```naninovel
; Localization/ja/Scripts/Scene1.nani
Saki: おはようございます！

; Localization/en/Scripts/Scene1.nani  
Saki: Good morning!
```

- 翻譯腳本分離
- 資源本地化（圖片、音效）
- 語言切換 UI

---

### 工作流程

**典型開發流程：**

1. **設定專案**
   - 安裝 Naninovel 插件
   - 設定資源路徑
   - 設定角色與背景

2. **撰寫腳本**
   - 使用 NaniScript 或 C# API
   - 利用熱重載即時測試
   - 版本控制友好（純文字腳本）

3. **整合素材**
   - 匯入立繪、背景
   - 設定音樂與音效
   - 配置 UI 風格

4. **Unity 整合**
   - 添加自訂遊戲機制
   - 連接其他 Unity 系統
   - 自訂指令擴展

5. **測試與發布**
   - 多路線測試
   - 各平台測試
   - 打包發布

**專案結構範例：**

```
Assets/
├── Naninovel/
│   ├── Resources/
│   │   ├── Characters/
│   │   │   ├── Saki/
│   │   │   │   ├── Saki.Happy.png
│   │   │   │   ├── Saki.Sad.png
│   │   │   │   └── Saki.Idle.png
│   │   │   └── Yuki/
│   │   ├── Backgrounds/
│   │   ├── Audio/
│   │   └── Scripts/
│   │       ├── Chapter1.nani
│   │       └── Chapter2.nani
│   └── Localization/
│       ├── en/
│       └── ja/
├── Scripts/  (自訂 C# 腳本)
├── Scenes/
└── Prefabs/
```

---

### 效能考量

**記憶體管理：**
- Naninovel 使用 Unity 的資源管理系統
- 支援 Addressables 以優化載入
- 大型專案需注意素材壓縮
- 可設定資源卸載策略

**行動平台：**
- 需要額外測試與優化
- 圖片壓縮格式選擇重要
- 存檔大小管理
- 冷啟動時間

**建議：**
- 立繪使用適當解析度（不必過大）
- 音樂使用串流而非完全載入
- 背景圖視需要壓縮
- 測試各目標平台

---

## 成本效益分析

### Naninovel 成本考量

**直接成本：**
- 插件購買：$158-$308
- Unity 授權：免費（個人版）/ $2040/年（專業版）

**隱藏成本：**
- 學習曲線（Unity + Naninovel）
- 自訂功能開發時間
- Unity 升級維護

**節省的成本：**
- 不需從頭建構 VN 系統
- 減少常見 bug
- 內建本地化系統

### 與 Ren'Py 的比較

| 面向 | Ren'Py | Naninovel |
|------|--------|-----------|
| 價格 | 免費 | $158+ |
| 學習曲線 | 平緩 | 較陡（需懂 Unity） |
| 功能完整度 | 高（VN 專用） | 高（需 Unity） |
| 混合類型 | 有限（主要 2D） | 強（Unity 全功能） |
| 3D 支援 | 有限 | 完整 |
| 社群規模 | 極大 | 中等 |
| 文件品質 | 優 | 優 |
| 主機發布 | 困難 | 較易（Unity 原生） |

### 選擇建議

**選擇 Ren'Py 當：**
- 純 2D VN
- 獨立開發 / 小團隊
- 預算有限
- 快速開發週期

**選擇 Unity + Naninovel 當：**
- 混合類型遊戲
- 已有 Unity 技術棧
- 商業級專案
- 需要 3D 或複雜演出
- 多平台（含主機）發布

---

## 商業案例

### 使用 Naninovel 的作品

**已發布作品：**
- 多數為中小型獨立作品
- Asset Store 有展示案例
- Discord 社群有用戶分享

**類型分布：**
- 純 VN（少）
- VN + RPG 混合
- VN + 經營模擬
- 3D VN

### 使用其他 Unity 方案的作品

**Ink 系列：**
- 80 Days（商業成功）
- Heaven's Vault（好評）
- Sorcery! 系列

**自訂方案：**
- 許多商業 VN 使用自建系統
- 大公司傾向自行開發
- 但成本遠高於插件方案

---

## 常見問題與陷阱

### 新手常見問題

**Unity 學習曲線：**
- 需要先理解 Unity 基礎
- GameObject、Component、Prefab
- Inspector 與 Project 視窗操作
- 建議：先完成 Unity 入門教學

**資源路徑問題：**
- Naninovel 有特定資源結構需求
- 路徑大小寫敏感
- 資源命名規範

**腳本語法錯誤：**
- NaniScript 有特定語法
- 縮排與空格敏感
- 使用內建語法檢查

### 進階陷阱

**過度工程：**
- Unity 功能太多，容易失焦
- 應專注於 VN 核心體驗
- 不要因為「能做」就做

**效能問題：**
- Unity 專案容易膨脹
- 素材管理需要規劃
- 行動平台需額外注意

**版本升級：**
- Unity 升級可能破壞專案
- Naninovel 升級需測試相容性
- 建議：穩定後不輕易升級

---

## 學習資源

### 官方資源

**Naninovel：**
- 文件：https://naninovel.com/guide/
- Discord：官網連結
- YouTube：官方教學影片

**Unity：**
- Unity Learn：https://learn.unity.com/
- 官方文件：https://docs.unity3d.com/

### 社群資源

**Discord：**
- Naninovel 官方 Discord
- Unity VN 開發相關伺服器

**YouTube：**
- Naninovel 官方頻道
- 各種 Unity VN 教學

**論壇：**
- Unity Forums
- Lemma Soft（有 Unity 討論區）

### 學習路徑建議

**Unity 新手：**
1. Unity 基礎教學（2-4 週）
2. C# 基礎（如未學過）
3. Naninovel Quickstart（1 週）
4. 製作第一個短篇 VN

**Unity 熟手：**
1. Naninovel 文件閱讀
2. 範例專案研究
3. 自訂指令開發
4. 整合自有系統

---

## 相關連結

### Naninovel

- 官網：https://naninovel.com/
- 文件：https://naninovel.com/guide/
- Asset Store：搜尋 "Naninovel"
- GitHub（範例）：https://github.com/Naninovel

### Fungus

- 官網：https://fungusgames.com/
- GitHub：https://github.com/snozbot/fungus
- 文件：https://fungusdocs.snozbot.com/

### Ink

- 官網：https://www.inklestudios.com/ink/
- GitHub：https://github.com/inkle/ink
- Unity 整合：https://github.com/inkle/ink-unity-integration
- Inky 編輯器：https://github.com/inkle/inky

### Unity

- 官網：https://unity.com/
- Learn：https://learn.unity.com/
- Asset Store：https://assetstore.unity.com/

---

## 待研究問題

- Naninovel 與 Live2D 整合的詳細流程
- Unity VN 作品的商業案例收集
- Ink vs NaniScript 的敘事能力比較
- 主機平台發布的具體流程與成本
- 中文 Unity VN 開發社群的生態

---

*狀態：初稿，持續累積中*
