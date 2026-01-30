# 互動小說（Interactive Fiction）與視覺小說的譜系

互動小說（Interactive Fiction, IF）是視覺小說的重要先驅與並行類型。探索兩者之間的關係，有助於理解 VN 設計選擇的歷史脈絡，以及可借鑑的設計空間。

---

## 什麼是互動小說

### 基本定義

**狹義定義：**
- 純文字為主的互動敘事
- 玩家透過文字指令或選項與故事互動
- 沒有或極少視覺元素
- 有時被稱為「文字冒險」（Text Adventure）

**廣義定義：**
- 任何以敘事為核心的互動體驗
- 包含 VN、互動電影、Twine 遊戲等
- 此用法下 VN 是 IF 的子類型

本文主要討論狹義的互動小說，探索其與 VN 的異同。

### 歷史脈絡

**1970年代：起源**
- Adventure（1977）/ Colossal Cave Adventure
- 第一款文字冒險遊戲
- 透過文字描述場景，玩家輸入指令

**1980年代：商業黃金期**
- Infocom 公司的系列作品
- Zork 系列成為代表
- 純文字但敘事複雜度高

**1990年代：圖像興起與衰落**
- 圖形冒險遊戲興起
- 純文字 IF 退出主流
- 進入業餘/同人創作時代

**2000年代至今：復興**
- Twine 等工具降低創作門檻
- 獨立遊戲浪潮中重新獲得關注
- 與 VN 形成並行發展

### 現代平台與社群

**主要平台：**
- Interactive Fiction Database（IFDB）
- itch.io 的 IF 分類
- Choice of Games（選項式商業 IF）
- Sub-Q Magazine（IF 文學雜誌）

**創作工具：**
- Twine（視覺化分支編輯器，最流行）
- Ink（Inkle Studio 開發的腳本語言）
- ChoiceScript（Choice of Games 的格式）
- Inform（傳統 parser-based IF 工具）
- TADS（另一 parser-based 工具）

**年度競賽：**
- IFComp（最悠久的 IF 競賽，自 1995 年）
- Spring Thing（另一主要競賽）
- XYZZY Awards（IF 界的奧斯卡）

---

## IF 與 VN 的關鍵差異

### 輸入方式

**Parser-based IF：**
```
> 看看房間
這是一個昏暗的書房。有一張書桌和一扇窗戶。

> 打開窗戶
你打開窗戶，涼風吹入。

> 檢查書桌
書桌上有一封信和一支筆。
```

- 玩家需要猜測正確的動詞和名詞
- 高度自由但也高度挫折
- 「猜作者想法」的問題

**Choice-based IF：**
```
你站在書房中央。

- [查看書桌]
- [打開窗戶]
- [離開房間]
```

- 與 VN 的選項系統幾乎相同
- 差異主要在呈現方式（純文字 vs 視覺化）

**VN 的選項：**
- 固定選項，視覺化呈現
- 通常在特定劇情節點出現
- 不需要探索「可以做什麼」

### 視覺呈現

| 元素 | Parser IF | Choice IF | VN |
|------|-----------|-----------|-----|
| 角色立繪 | ❌ | ❌/有時 | ✓ |
| 背景圖 | ❌ | ❌/有時 | ✓ |
| CG | ❌ | ❌ | ✓ |
| UI 設計 | 極簡 | 簡單 | 精緻 |
| 動態效果 | ❌ | 有限 | ✓ |

**VN 是「視覺化的互動小說」這個說法的準確性：**
- 在 choice-based IF 的脈絡下相當準確
- Parser-based IF 的互動模式則差異較大
- 兩者在「故事驅動」這點上一致

### 文字密度與呈現

**IF 的文字傾向：**
- 環境描述詳盡（因為沒有視覺）
- 敘述者聲音明顯
- 可能更接近傳統小說的文風
- 段落可以很長

**VN 的文字傾向：**
- 對話為主
- 環境描述較少（有圖補充）
- 對話框大小限制文字長度
- 閱讀節奏更碎片化

**例子對比：**

