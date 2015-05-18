title: Hexo add DISQUS Comments 新增留言板
date: 2015-05-12 09:30:24
tags: 
- Hexo
- DISQUS
---

![新增 DISQUS 留言板](https://googledrive.com/host/0B4fEFbbW93y5RFczVENiaS1oYlE)

<!--more-->

# DISQUS

Hexo 本身內建 [Disqus](https://disqus.com/) 是一款專門針對部落格、網站留言機制做統合的服務，使用者想要留言可以匿名、DISQUS會員、Facebook帳號、Twitter帳號、Google帳號進流網站留言，同時這套留言機制可以幫你統計訪客留言排行榜，另外在留言下方也可以最近被熱門討論的文章，此外也可以透過本身的分享機制把文章分享出去，並且留言機制中支援階層式(巢狀式)留言。[引用：香腸炒魷魚](http://sofree.cc/disqus/)

因此我們將在 Blog 中新增 DISQUS 留言板，步驟如下：

1. 申請帳號
2. 新增頁面
3. 記下 **shortname**
4. 選擇外掛可以不須理會

![DISQUS shortname 簡單步驟](https://googledrive.com/host/0B4fEFbbW93y5LXNwYlZNLXpjb0k)

#Hexo _confid.yml

```bush
# Disqus
	disqus_shortname: yourShortname

```

----

#參考

http://sofree.cc/disqus/

http://morris821028.github.io/2014/04/12/web/hexo-comment/

http://code.kpman.cc/2013/04/28/%E5%AE%A2%E8%A3%BD%E5%8C%96hexo-light-theme/
