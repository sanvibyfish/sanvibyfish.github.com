---
layout: post
title: "sublime text 3"
description: ""
category: ""
tags: []
comments: true
---

###安装Package Control
我们可以很简便的去安装***Package Control***，可以使用快捷键***ctrl+`***或者在菜单上 ***View > Show Console***，然后在控制台键入如下代码

```
import urllib.request,os,hashlib; h = '7183a2d3e96f11eeadd761d777e62404e330c659d4bb41d3bdf022e94cab3cd0'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```
更多相关的资讯可以查看
[查看更多](https://sublime.wbond.net/installation)

###插件

####Emmet html/CSS快速编辑（原名Zen Coding）

Zen Coding估计大家都不会陌生，前不久改名为Emmet了，虽然用Emmet编辑html很快，但是要用好用快它需要付出不小的学习成本，学习的曲线有点陡峭，以至于让新手好奇而畏惧，我看看热闹就行了，感觉编辑得再快思维跟不上也是白搭，对我来说sublime text 3自带的代码提示够用了。网上有很多教学视频，有兴趣学习的可以去了解下。

![Emmt](http://img.hb.aicdn.com/e413abeb1bed993da92812c035da2d1736b8f38a1eb7b-QOvdcI_fw658)

插件下载：[https://github.com/sergeche/emmet-sublime](https://github.com/sergeche/emmet-sublime)

####Better CoffeeScript

CoffeeScript 的语法高亮，编译，命令等
插件地址: [https://github.com/aponxi/sublime-better-coffeescript](https://github.com/aponxi/sublime-better-coffeescript)

####Sublime CodeIntel

Sublime CodeIntel是我最喜欢的插件，它提供了很多IDE提供的功能，例如代码自动补齐，快速跳转到变量定义，在状态栏显示函数快捷信息等。

它支持的语言有：PHP, Python, RHTML, JavaScript, Smarty, Mason, Node.js, XBL, Tcl, HTML, HTML5, TemplateToolkit, XUL, Django, Perl, Ruby, Python3.

虽然有时候有点小问题，但真的能节省很多时间。强烈推荐安装。
![Sublime CodeIntel](http://img.hb.aicdn.com/b453b5b834f0219599ee2cabaeb4be0cd20f52f77500-BA2JWN_fw658)
插件地址: [https://github.com/Kronuz/SublimeCodeIntel](https://github.com/Kronuz/SublimeCodeIntel)