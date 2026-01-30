# 銷量數據與開發者分享

收集 VN 銷量數據的來源、開發者事後分析（postmortem）、以及市場觀察。本文件不做結論，僅整理可查證的參考點。

---

## 數據來源管道

### Steam 相關

**SteamDB**
- https://steamdb.info/
- 可查詢評論數、追蹤者數、歷史價格
- 評論數 × 30-50 ≈ 粗估銷量（Boxleiter method）
- 免費，資料相對準確

**Steam Spy**
- https://steamspy.com/
- 估算銷量範圍
- 2018 年後因 Steam 隱私政策而準確度下降
- 仍可作為參考

**VG Insights**
- https://vginsights.com/
- 付費工具，較精確的銷量估算
- 有免費預覽功能

**Gamalytic**
- https://gamalytic.com/
- 另一個 Steam 數據分析工具
- 部分功能免費

### VNDB 資料

**VNDB**
- https://vndb.org/
- 評分、人氣、發行資訊
- 無銷量數據，但可觀察社群熱度
- 「Popularity」排名反映被加入清單的次數

### 開發者自行公開

最準確的來源是開發者自己公開的數據：
- GDC / GAMES 演講
- 開發者部落格
- Twitter/X 發文
- Reddit AMA
- Gamasutra / Game Developer 文章

---

## 已公開的銷量案例

### 西方獨立 VN

**Doki Doki Literature Club! (DDLC)**
- 開發者：Team Salvato
- 發行：2017
- 模式：免費（有付費 Plus 版）
- 數據：原版下載量超過 1100 萬（2021）
- Plus 版 Steam 評論約 4 萬+
- 來源：開發者社群公告、Steam 頁面

**VA-11 Hall-A**
- 開發者：Sukeban Games
- 發行：2016
- 定價：$14.99
- 數據：首年銷量約 10 萬份（開發者 Twitter）
- 2020 年總銷量估計 50 萬+
- 來源：開發者公開、SteamDB 推估

