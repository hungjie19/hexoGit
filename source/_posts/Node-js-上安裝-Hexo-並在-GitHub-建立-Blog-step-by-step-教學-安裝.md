title: Node.js 上安裝 Hexo 並在 GitHub 建立 Blog step by step 教學-安裝
date: 2015-05-08 08:06:37
tags: Hexo 
---

![Hexo](https://googledrive.com/host/0B4fEFbbW93y5dVZoRTBCbjJEVHc)

> A fast, simple & powerful blog framework powered by Node.js.

<!--more-->

# Why Hexo ?

* 使用 [Hexo](http://hexo.io/) 建立個人 Blog 的好處有以下：
	1. 使用 [Node.js](https://nodejs.org/) 環境建立
	2. 使用 [NPM](https://www.npmjs.com/) 管理套件安裝
	3. 使用 [Markdown](http://zh.wikipedia.org/wiki/Markdown) 語言快速編輯，筆記、Blog 一次搞定。
	4. 文章裡面可以放上 `Code` 並加上 [highlight.js](https://highlightjs.org/static/demo/) 高亮語法顯示。
	5. 可使用 [GitHub](https://github.com/) 版本管理 / 備份
	6. 最後可以直接發佈到 [GitHub Page / GitHub.io](https://pages.github.com/)

根據以上多種優點，因此建立一個 **Hexo Blog Project** 可以一次學習到多種工具與管理套件，因此也成為我買下 MBPR 後第一個想要玩的技術，接著就直接進入主題。

---

## 環境介紹

系統|版號
----|-----
MBPR|2015
OSX|10.10.2
Hexo|2.8.3
node.js|v0.12.2

## 安裝 hexo 2.8.3 版本

如果安裝過程出現 **"權限錯誤"** 可以試著在命令前加上 `sudo`

### 解除安裝 hexo
``` bash
npm uninstall hexo
```

### Step.1 安裝 hexo 2.8.3 版本
``` bash
npm install hexo@v2.8.3 -g
```

### Step.2 建置 hexo 存放資料夾

``` bash
XXX = 自訂資料夾名稱 ex: hexo
mkdir XXX
```

### Step.3 移動到 hexo 存放資料夾
```
cd XXX
```

### Step.4 初始化
``` bash
hexo init
npm install
```

### Step.5 hexo 2.8.3 Plugin
``` bash
npm install hexo-renderer-marked@0.1 --save
npm install hexo-renderer-stylus@0.1 --save
```

## 檢查是否完成安裝
1. 在 `node_modules` 資料夾下面有與 plugin 同名資料夾。
2. `package.json` 中有以下資料 :

``` json
{
    "hexo-renderer-marked": "0.1",
    "hexo-renderer-stylus": "0.1"
}
```

### Step.6 在主機上啟動 Server
``` bush
hexo server
```

> 現在開啟瀏覽器在網址列輸入以下就可以看到預設的 Hello Page 囉！！

``` bash
localhost:4000
```

是不是很酷呢?!!

------

####Reference:
[Hexo Twitter](https://twitter.com/hexojs?lang=zh-tw)

* http://hexo.io/zh-tw/docs/
* https://github.com/hexojs/hexo/issues/1094
* http://pagent.github.io/2015/03/14/hexo-283-install/
