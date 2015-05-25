title: coServ 開發小幫手使用 gulp 實踐 Live Reload
date: 2015-05-24 15:01:54
tags:
- coServ
- gulp
- Live Reload
---
![coServ + gulp 實踐 Live Reload](https://googledrive.com/host/0B4fEFbbW93y5RVh2cjFKa1R0eU0)

<!--more-->

本篇參考 [youTobe by Ben Lue](https://www.youtube.com/watch?v=swQ5pVxDHwo)

### 開始之前
* [install coServ](http://www.coservjs.org/)
* [也可以參考之前的coServ安裝心得](http://hungjie19.github.io/hexoblog/2015/03/11/coServ-install/#more)

## install Tools

### gulp
```
 npm install gulp
```
### browser-sync
```
sudo npm install browser-sync
```	

以上完成後在 coServ 資料夾中產生 `gulpfile.js` 內容：

```js
var  browserSync = require('browser-sync'),
     gulp = require('gulp'),
     config = require('./lib/server/config.js'),
     coServ = require('./coServ');

// deal with the www path
var  reload = browserSync.reload,
     wwwPath = config.getWWW();

gulp.task('default', function() {
    browserSync({
        proxy: '127.0.0.1:8080'
    });

    gulp.watch(['./**/*.html', './**/*.css', './**/*.js', './**/*.inc', './**/*.lang'],
        {cwd: wwwPath}, reload);

    gulp.watch(['./themes/*/blocks/modules/**/*.js'], {cwd: wwwPath}, function(e) {
        coServ.restart();
    });
});
```
	
最後原本啟動 server 命令為：

```
node coserv
```

現在有了 `gulp` 的幫忙直接啟動它，就會幫我們開啟網頁與監聽檔案變動，即時的幫你更新網頁修改畫面！

```
gulp
```

----

### gulp issue [參考](https://laracasts.com/discuss/channels/elixir/bash-gulp-command-not-found)

Command Line : `gulp` 發生以下回應：

```
command not found: gulp
```

### 將 gulp 改全域安裝的方式，以下：
```
npm install --global gulp
npm install
```