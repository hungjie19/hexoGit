title: Hexo depoly to GitHub
date: 2015-05-08 22:29:57
tags:
- Hexo

---

#目標：
1. 新增一篇文章
2. 上傳到Github

<!--more-->

----

#實作：

##為你的 Blog 新增一篇文章

``` bush
hexo new "Name"
```

如果文章有空格需要用 `" "` 將名稱包起，

編輯 `.md` 檔案可以使用 `MacDown` 軟體編輯，

編輯期間可使用以下命令檢視呈現結果：

``` bush
hexo server
 or
hexo s

查看：localhost:4000 
```

## push in GitHub

1. 申請一個GitHub帳號
2. new repository  `ex: Blog`

## 編輯 _config.yml file

``` yml
deploy:
  type: github
  repository: https://github.com/帳號/名稱.git
  branch: gh-pages
```
其實 repository: `HTTPS clone URL` !!

## 產生靜態檔
``` bush
hexo generate
 or 
hexo g
```

## 提交至GitHub
``` bush
hexo deploy
 or 
hexo d
```

### 最後commend line 要求
```
Username:
Password:
```

#現在快到GitHub Page 看看吧!!

帳號.github.io/名稱