**Coffee Talk**
- 開發者：Toge Productions
- 發行：2020
- 定價：$12.99
- 數據：首週約 3 萬份（Game Developer 文章）
- 來源：[Game Developer postmortem](https://www.gamedeveloper.com/)

**Katawa Shoujo**
- 開發者：Four Leaf Studios
- 發行：2012
- 模式：免費
- 數據：累計下載量超過 400 萬（2019）
- 來源：開發者統計頁面

**Slay the Princess**
- 開發者：Black Tabby Games
- 發行：2023
- 定價：$17.99（後漲至 $19.99）
- 數據：首月估計 10 萬+（SteamDB 評論推算）
- 來源：SteamDB、開發者社群

**The Coffin of Andy and Leyley**
- 開發者：Kit9 Studio（solo dev）
- 發行：2023（Early Access）
- 定價：$9.99
- 數據：Steam 評論約 3.5 萬+（2024）
- 特點：RPG Maker + VN 混合，爭議性內容帶來病毒傳播
- 來源：SteamDB

**Necrobarista**
- 開發者：Route 59（澳洲）
- 發行：2020
- 定價：$21.99
- 數據：Steam 評論約 2,500+
- 特點：3D 視覺風格、澳洲團隊
- 來源：Steam、開發者 GDC 演講

**Boyfriend Dungeon**
- 開發者：Kitfox Games
- 發行：2021
- 定價：$19.99
- 數據：首週 PC 銷量估計約 10 萬+（含 Game Pass）
- 特點：Roguelike + 約會模擬混合
- 來源：Game Developer 訪談

**Lake**
- 開發者：Gamious
- 發行：2021
- 定價：$19.99
- 數據：Steam 評論約 4,000+
- 特點：郵差模擬 + 敘事，收入足以支持續作
- 來源：開發者部落格

**Eliza**
- 開發者：Zachtronics
- 發行：2019
- 定價：$14.99
- 數據：Steam 評論約 1,500+
- 特點：AI 諮商主題，知名工作室的 VN 嘗試
- 來源：Steam

**Spirit Hunter: Death Mark / NG**
- 發行商：Aksys Games（西方版）
- 定價：$49.99
- Steam 評論：各約 500-1,000
- 特點：恐怖 ADV 系列，主機優先

**Our Life: Beginnings & Always**
- 開發者：GB Patch Games
- 發行：2020
- 模式：免費本篇 + DLC
- 數據：Steam 評論約 18,000+（免費版）
- 特點：乙女遊戲、DLC 模式成功案例
- 來源：Steam、開發者 Tumblr

**Arcade Spirits**
- 開發者：Fiction Factory Games
- 發行：2019
- 定價：$19.99
- 數據：Steam 評論約 1,200+
- 特點：復古街機主題、包容性角色設計
- 來源：Steam、開發者訪談

---

### 日本商業 VN（英文版）

**Steins;Gate**
- 發行商：Spike Chunsoft（英文版）
- Steam 發行：2016
- 定價：$29.99（常態）
- Steam 評論：約 2.7 萬+
- 推估 Steam 銷量：80-150 萬範圍

**CLANNAD**
- 發行商：Sekai Project
- Steam 發行：2015
- 定價：$49.99（高價位策略）
- Steam 評論：約 1.3 萬+
- 眾籌：Kickstarter 目標 $140K，實際 $541K

**The House in Fata Morgana**
- 發行商：MangaGamer
- Steam 發行：2016
- 定價：$24.99
- Steam 評論：約 6,000+
- 以極高評價獲得長尾效應

**Umineko When They Cry**
- 發行商：MangaGamer
- Steam 發行：2016-2017（分卷）
- 定價：各 $24.99
- Steam 評論：Question Arc 約 5,000+、Answer Arc 約 3,000+
- 特點：超長篇、Steam 版有語音補丁爭議

**Danganronpa 系列**
- 發行商：Spike Chunsoft
- Steam 發行：2016 起
- 定價：各 $19.99-29.99
- Steam 評論：1 代約 3.5 萬+、2 代約 2.5 萬+、V3 約 1.5 萬+
- 推估總銷量：數百萬（全平台）

**Doki Doki Literature Club Plus!**
- 發行商：Serenity Forge
- Steam 發行：2021（付費版）
- 定價：$14.99
- Steam 評論：約 4 萬+
- 特點：免費版成功後的付費升級版

**Higurashi When They Cry**
- 發行商：MangaGamer
- Steam 發行：2015-2019（分卷發行）
- 定價：各 $5.99-7.99
- 特點：分卷策略、社群自製語音/PS3 畫面補丁

**AI: The Somnium Files**
- 發行商：Spike Chunsoft
- Steam 發行：2019
- 定價：$59.99（首發）
- Steam 評論：約 6,000+
- 來自《極限脫出》創作者

**Raging Loop**
- 發行商：PQube
- Steam 發行：2019
- 定價：$29.99
- Steam 評論：約 2,500+
- 特點：人狼遊戲 + 循環敘事

**Chaos;Head Noah / Chaos;Child**
- 發行商：Spike Chunsoft
- Steam 發行：2022-2023
- 定價：$24.99
- Steam 評論：Noah 約 2,000+、Child 約 1,500+
- 科學 ADV 系列補完

**Aokana: Four Rhythms Across the Blue**
- 發行商：NekoNyan
- Steam 發行：2019
- 定價：$34.99
- Steam 評論：約 3,000+
- 特點：sprite 社代表作、運動 + 戀愛

**Riddle Joker**
- 發行商：NekoNyan
- Steam 發行：2020
- 定價：$44.99
- Steam 評論：約 2,500+
- 特點：ゆずソフト代表作

---

### 中文原創 VN

**隱形守護者**
- 開發者：New One Studio
- 發行：2019
- 定價：¥78（約 $11）
- 數據：首月銷量超過 100 萬份（官方公告）
- Steam 評論：約 11 萬+
- 真人互動影視形式

**OPUS 系列（SIGONO）**
- 開發者：SIGONO
- 地區：台灣
- 《OPUS: 龍脈常歌》：Steam 評論約 5,000+
- 跨平台（Steam + Switch + Mobile）
- 定價：$14.99-19.99

**煙火**
- 開發者：拾英工作室
- 發行：2021
- 定價：¥38（約 $6）
- Steam 評論：約 4 萬+
- RPG Maker 恐怖解謎 + VN 元素

**三色繪戀**
- 開發者：SukeraSparo（中國分部）
- 發行：2018
- 定價：¥68（約 $10）
- Steam 評論：約 7,000+
- 純愛 ADV

**古劍奇譚：木語人**
- 開發者：網元聖唐
- 發行：2023
- 定價：¥68
- Steam 評論：約 3,000+
- 特點：AVG + 3D 演出、古風

**女神異聞錄 5 同人作品群**
- 如《Persona 5: Thievery》等
- 同人 VN 生態觀察點
- 大多免費或低價

**白色相簿2（官方中文）**
- 發行商：Leaf/Aquaplus
- Steam 發行：2023
- 定價：¥98（約 $14）
- Steam 評論：約 8,000+
- 特點：經典作品官方中文版的延遲需求

**文字遊戲**
- 開發者：Team9
- 發行：2021
- 定價：¥36
- Steam 評論：約 15,000+
- 特點：文字解謎 + 敘事，中國獨立

**山桂**
- 開發者：漫漫長夜工作室
- 發行：2022
- 定價：¥58
- Steam 評論：約 1,500+
- 特點：中式恐怖 + AVG

**紅燒天堂（Loopers 中文）**
- 原作：Key/VisualArts
- 發行：2021
- 定價：¥50
- Steam 評論：約 2,000+
- 特點：Key 社短篇、Ryukishi07 執筆

---

## 開發者 Postmortem 資源

### GDC Vault（部分免費）

**搜尋關鍵字：**
- "visual novel postmortem"
- "indie narrative game"
- "story-driven game sales"

**推薦演講：**
- GDC 每年的 Indie Game Summit 常有小型 VN 開發者分享
- 搜尋 "GDC vault visual novel" 可找到相關演講

**已知相關演講：**
- "The Making of Slay the Princess"（GDC 2024）
- "Writing Necrobarista"（Route 59）
- "Designing Doki Doki Literature Club"（Dan Salvato）
- "Creating Visual Novels for Western Audiences"（歷年 Indie Summit）

### Game Developer / Gamasutra

**網址：** https://www.gamedeveloper.com/

**有用的文章類型：**
- Postmortem 系列
- "By the Numbers" 銷售分析
- Indie game marketing 專題

### Reddit 討論

**r/visualnovels**
- https://reddit.com/r/visualnovels/
- 偶有開發者分享銷售經驗
- 搜尋 "sales numbers" "how much did" "revenue"

**r/vndevs**
- https://reddit.com/r/vndevs/
- VN 開發者專屬社群
- 更多技術與商業討論

**r/gamedev**
- https://reddit.com/r/gamedev/
- 通用獨立遊戲開發
- "Sales Report" flair 可找銷售分享

**r/VisualNovelDev**
- https://reddit.com/r/VisualNovelDev/
- 較新的 VN 開發社群
- 偶有銷售分享和行銷討論

**Itch.io Devlogs**
- 許多小型 VN 開發者在 itch.io 寫 devlog
- 搜尋 "sales" "revenue" "postmortem" 可找分享

**Twitter/X 開發者帳號**
- 追蹤 VN 開發者常有即時數據分享
- 搜尋 "#VNDev" "#indiedev" "sales numbers"

### Lemma Soft Forums

**網址：** https://lemmasoft.renai.us/forums/

**相關板塊：**
- Completed Games（可看到專案規模）
- General Discussion（偶有商業討論）
- 歷史悠久的 Ren'Py 社群

---

## 粗估方法論

### Boxleiter Method（評論推算銷量）

**公式：** 銷量 ≈ 評論數 × 乘數

**乘數範圍：**
- 熱門遊戲：20-30
- 一般遊戲：30-50
- 小眾遊戲：50-100
- VN 傾向較高乘數（玩家留評比例較低）

**注意事項：**
- 僅為粗估
- 免費遊戲的比例完全不同
- 不同類型遊戲差異大
- 促銷期間評論比例下降

### 願望清單轉換率

**一般數據：**
- 首發轉換率：10-20%
- 促銷轉換率：5-15%
- VN 轉換率可能略低（衝動購買少）

### 退款率

**Steam 一般數據：**
- 整體平均：約 5-10%
- VN 可能較低（2 小時內不易判斷品質）
- 短篇 VN 可能較高（2 小時內可能玩完）

---

## 定價參考點

### 獨立 VN 的常見價位

| 長度 | 建議價位（USD）| 說明 |
|------|----------------|------|
| 短篇（<2 小時） | $0-5 | 或免費 + 捐款 |
| 中短篇（2-5 小時） | $5-10 | 獨立中小作品 |
| 中篇（5-15 小時） | $10-15 | 主流獨立價位 |
| 長篇（15-30 小時） | $15-25 | 有自信的作品 |
| 超長篇（30+ 小時） | $20-40 | 品牌認知或系列作 |

### 日本商業 VN（英文版）

| 類型 | 常見價位（USD）| 說明 |
|------|----------------|------|
| 短篇/老作品 | $9.99-14.99 | 促銷常見 $5 以下 |
| 中型作品 | $19.99-29.99 | 主流價位 |
| 大型 / Key 社 / TM | $34.99-49.99 | 品牌溢價 |
| 超大型合集 | $59.99+ | 如 Umineko 完整版 |

---

## 促銷策略觀察

### Steam 促銷週期

| 促銷類型 | 時間 | 折扣深度 |
|----------|------|----------|
| 首發折扣 | 發售時 | 10-20% |
| 週末特賣 | 任意週末 | 20-40% |
| 季節特賣 | 夏促/冬促/秋促/春促 | 30-60% |
| 發行商特賣 | 不定期 | 20-50% |
| 老作品清倉 | 不定期 | 70-90% |

### VN 的長尾特性

**觀察：**
- VN 不像動作遊戲那樣依賴首發
- 口碑傳播、動畫化、實況推廣可帶來後期銷量
- 經典作品持續有新玩家發現
- 但首發仍然重要（演算法曝光）

---

## 眾籌案例

### 成功案例

**CLANNAD（英文版）**
- 平台：Kickstarter
- 目標：$140,000
- 實際：$541,161
- 贊助人：約 5,000
- 結果：成功發行

**Muv-Luv（英文版）**
- 平台：Kickstarter
- 目標：$250,000
- 實際：$1,255,444
- 贊助人：約 8,000
- 結果：系列完整移植

**Grisaia Trilogy（英文版）**
- 平台：Kickstarter
- 目標：$160,000
- 實際：$475,255
- 結果：三部曲完整發行

**Sharin no Kuni**
- 平台：Kickstarter
- 目標：$180,000
- 實際：$543,114
- 狀態：長期延遲，爭議案例

**ISLAND（英文版）**
- 平台：Kickstarter（Frontwing 自營）
- 目標：$160,000
- 實際：$257,088
- 結果：成功發行

**Root Double**
- 平台：Kickstarter
- 目標：$135,000
- 實際：$232,848
- 結果：成功發行

**The Silver Case（SUDA51）**
- 平台：Kickstarter
- 目標：$300,000
- 實際：$469,578
- 結果：成功發行，帶動續作

**西方原創 VN 眾籌**

**Highway Blossoms**
- 平台：Kickstarter
- 規模：約 $30,000+
- 結果：成功發行，獲得好評

**Heart of the Woods**
- 平台：Kickstarter（Studio Élan）
- 規模：中小型
- 結果：成功，工作室持續運作

### 警示案例

（眾籌延期、規模縮水、或未完成的案例存在，但因敏感性不詳列，可搜尋相關討論）

**研究方向：**
- r/visualnovels 的眾籌追蹤討論
- Kickstarter VN 標籤的歷史專案
- Fuwanovel 的眾籌專案追蹤文章

---

## 待補充

- Patreon/Fanbox 成人 VN 的收入案例
- 主機版（Switch）的銷量對比
- 不同年份的市場變化趨勢
- 失敗案例的原因分析（需謹慎處理）
- 韓國 VN 市場數據
- 東南亞市場（越南、印尼等）的 VN 生態

---

## 關鍵字（供後續搜尋）

`visual novel sales numbers`, `VN steam revenue`, `indie vn postmortem`, `visual novel kickstarter`, `ビジュアルノベル 売上`, `galgame 销量`, `Steam 中文 VN 銷量`, `VN dev revenue`, `how much did visual novel make`, `steam reviews to sales`, `boxleiter method`, `VN publisher sales`, `NekoNyan sales`, `MangaGamer revenue`, `Sekai Project kickstarter`

---

## 相關連結

### 數據追蹤工具
- [SteamDB](https://steamdb.info/) - 評論追蹤、價格歷史
- [Steam Spy](https://steamspy.com/) - 銷量估算（精確度受限）
- [VG Insights](https://vginsights.com/) - 付費精確數據
- [Gamalytic](https://gamalytic.com/) - Steam 數據分析
- [HowLongToBeat](https://howlongtobeat.com/) - 遊戲長度參考

### 討論社群
- [r/visualnovels](https://reddit.com/r/visualnovels/) - 西方 VN 主社群
- [r/vndevs](https://reddit.com/r/vndevs/) - 開發者社群
- [Lemma Soft Forums](https://lemmasoft.renai.us/forums/) - Ren'Py 社群
- [Fuwanovel](https://fuwanovel.net/) - VN 翻譯與討論

### 行業媒體
- [Game Developer](https://www.gamedeveloper.com/) - Postmortem 文章
- [GDC Vault](https://gdcvault.com/) - 演講存檔
- [Gematsu](https://www.gematsu.com/) - 日本遊戲新聞

---

*狀態：持續累積公開案例，2025-01 大幅擴充*
