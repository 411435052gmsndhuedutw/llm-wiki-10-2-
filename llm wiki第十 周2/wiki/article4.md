# Graph：用 State、Nodes、Edges 管理流程

## 三個基本元素

LangGraph 文件以共享狀態（State）、節點（Nodes）與邊（Edges）描述 Graph：節點執行工作，邊決定後續路徑；邊可固定或條件式，並支援序列、分支及迴圈。[S4](../raw/sources.md#s4--langgraph-graph-api-overview)

## 對應到課程測驗 Agent

- **State：**目前課程專案、講義清單、模式、範圍、題目、作答、錯題 ID。
- **Nodes：**讀取講義、建立證據卡、產生題目、驗證題目、呈現測驗、批改、存錯題、匯出。
- **Edges：**控制正常前進，以及資料不足、題目驗證失敗、答錯重練或跳過等分流。

## 圖比單一 Loop 更合適的地方

專案管理、雙資料模式、兩種回饋模式、錯題保存與匯出，各有不同輸入與檢查標準。Graph 讓這些選擇與回退路線在執行前就可讀、可檢查；每個節點內仍可保留小型 Loop。

**來源：**[S4 — LangGraph Graph API](../raw/sources.md#s4--langgraph-graph-api-overview)