IF 風格：
> 你走進圖書館。這是一個寬敞的房間，天花板高聳，橡木書架從地板延伸到天花板，每一層都塞滿了褪色的書脊。空氣中瀰漫著舊紙和灰塵的氣味。陽光透過彩繪玻璃窗灑落，在地板上投下斑駁的光影。在房間的盡頭，一位白髮老人坐在扶手椅上，似乎在打盹。

VN 風格：
> 背景切換至：圖書館內部

> 【主角內心】
> 好大的圖書館......

> 【主角內心】
> 那邊有個老人在睡覺？

---

## 設計技巧的借鑑

### IF 對 VN 的可能借鑑

**探索式敘事：**
- IF 常允許玩家自由探索環境
- VN 傾向線性推進
- 可能的混合：VN 中加入「探索模式」場景

**世界模型的豐富度：**
- Parser IF 需要建立可互動的物件系統
- 每個物件都有描述、可能的互動
- VN 可借鑑：更豐富的環境互動選項

**敘述者作為角色：**
- IF 中敘述者常有明確的聲音和個性
- 可以評論、諷刺、誤導
- VN 通常敘述者較中性
- 潛在設計空間：有個性的敘述者

**非線性結構：**
- IF 社群發展了豐富的非線性敘事技巧
- Sam Kabo Ashwell 的「IF 結構分類學」
- 包括：洞穴、分支、循環、集中、環狀等

**極短篇形式：**
- IF 競賽作品常是 15-60 分鐘的體驗
- VN 傾向較長篇幅
- 短篇 VN 的設計可參考 IF 的精煉技巧

### VN 對 IF 的影響

**視覺化的價值：**
- 許多現代 IF 開始加入視覺元素
- Twine 遊戲常有圖片、動畫、音效
- 模糊兩者的界線

**角色中心的敘事：**
- 傳統 IF 較環境/謎題中心
- VN 的角色刻畫技巧影響現代 IF
- 浪漫/情感線在 IF 中增加

**商業可行性啟示：**
- VN 證明「閱讀為主的遊戲」有市場
- 啟發 IF 作者探索商業化可能
- Choice of Games 的成功部分受 VN 市場鼓舞

---

## 重要的 IF 作品

### 經典時期（1980-1990年代）

**Zork 系列（Infocom, 1977-）**
- 文字冒險的代名詞
- 建立了許多 IF 的慣例
- 「You are likely to be eaten by a grue」

**A Mind Forever Voyaging（Infocom, 1985）**
- Steve Meretzky 作品
- 社會科幻主題
- 被視為「IF 作為文學」的早期嘗試

**Trinity（Infocom, 1986）**
- Brian Moriarty 作品
- 核戰主題
- 文學性獲高度評價

**Photopia（Adam Cadre, 1998）**
- 非線性敘事結構
- 情感衝擊力強
- 證明 IF 可以處理嚴肅主題

### 現代 Choice-based IF

**Choice of Games 系列**
- 商業化最成功的 IF 出版商
- 以手機為主要平台
- 數值系統 + 長篇敘事
- 代表作：Choice of the Deathless、The Wayhaven Chronicles

**80 Days（Inkle, 2014）**
- 改編凡爾納《環遊世界八十天》
- 大量分支的旅行敘事
- 獲多項遊戲獎項
- 在商業和評論上都成功

**Sorcery! 系列（Inkle）**
- 改編 Fighting Fantasy 書系
- 圖文結合
- 保留骰子元素

**Fallen London / Sunless Sea / Sunless Skies（Failbetter Games）**
- 建立了龐大的敘事世界
- Quality-based Narrative（QBN）系統
- 片段式敘事累積

### 藝術/實驗性 IF

**Galatea（Emily Short, 2000）**
- 單一場景、單一角色的對話
- 探索「人工智慧/人造物的意識」
- 高度非線性的對話樹
- 被視為 IF 的里程碑

**Spider and Web（Andrew Plotkin, 1998）**
- 嵌套敘事結構
- 「敘述不可靠」作為機制
- 玩家說謊 vs 說實話

**Shade（Andrew Plotkin, 2000）**
- 心理恐怖
- 空間逐漸崩解
- 氛圍營造的典範

