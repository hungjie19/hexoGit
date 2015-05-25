title: hexo new 文章後幫你開啟 MarkDown 編輯器
date: 2015-05-24 00:23:47
tags:
- Hexo
---

本篇就是來解決這樣的問題：
```
hexo new "我的新文章"
``` 
Commend Line 下完直接幫你開啟編輯器，直接撰寫文章！

<!--more-->

大家在新增完文章後的動作應該是會開啟 `Finder` 找到 Hexo 放置的資料夾然後至路徑 `Source/_posts` 找到剛剛新增的文章，在開啟 `Markdown` 編輯器或直接開 `Sublime Text` 撰寫文章，隨著文章變多找起來是相當不易，且動作也煩瑣。

[本文參考 liam0205](http://liam0205.me/2015/05/01/open-editor-after-hexo-new-immediately/)

1. 首先在 `hexo` 目錄下找到 `scripts` 資料夾如果沒有就新增一個囉！ 
2. 新增一個 `JavaScript` 檔案，加入下面的 `Sample code`
	* 示範開啟 `MacDown` 
	* 註解中示範的是 `Sublime Text`

### Sample Code:

```js
var exec = require('child_process').exec;

// Hexo 2.x
hexo.on('new', function(path){
    //exec('open -a "/Applications/Sublime Text.app" ' + path);
    exec('open -a "/Applications/MacDown.app" ' + path);
});
```

**原理:** 用 JavaScript 監聽 "new" event

[tommy351 commented on Jan 26](https://github.com/hexojs/hexo/issues/1007)

```js
You can try to listen to the new event. For example:

var spawn = require('child_process').spawn;

// Hexo 2.x
hexo.on('new', function(path){
  spawn('vi', [path]);
});

// Hexo 3
hexo.on('new', function(data){
  spawn('vi', [data.path]);
});
```

----

## Reference:

http://liam0205.me/2015/05/01/open-editor-after-hexo-new-immediately/
http://hexo.io/zh-tw/docs/plugins.html