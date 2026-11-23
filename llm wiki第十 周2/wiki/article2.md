# ReAct 與題目級 Loop

## ReAct 的概念

ReAct 研究將推理軌跡與任務行動交替產生；行動能連接外部資訊來源，觀察結果再影響後續決策。[S2](../raw/sources.md#s2--react-synergizing-reasoning-and-acting-in-language-models)

對互動式測驗來說，可轉成較容易檢查的題目級迴圈：

```text
取一張證據卡
→ 產生一道選擇題
→ 核對正解、干擾選項與來源
→ 顯示題目、等待學生作答
→ 回饋或補強
→ 下一題，或將錯題存入複習集
```

## Loop 做什麼、不做什麼

- Loop 負責重試或修正**當前題目**，不應讓一題的錯誤重跑整個課程題庫。
- 證據不足時，回到資料擷取或標示「未提及」，不可用模型常識補洞。
- 答錯後由學生選重練或跳過；跳過是有效選擇，不是失敗懲罰。

## 邊界

ReAct 描述的是推理、行動與觀察互相配合的模式，不保證生成內容正確。每題仍需獨立查證來源。

**來源：**[S2 — ReAct](../raw/sources.md#s2--react-synergizing-reasoning-and-acting-in-language-models)
