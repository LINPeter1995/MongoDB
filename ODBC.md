# 實務情境

假設你公司原本用 MySQL 存會員資料，但現在要改用 MongoDB 儲存使用者行為紀錄或訂單資料，你就可以：

用 ODBC 從 MySQL 撈資料（例如：使用者帳號、訂閱資訊）

搭配 ETL 工具轉成 JSON 文件

寫入 MongoDB

https://dev.mysql.com/downloads/connector/odbc/
