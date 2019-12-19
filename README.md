# 自動點名系統Restful API

以 `Koa`、`koa-router`、`koa-body`、`koa-bodyparser` 實作該API。

## 下載

https://drive.google.com/drive/u/0/folders/1o8hbHh7M5Q7L3AQS9xsJurGhMhxd6rEz

## API介紹

總共有以下功能API:
1. 簡易測試用：
- search-user
    該API網址：http://localhost:3000/user/
    若要查詢使用者資料,可以在網址後面加入想要查詢的學號：
    http://localhost:3000/user/106360734
    回傳結果如下：
    ```
    {
    "account": 106360734,
    "password": "ianchen0119",
    "email": "iancodinghtml@gmail.com",
    "permit": 1,
    "name": "陳毅"
    ```
- search-user-all
    該API網址：http://localhost:3000/user/queryall
    該API可以直接獲得所有使用者的資料,回傳結果如下：
    ```
    [
    {
        "account": 106360728,
        "password": "abc0728",
        "email": "t106360728@ntut.edu.tw",
        "permit": 1,
        "name": "廖晨佑"
    },
    {
        "account": 123456,
        "password": "abc123456",
        "email": "htcunflrt@gmail.com",
        "permit": 0,
        "name": "tea"
    },
    {
        "account": 106360734,
        "password": "ianchen0119",
        "email": "iancodinghtml@gmail.com",
        "permit": 1,
        "name": "陳毅"
    },
    {
        "account": 106360718,
        "password": "abc0718",
        "email": "t106360718@ntut.edu.tw",
        "permit": 1,
        "name": "林家豪"
    },
    {
        "account": 106360824,
        "password": "abc111111",
        "email": "fbsgfbfd@gsfdb.co",
        "permit": 1,
        "name": "fuhebivo"
    },
    {
        "account": 106360729,
        "password": "molly880728",
        "email": "candies880728@gmail.com",
        "permit": 1,
        "name": "吳孟庭"
    },
    {
        "account": 106360798,
        "password": "abc0798",
        "email": "forfun@gmail.com",
        "permit": 1,
        "name": "陳毅"
    },
    {
        "account": 1063607108,
        "password": "abc07108",
        "email": "forfun@gmail.com",
        "permit": 1,
        "name": "陳毅"
    },
    {
        "account": 100718,
        "password": "0718",
        "email": "t10618@gmail.com",
        "permit": 1,
        "name": "林"
    }
    ]
    ```
2. 實作應用：
![https://ithelp.ithome.com.tw/upload/images/20191209/20110850gGm5Oy6Kl1.png](https://ithelp.ithome.com.tw/upload/images/20191209/20110850gGm5Oy6Kl1.png)
- login

該API提供登入功能,請使用GET方式做請求,相關傳送參數在此（Params）：

![https://ithelp.ithome.com.tw/upload/images/20191209/20110850fZwXLqm2MZ.png](https://ithelp.ithome.com.tw/upload/images/20191209/20110850fZwXLqm2MZ.png)
    
 該API網址：http://localhost:3000/login

 實際請求（結合參數）：http://localhost:3000/login?account=106360728&password=abc0728


    
- signup

 該API提供註冊功能,請使用POST方式做請求,相關傳送參數在此：
    
![https://ithelp.ithome.com.tw/upload/images/20191209/201108503OcNGKxpjq.png](https://ithelp.ithome.com.tw/upload/images/20191209/201108503OcNGKxpjq.png)
    
![https://ithelp.ithome.com.tw/upload/images/20191209/20110850GkLbnGgpAw.png](https://ithelp.ithome.com.tw/upload/images/20191209/20110850GkLbnGgpAw.png)

 該API網址：http://localhost:3000/signup
    
    

- mycourse

   該API提供查詢我的課程功能,請使用GET方式做請求,相關傳送參數在此：
    
![https://ithelp.ithome.com.tw/upload/images/20191209/20110850zKRlE124dD.png](https://ithelp.ithome.com.tw/upload/images/20191209/20110850zKRlE124dD.png)

   該API網址：http://localhost:3000/mycourse
   
- performance

   該API提供秀出指定課程的個人表現功能,請使用GET方式做請求,相關傳送參數在此：
    
![https://ithelp.ithome.com.tw/upload/images/20191209/20110850kI97EnsUce.png](https://ithelp.ithome.com.tw/upload/images/20191209/20110850kI97EnsUce.png)

   該API網址：http://localhost:3000/performance


- getcourse

    該API提供列出可選課程功能,請使用GET方式做請求。

    該API網址：http://localhost:3000/getcourse

- newcourse

    該API提供加選課程功能,請使用POST方式做請求,相關傳送參數在此：

![https://ithelp.ithome.com.tw/upload/images/20191209/201108503OcNGKxpjq.png](https://ithelp.ithome.com.tw/upload/images/20191209/201108503OcNGKxpjq.png)
    
![https://ithelp.ithome.com.tw/upload/images/20191209/20110850kCCkSQAu7l.png](https://ithelp.ithome.com.tw/upload/images/20191209/20110850kCCkSQAu7l.png)

    該API網址：http://localhost:3000/newcourse

## 快速開始

在了解相關參數及設定後,我們可以透過以下步驟開啟該API server。

下載並解壓縮後,實施以下步驟：

```bash
cd api
npm install
node server_db.js
```

## 使用Postman測試API

1.請先至Postman官網下載該程式

[官網](https://www.getpostman.com/)

2.使用import把下載下來的api資料夾內的`自動點名系統.postman_collection.json`導入

![https://ithelp.ithome.com.tw/upload/images/20191209/20110850o2ENyvshfb.png](https://ithelp.ithome.com.tw/upload/images/20191209/20110850o2ENyvshfb.png)

3.導入後,我們會發現collection內出現自動點名系統資料夾,而該資料夾內有針對各支API的測試檔可供使用。

![https://ithelp.ithome.com.tw/upload/images/20191209/201108504j8xdRzrYQ.png](https://ithelp.ithome.com.tw/upload/images/20191209/201108504j8xdRzrYQ.png)

## 聲明

本專案僅提供畢業專題同組員使用


