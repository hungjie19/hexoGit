title: Hexo livereload
date: 2015-05-14 23:24:06
tags: Hexo
---

# Live Reload

減少網頁開發中常按 command + R 的情況，監聽文件更動既幫你 Reload 的開發好幫手。

[hexo-livereload Github](https://github.com/hexojs/hexo-livereload)

[livereload 官網](http://livereload.com/)

<!--more-->

## install node.js livereload

``` bash
$ sudo npm install -g node-livereload
```

## install hexo-livereload
``` bash
$ sudo npm install hexo-livereload --save
```
## install browser extensions

[Chrome 商店下載 LiveReload](https://chrome.google.com/webstore/detail/livereload/jnihajbhpnppcggbcgedagnkighmdlei)

[Firefox extension 2.1.0](http://download.livereload.com/2.1.0/LiveReload-2.1.0.xpi)

[官方連結](http://livereload.com/extensions/)

### _config.yml
``` bash
livereload:
	port: 35729
```

安裝完成！！

接下來只要啟動，就可以即時監看

``` bash
hexo s
```

##小提醒！！

hexo server 啟動後一樣到 `localhost:4000` 就可以看到即時 `reload` 的頁面了。

千萬不要像我這麼笨，開開心心去 `localhost:35729` 傻傻的研究30幾分鐘，爬了很多文只有一篇特別提醒...Orz..。 
