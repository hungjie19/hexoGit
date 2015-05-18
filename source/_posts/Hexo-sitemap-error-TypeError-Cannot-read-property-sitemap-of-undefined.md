title: "Hexo sitemap [error] TypeError: Cannot read property 'sitemap' of undefined"
date: 2015-05-16 11:20:54
tags: 
- Hexo
- sitemap
---

![sitemap ［error］ Cannot read property 'sitemap' of undefined](https://googledrive.com/host/0B4fEFbbW93y5TloxVTZSbU5wbEE)

<!--more-->

## 版本：

* Hexo 2.8.3

將原本 `hexo-generator-sitemap Plugin` 修改成以下版本既可。

``` bush
$ npm uninstall hexo-generator-sitemap
$ npm install hexo-generator-sitemap@0.2.0 --save
```

### _config.yml

``` bush
sitemap:
    path: sitemap.xml
```

-----

Reference :
[When I use the plugin, I can't deploy my blog with error #10](https://github.com/hexojs/hexo-generator-sitemap/issues/10)
[hexo-generator-sitemap](https://github.com/hexojs/hexo-generator-sitemap)




