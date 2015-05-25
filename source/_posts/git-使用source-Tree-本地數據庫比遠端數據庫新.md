title: git 使用source Tree 本地數據庫比遠端數據庫新
date: 2015-05-25 22:07:38
tags:
- Git
---

情況：用 GitHub repository 做 Hexo Blog 的版控兼遠端儲存庫，方便用第二台電腦寫部落格時候環境一致。

狀況與目的：

1. 本地電腦已用 `git command line` 命令提繳至 github
2. 將專案用 source Tree 開啟
3. 將專案 commit 並 push to github

<!--more-->

註：目前還是 git 新手因此這問題困擾我一陣子，所以做個筆記 :-)

最初是因為不太懂為什麼 `clone` 時一直噴錯說我選的資料夾不是一個空的而且已經是 git（因為要先 git init），所以重練直接用 command line 下 git 指令將整個 hexo 環境提交上 github 但是覺得還是用 `source Tree` 的 GUI 還是比較清楚，所以在 google 無所獲＋亂按之下不小心完成..以下是步驟：（說明或步驟有錯也請告訴我，謝謝感恩）


### 選擇本地專案資料夾：
![add Repository -> Create Repository](https://googledrive.com/host/0B4fEFbbW93y5RXRnZ2xyV3ppT3M)

### 因為本地專案資料比遠端新，所以直接提交一個 commit
![Dsitemap 提交至 Google 網站管理員](https://googledrive.com/host/0B4fEFbbW93y5cTZRUzZKRm1JVE0)

### 這邊 Commit mode 我選擇是 selected files(文件)

嘗試用預設的 `Staged changes` 並無法讓我成功提交，可能是因為 `hexo` 增加一篇文章就是一個 `.md` 檔案。

![Commit mode](https://googledrive.com/host/0B4fEFbbW93y5OWRFU3FlMmdjdWc)

### commit 後接著 `Push` 就完成了！

註：因為一開始就使用 `command line` 流程將專案提繳到 github 上去過，因此用 source Tree 操作 `Push` 時已經幫我把遠端網址帶入，所以就沒有補這部分流程了 sorry。
