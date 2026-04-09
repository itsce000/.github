# 全域開發規範 (Global Development Standards)

## .NET 與 C# 規範
- 統一使用非同步程式設計模式 (Task-based Asynchronous Pattern)。
- 所有的資料存取層必須處理連線生命週期，優先使用 'using' 宣告。

## 資料庫與交易 (SQL Server)
- 執行多步驟更新時，必須明確檢查 SqlTransaction 是否已正確 Begin、Commit 或 Rollback。
- 避免在查詢中使用 SELECT *，必須明確指定欄位。

## 紀錄檔與錯誤處理 (Logging & Error Handling)
- 專案統一使用 NLog 進行紀錄。
- 禁止在 Production code 中留下 Console.WriteLine。
- 在 Catch 區塊中必須至少紀錄一筆 Error Level 的 Log 並包含 Exception 內容。