**Howling Dogs（Porpentine, 2012）**
- Twine 遊戲的代表作
- 探索困境與逃避
- 詩意的語言

**With Those We Love Alive（Porpentine, 2014）**
- 要求玩家在身上畫符號
- 打破第四面牆
- 儀式性的互動

**Depression Quest（Zoe Quinn, 2013）**
- 以憂鬱症經驗為主題
- 選項會被劃掉（「你無法選擇這個」）
- 引發關於「遊戲」定義的討論

### 與 VN 風格接近的 IF

**Analogue: A Hate Story（Christine Love, 2012）**
- 技術上是 VN 但有強烈 IF 設計思維
- 資料庫探索式敘事
- 韓國歷史與 AI 主題

**Digital: A Love Story（Christine Love, 2010）**
- 模擬 1988 年的 BBS 介面
- 非傳統的 VN/IF 混合
- 介面即敘事

---

## IF 的敘事結構分類

Sam Kabo Ashwell 發展的 IF 結構分類法，對 VN 設計也有參考價值：

### 線性（Linear）

```
A → B → C → D
```

- 沒有真正的分支
- Kinetic Novel 屬於此類
- IF 中較少見

### 分支與瓶頸（Branch and Bottleneck）

```
    ┌─ B1 ─┐
A → ┼─ B2 ─┼ → C → ...
    └─ B3 ─┘
```

- 分支後合流
- VN 常見模式
- 管理複雜度的妥協

### 探索/謎題樞紐（Quest / Puzzle Hub）

```
        ┌─ B ─┐
    A → ┼─ C ─┼ → 終點
        └─ D ─┘
```

- 從中心點探索多個區域
- 收集必要物品/資訊後推進
- 傳統冒險遊戲模式

### 分支（Branching）

```
    ┌─ B ─┬─ E
A → ┤     └─ F
    └─ C ─┬─ G
          └─ H
```

- 選擇導向不同結局
- 乙女遊戲的角色路線
- 成本高，重複內容管理困難

### 時間洞穴（Time Cave）

極端的分支，幾乎每個選擇都分裂：

```
    ┌─ B ─┬─ D
    │     └─ E
A → ┤
    └─ C ─┬─ F ─┬─ H
          │     └─ I
          └─ G
```

- 大量短結局
- 早期 CYOA 書常見
- 現代較少用（太碎片）

### 浮木（Floating Modules）

```
[A] [B] [C] [D] [E]
   ↘   ↓   ↙
      [F]
```

- 非線性碎片，最終收束
- 順序可變但必須經歷全部
- Her Story 的設計接近此

### 迴圈與成長（Loop and Grow）

```
    ┌────────────┐
    │            ↓
A → ┼─→ B → C → A'
    │
    └─→ 結局
```

- 時間迴圈敘事
- 每次循環有新資訊/選項
- Undertale、Zero Escape 的元素

### 品質式敘事（Quality-Based Narrative）

不是單純的「如果A則B」，而是：

```
條件：勇氣 > 5 且 有劍 且 見過長老
→ 解鎖選項：挑戰龍
```

- Fallen London 的核心系統
- 累積式的敘事解鎖
- 可重複遊玩的內容

---

## 跨界創作者

### Christine Love

- **Digital: A Love Story**（2010）
- **Analogue: A Hate Story**（2012）
- **Hate Plus**（2013）
- **Ladykiller in a Bind**（2016）

特徵：
- 從 IF 社群背景出發
- 融合 IF 設計思維與 VN 視覺
- 介面創新（模擬舊電腦、檔案系統）

### Emily Short

- IF 社群最重要的作者/評論者之一
- **Galatea**、**Counterfeit Monkey**
- 為 Failbetter Games 工作
- 大量關於互動敘事的理論文章

影響 VN 開發者的觀點：
- 對話系統設計的深入分析
- NPC 反應的「社會模型」
- 世界模型與敘事的關係

### Porpentine

- Twine 遊戲的代表作者
- **Howling Dogs**、**With Those We Love Alive**
- 詩意、超現實、常涉及創傷主題

風格特徵：
- 文字的節奏與畫面感
- 非傳統的互動設計
- 模糊遊戲與詩的界線

---

## IF 與 VN 的受眾比較

