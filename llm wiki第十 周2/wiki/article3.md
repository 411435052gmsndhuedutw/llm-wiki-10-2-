# RAG、課程證據與可追溯題目

## 為什麼從證據出題？

Retrieval-Augmented Generation（RAG）結合語言模型與檢索到的非參數知識。Lewis 等人的研究指出，對知識密集任務而言，模型知識存取、精確操作與決策來源等仍是重要挑戰。[S3](../raw/sources.md#s3--retrieval-augmented-generation-for-knowledge-intensive-nlp-tasks)

在本案例中，課程講義作為使用者提供的知識來源；題目不應只存答案，還需存能檢查答案的證據位置。

## 證據卡的最小欄位

| 欄位 | 用途 |
|---|---|
| `evidence_id` | 唯一識別 |
| `project_id` | 隔離不同課程 |
| `source_id` | 對應講義或網路來源 |
| `location` | 章節、頁碼或段落 |
| `claim` | 來源實際支持的概念 |
| `mode` | lecture 或 web supplement |

## 重要限制

檢索到相關段落，不代表答案一定正確；引用也可能錯誤對應。因此每題仍須檢查「題幹、正解、解說」是否都受到證據支持。

講義模式找不到依據時標示「講義未提及」。深入模式可以查可信公開來源，但外部內容需使用不同顏色、明確標籤和來源資訊，不得混成講義原文。

**來源：**[S3 — RAG](../raw/sources.md#s3--retrieval-augmented-generation-for-knowledge-intensive-nlp-tasks)
