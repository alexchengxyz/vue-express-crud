# Node Express + MongoDB + Mongoose

## 啟用資料庫

執行以下指令後 docker-images 資料夾底下會生成 database 資料夾，這是掛載資料庫用的。
container 停止或刪除 database 一樣會保留資料。

```bash
cd backend/docker-images
docker-compose up -d
docker-compose stop #關閉所有 container
docker-compose ps # 查看是否啟用
docker ps # 查看啟用的 container
```

## 安裝 MongoDB Compass 並新增資料庫

1. 預設資料庫路徑: mongodb://localhost:27017/VueExpress
2. 安裝 MongoDB Compass 連結資料庫並新增資料庫和collection

- 資料庫名稱: VueExpress
- collection: users

## 設定 env 參數

請新增 .env 並加入以下參數
PORT=8000
MONGO_URI='mongodb://localhost:27017/VueExpress'

## 啟動 API

```bash
npm run devServer
```

## api 路徑、資料結構

1. models> Users.js 可瀏覽資料結構
2. app.js 可瀏覽api 路徑

## 建議用 PostMan 瀏覽以下api

- get: /api/v1/users/list
- post: /api/v1/users
- put: /api/v1/users/:id
- deleted: /api/v1/users/:id

## 筆記

___

## Mongo 指令

```bash
# 更改 collection 名稱
db.collection.renameCollection()

# 刪除 collection
db.collection.drop()
```