### IF 的傳統受眾

- 英語為主
- 文學傾向
- 接受純文字
- 較高的「讀者」認同（vs「玩家」）
- 獨立/小眾社群

### VN 的主流受眾

- 國際化但以日本為原生市場
- ACG 文化背景
- 期待視覺呈現
- 「玩家」認同
- 較大的商業市場

### 重疊區域

- 對敘事的高度興趣
- 接受閱讀為主的體驗
- 對「選擇」的意義有興趣
- 獨立遊戲愛好者
- 追求不同於 AAA 遊戲的體驗

### 相互引介的可能

**IF → VN：**
- 喜歡 IF 但想要更多視覺的讀者
- 對日式敘事/美學有興趣的 IF 玩家
- 入門推薦：Analogue: A Hate Story

**VN → IF：**
- 想要更多選擇自由度的 VN 玩家
- 對純敘事（無養成/收集）有興趣者
- 入門推薦：80 Days、Choice of Games 系列

---

## 工具比較

### IF 工具

**Twine**
- 視覺化分支編輯器
- 完全免費
- HTML/CSS/JavaScript 為基礎
- 低技術門檻
- 限制：主要輸出網頁

**Ink / Inky**
- Inkle 開發
- 專為分支對話設計的語言
- 可整合到 Unity
- 語法乾淨，適合作家

**ChoiceScript**
- Choice of Games 的格式
- 專為數值+選項設計
- 必須透過 CoG 或 Hosted Games 發行

**Inform 7**
- 以「自然英語」為基礎的程式語言
- 專為 parser-based IF 設計
- 學習曲線較陡

### VN 工具

**Ren'Py**
- Python 基礎
- 最流行的免費 VN 引擎
- 功能完整

**Tyrano Builder / TyranoScript**
- 日本開發
- 視覺化編輯器

**Visual Novel Maker**
- RPG Maker 系列的 VN 版
- 商業軟體

**Unity + Naninovel / Fungus**
- 使用通用遊戲引擎
- 彈性高但學習成本高

### 工具選擇的影響

**Twine 的「IF 風格」：**
- 網頁為主
- 視覺極簡
- 分支設計為核心

**Ren'Py 的「VN 風格」：**
- 獨立可執行檔
- 視覺精緻度期待
- 對話框、立繪、CG 為核心

工具選擇會影響創作者思考設計的方式，也會影響作品被歸類的類型。

---

## 術語對照

| IF 術語 | VN 術語 | 說明 |
|---------|---------|------|
| Parser | — | 文字輸入解析器 |
| Choice-based | 選項式 | 預設選項供選擇 |
| Hypertext | — | 點擊文字連結前進 |
| CYOA | — | Choose Your Own Adventure |
| WIP | 製作中 | Work in Progress |
| Comp | — | 競賽（IFComp） |
| NPC | 攻略對象/角色 | 非玩家角色 |
| PC | 主角 | 玩家角色 |
| Transcript | — | 遊玩記錄 |
| — | 立繪 | 角色圖像 |
| — | CG | 事件插圖 |
| — | BGM | 背景音樂 |
| — | 路線 | 角色專屬劇情線 |
| — | 共通線 | 所有路線共享的部分 |

---

## 待探索方向

- IF 的「環境敘事」技巧如何轉譯到 VN
- Parser 式 VN 的可能性（語音輸入？）
- IF 社群的評論文化可供 VN 社群參考之處
- 跨社群合作與作品交流
- 教育用途：IF 與 VN 在敘事教學中的應用
- AI 時代：LLM 對 IF/VN 創作的影響差異

---

## 延伸閱讀

**Emily Short's Interactive Storytelling**
- https://emshort.blog/
- IF 理論與設計的重要資源

**Standard Patterns in Choice-Based Games**
- Sam Kabo Ashwell 的結構分析文章

**IFDB（Interactive Fiction Database）**
- https://ifdb.org/
- IF 作品資料庫與評論

**Twine Cookbook**
- Twine 設計的技巧集

**Choice of Games 設計文件**
- 公開的 ChoiceScript 最佳實踐

---

*狀態：初稿，持續累積範例與分析*
