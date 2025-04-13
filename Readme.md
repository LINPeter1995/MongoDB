停用自動登入

Add new connection

Advanced Connection Options

Authentication

Open MongoDB shell

use admin

db.createUser({user:"MongoDBAdmin", pwd: "Password_1", roles:[{role: "userAdminAnyDatabase", db:"admin"}]})

--------------------------------------------------------------------------------------------------------------------

MongoServerError[Location51003]: User "MongoDBAdmin@admin" already exists

use admin

db.dropUser("MongoDBAdmin")

true

---------------------------------------------------------------------------------------------------------------------

編輯C:\Program Files\MongoDB\Server\8.0\bin\mongo.cfg

轉存mongo.cfg再存回

加入 #security:
security:
  authorization: enabled

儲存

重啟mongod.exe(手動啟動,重啟服務)

控制台\系統及安全性\Windows 工具
服務-MongoDB Server 重啟
工作排程器(常常用)

MongoDB Shell(命令式介面)

CLI(Command Line Interface)

Atlad CLI

