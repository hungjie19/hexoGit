title: '快速上手 Parse & 前端測試神器 Selenium 雙主題初體驗'
date: 2015-05-19 19:35:49
tags:
- workshop
- Testing
---
![Parse & Selenium 台南-好想工作室](https://googledrive.com/host/0B4fEFbbW93y5RTNHenpXYW1ReTg)

<!--more-->

# 1.快速建立前端的利器 Parse Cloud Code 介紹

{% iframe http://www.slideshare.net/slideshow/embed_code/key/pHzkGR0bIkzy47 425 355 %}

新創公司趕著把點子推出去，可是缺乏架構工程師，因此使用 Parse 就可以省去這些麻煩，將所有專案建置到雲端上，因此就可以全力專注在產品開發上面。

### 提供非常多的功能
* Cloud code
* Data
	* SQL API
	* CRUD
	* 關連式資料
	* ACL (安全性限制)
* Push 通知
	* iOS
	* Andorid
	* win / 8
* Analyics
	* 錯誤回報
* Social USER Login
	* 註冊
	* 登入
	* email 驗證
* Hosting
	* 提供 subdomain.Parseapp,com
	* 自訂
	* 後台 log、error
	* 背景排程

## Parse 建置網站

* 註冊
* ACL 設定 權限
* 下載 console
* Programming Language
	* 原生 JavaScript
	* parse SDK
* 其他功能
	* Email 樣板罐頭簡訊可以自動回覆 USER
	* 忘記密碼，找回密碼

## Parse.Object
* Parse會自動替每一筆資料產生欄位
	* id
	* createdAt
	* updatedAt
	
> 上述欄位前面加上`Obj.` 可以直接取得 value

# Demo

* 一個吃貨網站
	* 登入 CRUD 
	* 登出 唯讀
	* 新增地點
	* 串接 google Map API

## 結論 & 討論

1. parse 可以讓小型新創團隊直接專注產品開發
2. 後端 debug 不易
3. 產品將會綁在 parse 上..
4. 已被 FaceBook 買走
5. 另一套 FileBase
6. 練習寫 app
7. 是一個當 Prototype 的好工具 ?
8. 無法在本機 debug 必須 deploy 上 server..
9. AWS ?  
10. Heroku ? 沒有 DB API 需要自己建立

--------

# 2. 前端測試神器 Selenium

{% iframe http://www.slideshare.net/slideshow/embed_code/key/ziFjTib3QOb1RY 425 355 %}

# What is Selenium
* 整合性測試
* UI 黑箱測試 - 自動化測試
* Selenium ＝ 自動化啟動瀏覽器
* 腳本語言支援：非常多

## How to use ?

* Selenium IDE
	* install JAVA SDK
	* npm 可以安裝
	* 安裝瀏覽器 plugin
* Selenium RC
* 測試多種平台
	* BrowserStack
	* etc..
* Selenium Grid (實際硬體測試)
	* 建置一台 Hub 串接實體設備，透過網路溝通，幫你做自動測試
	* 設備要安裝 cline 端窗口設定 Listener (IP, Port..)

```
Q、問題是 JavaScript 具有 Asynchronous 
非同步特性因此無法按照我們寫的腳本 1 > 2 > 3 照順序做 ??

A : Selenium 運用Control Flow 方法解決
因此只要照正常想法一步一步寫好腳本 Selenium 會幫你解決這塊問題!!
```

## WebDriverJS for Node.js

* 站在巨人肩膀 use Node.js NPM 
* WebDriver IO (web Testing)
* Nightwatch.js (new)
* Protractor (AngularJS)
	* Protractor Testing DEMO

> 所以.. 我們有更快的方法嗎？

## a Single Command (一行指令夠快嗎？)

### Gulp.js
* 前端工程師的好朋友
* 自動化工具
* 可以幫你截圖
* 具有 log 擋

```
gulp test 
```

