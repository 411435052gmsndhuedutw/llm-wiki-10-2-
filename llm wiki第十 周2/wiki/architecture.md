# 系統架構與檔案導覽

## 檔案結構

```text
專案根目錄
├─ AGENTS.md                  # Wiki 與簡報的編輯和查核規則
├─ index.html                 # 專案入口頁（成果導覽，不是測驗應用）
├─ css/style.css              # 像素 RPG 視覺樣式
├─ js/app.js                  # 舊版佔位檔；目前入口頁未載入
├─ raw/sources.md             # 五項來源的 Ingest 紀錄
├─ wiki/
│  ├─ index.md                # Wiki 目錄
│  ├─ overview.md             # 主題、讀者與用途
│  ├─ architecture.md         # 專案架構
│  ├─ article1.md             # Agentic workflow
│  ├─ article2.md             # ReAct 與題目級 Loop
│  ├─ article3.md             # RAG 與來源依據
│  ├─ article4.md             # Graph 的 State / Nodes / Edges
│  ├─ article5.md             # Agent 測試與追蹤
│  ├─ evidence-cards.md       # 證據卡與示範題
│  ├─ study-notes.md          # 考前重點整理示範
│  ├─ workflow.md             # 學習 Agent 的 Graph / Loop 規格
│  ├─ user-guide.md           # 使用目標系統的流程圖與說明
│  └─ log.md                  # 執行、檢查與反思
├─ slides/presentation.html   # 互動式教學簡報
└─ submission.md              # 作業繳交摘要
```

## 目標系統的資料邊界

此架構描述的是設計案例，不代表本專案已實作上傳、出題、儲存或 AI 服務。

- 一個課程專案保存上傳講義／簡報或可讀取連結、範圍設定、題庫與錯題集。
- 講義模式的答案必須能回指講義證據。
- 深入模式可補充網路資訊，但需有獨立標籤、明顯顏色與來源說明。
- 錯題庫按課程隔離；跳過題目後保留題目、作答、正解、來源與錯誤概念。
- 目標系統可匯出考前重點、題目集與錯題集 PDF；本作業未實作匯出服務。

詳細流程與錯誤退回路線見 [workflow.md](workflow.md)；使用者操作順序見 [user-guide.md](user-guide.md)。

## 保留的舊檔案

`js/app.js`、`data/timetables/template.json` 和 `extra/README.md` 是早期範本留下的檔案，目前不屬於 Study Quest 網站，也沒有被入口頁載入。為避免誤刪其他用途的資料，先保留；除非使用者要求，不要把新功能放進這些檔案。
