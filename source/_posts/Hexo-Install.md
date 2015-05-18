title: Hexo install
date: 2015-05-08 08:06:37
tags: Hexo 
---

##Why Hexo ?

使用 Hexo 建立 Blog 的好處有以下：

* 文章裡面可以放上 Coge 並加上 highlight 高亮語法顯示。
* 使用 markdown 語言快速編輯，筆記、Blog 一次搞定。
* 可建立於 GitHub
* 使用 Node.js 建立

<!--more-->

根據以上多種好處．因此建立 **Hexo Blog** 成為我敗下 MBPR 後第一個想要玩的技術，直接進入主題。

##環境介紹

系統|版號
----|-----
MBPR|2015
OSX|10.10.2
Hexo|2.8.3
node.js|v0.12.2

##安裝hexo2.8.3版本

如果安裝過程出現**權限錯誤**，須在命令前加上`sudo`

###解除安裝hexo
``` bash
npm uninstall hexo
```

###安裝2.8.3版本
``` bash
npm install hexo@v2.8.3 -g
```


### 建置hexo存放資料夾
``` bash
mkdir [filename]
cd [filename]
```

### 初始化
``` bash
hexo init
npm install
```

###如果無法安裝請嘗試以下命令
``` bash 
npm install -g -unsafe-perm hexo
```

##hexo 2.8.3 plugin
``` bash
npm install hexo-renderer-marked@0.1 --save
npm install hexo-renderer-stylus@0.1 --save
```

##檢查是否完成安裝
1. 在 `node_modules` 資料夾下面有與 plugin 同名資料夾。
2. `package.json` 中有以下資料 :

``` json
{
    "hexo-renderer-marked": "0.1",
    "hexo-renderer-stylus": "0.1"
}
```

###在主機上啟動 Server
``` bush
hexo server
```

###現在開啟瀏覽器在網址列輸入以下就可以看到預設的 Hello Page 囉！！
``` bash
localhost:4000
```

------

####Reference:

* http://hexo.io/zh-tw/docs/
* https://github.com/hexojs/hexo/issues/1094
* http://pagent.github.io/2015/03/14/hexo-283-install/
