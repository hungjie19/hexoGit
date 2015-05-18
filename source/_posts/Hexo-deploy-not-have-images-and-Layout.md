title: Hexo deploy not have images and Layout
date: 2015-05-09 10:55:18
tags: Hexo
---

![到 github.io 看到 deploy 後畫面](https://googledrive.com/host/0B4fEFbbW93y5eXJSektaSXd2QXc)

## 情況：

* 成功 deploy
* 沒有 Image
* 沒有 Layout

## 解：

###_config.yml 設定
` : 分號前面記得加空格 `

``` bush
url: http://帳號.github.io/名稱
root: /名稱/
```