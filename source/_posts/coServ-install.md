title: coServ install
date: 2015-03-11 12:44:33
tags:
- coServ
- workshop
- nodeJS
---
![coServ](https://googledrive.com/host/0B4fEFbbW93y5TjMzT2xINlh4dzA)

<!--more-->

系統|版號
----|-----
MBPR|2015
OSX|10.10.2
coServ|0.9.6
node.js|v0.12.2

* 開始之前，請先安裝以下環境：
	* [Node.js](https://nodejs.org/)
	* [NPM](https://www.npmjs.com/)

# install coServ

### 1、利用 npm 幫我們安裝 coServ

``` bash
sudo npm install coserv
```
### 2、檢查安裝 / 移動

安裝完成後會在 `node_modules` 資料夾下面，產生一個同名檔案 `coServ` 
因此我們要移動至資料夾進行網站開發。

``` bash
cd node_modules/coserv
```

### 3、測試，啟動 `coServ`

```bash
node coserv
```

### 4、執行後不會有任何反應，請到瀏覽器觀看：

``` bash
http://127.0.0.1:8080
```

> 注意！在coServ 中 localhost 不等於 127.0.0.1 
> 因此請用預設 127.0.0.1 觀看頁面

### 建立一個新網站

```bash
node cli/addSite yourNewSite
```
### 建立一個新頁面
```bash
node cli/addPage yourNewSite yourNewPage
```
