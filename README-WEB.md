# 網站本地預覽指南

本 repo 可透過 MkDocs 生成靜態網站，方便閱讀。

---

## 最少步驟

```bash
# 1. 建立虛擬環境（只需做一次）
python3 -m venv .venv

# 2. 啟動虛擬環境
source .venv/bin/activate

# 3. 安裝 MkDocs（只需做一次）
pip install -U mkdocs

# 4. 本地預覽
mkdocs serve
```

預設網址：http://127.0.0.1:8000

---

## 生成靜態網站

```bash
mkdocs build
```

輸出至 `site/` 目錄。可用任意靜態 server 開啟：

```bash
cd site
python -m http.server 8080
```

然後開啟 http://127.0.0.1:8080

---

## 注意事項

- `site/` 目錄已加入 .gitignore，不會被 commit
- `.venv/` 虛擬環境也不會被 commit
- 內容更新後需重新執行 `mkdocs serve` 或 `mkdocs build`

---

## 網站結構

- 首頁 → `docs/index.md`
- 閱讀指南 → `docs/reading-guide.md`
- 全域索引 → `docs/index-all.md`
- 各主題總覽 → `docs/topics/*.md`

原始內容位於根目錄的各資料夾（genres/, narrative-structures/, 等）。
