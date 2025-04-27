# 在 VSCode 中連接到 MongoDB Atlas

Cluster-Connect-Compass-Copy the connection string, then open MongoDB Compass

Use this connection string in your application

mongodb+srv://Peter:<db_password>@cluster0.lobr68x.mongodb.net/

from pymongo import MongoClient

uri = "mongodb+srv://Peter:Peter@cluster0.lobr68x.mongodb.net/"

client = MongoClient(uri)

db = client.FullTextDB
collection = db.LodgingCollection

pipeline = [
    {
        "$search": {
            "index": "ixLodging",  # Replace with your index name if different
            "text": {
                "query": "Downtown",
                "path":{
                    "wildcard": "*"     
                }
            }
        }
    }
]

results = collection.aggregate(pipeline)

for doc in results:
    print(doc)

--------------------------------------------------------------------------------------------------------------------------------------------

下载并安装 MongoDB Atlas Power BI Connector

下载连接器文件。

https://www.mongodb.com/try/download/power-bi-connector

Power BI Connector Download-Download

将连接器文件移至以下目录路径：C:\Users\<user>\Documents\Power BI Desktop\Custom Connectors。

如果这个文件夹不存在，请创建。

--------------------------------------------------------------------------------------------------------------------------------------------

# SQL Query

Atlas-Project-Clusters-Atlas SQL/Connect-Copy Database Name + Copy URL

Database Access-Edit-Edit Password

-------------------------------------------------------------------------------------------------------------------------------------------

# Power BI Desktop

取得資料-其他-收尋atlas-連接-繼續-輸入MongoDB URL、Database匯入資料
