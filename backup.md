自動備份(Commandline+工作排程器)

手動備份(GUI介面)

MongoDB Command Line Database Tools Download

https://www.mongodb.com/try/download/database-tools

下載解壓縮複製bin貼上C:\Program Files\MongoDB

bin改名Command Line Database Tools

C:\MondoDBBackup 路徑欄位輸入cmd

C:\MondoDBBackup>"C:\Program Files\MongoDB\Command Line Database Tools\mongodump.exe"

C:\MondoDBBackup>"C:\Program Files\MongoDB\Command Line Database Tools\mongorestore.exe"

C:\MondoDBBackup>dir 磁碟區 C 中的磁碟是 Windows 磁碟區序號: 789C-4BD5

C:\MondoDBBackup 的目錄

2025/04/13 下午 03:28

. 2025/04/13 下午 03:28 dump 0 個檔案 0 位元組 2 個目錄 385,646,141,440 位元組可用

📦 舉個例子：
你可以把 mongodump 想成：

「我把 MongoDB 裡面的東西撈出來（傾印出來）儲存在另一個資料夾，作為備份。」

相對的：

mongorestore 則是把你備份的資料「倒回去」

備份指令（dump）

"C:\Program Files\MongoDB\Command Line Database Tools\mongodump.exe" --uri="mongodb://localhost:27017/MyDB" --out="C:\MondoDBBackup\dump"


你用這條指令成功還原了資料：

"C:\Program Files\MongoDB\Command Line Database Tools\mongorestore.exe" --uri="mongodb://localhost:27017" --drop --dir="C:\MondoDBBackup\dump"


-----------------------------------------------------------------------------------------------

工作排程器-建立工作
