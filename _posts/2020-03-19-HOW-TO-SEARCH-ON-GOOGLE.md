---
date: 2010-03-19 13:26:40
layout: post
title: how to search on google 
subtitle: searching 
description: Manually Searching OpenDirectories on Google
image: https://i.loli.net/2020/03/21/BfM8sPLt1QqyxdE.png
optimized_image: https://i.loli.net/2020/03/21/BfM8sPLt1QqyxdE.png
category: search
tags:
  - search
  - tips
  - book
author: deilt
---

# Manually Searching OpenDirectories on Google

此原文是reddit上的某个文章，看原文链接点击[这里](https://www.reddit.com/r/opendirectories/comments/933pzm/all_resources_i_know_related_to_open_directories/)

### 对于视频/电影/电视节目：

```
intext:"Search Term" intitle:"index.of" +(wmv|mpg|avi|mp4|mkv|mov) -inurl:(jsp|pl|php|html|aspx|htm|cf|shtml)
```

### 图片 ：

```
intext:"Search Term" intitle:"index.of./" (bmp|gif|jpg|png|psd|tif|tiff) -inurl:(jsp|pl|php|html|aspx|htm|cf|shtml)
```

### 音乐：

```
intext:"Search Term" intitle:"index.of./" (ac3|flac|m4a|mp3|ogg|wav|wma) -inurl:(jsp|pl|php|html|aspx|htm|cf|shtml)
```

### 书籍：

```
intitle:"Search Term" (pdf|epub|mob) "name or title" -inurl:(jsp|pl|php|html|aspx|htm|cf|shtml)
```

您也可以类似地找到Google Drive共享文件。
[shared floders](https://www.google.com/search?q=site%3Adrive.google.com+%2B%22drive%2Ffolders%22)
[Shared everything](https://www.google.com/search?q=site%3Adrive.google.com)
Works with other domains too.

有关google搜索运算符的一些信息可以在[这里](https://web.archive.org/web/20180729112702/https://moz.com/learn/seo/search-operators)找到

## 借助其他工具进行搜索
[Palined](http://palined.com/search/)
[The Eye](https://cgs.the-eye.eu/)
[SCRPED](http://scrped.com/)
[LENDX](http://lendx.org/)
[FileChef](http://www.filechef.com/)
[ewasion](https://ewasion.github.io/opendirectory-finder/)
[lumpySoft](https://lumpysoft.com/)
[EoJ OD.getter](https://www.eyeofjustice.com/od/)
[OD Search Tool](https://opendirsearch.abifog.com/)
[NMHDDS](https://doyou.needmorehdd.space/)
[Mattpalm](https://mattpalm.com/search/)
[Jimmyr](http://www.jimmyr.com/mp3_search.php)
[FilePursuit](https://filepursuit.com/)
[OD-Database](https://od-db.the-eye.eu/)
[Musgle](http://musgle.com/)
[Mamont's open FTP Index](http://www.mmnt.net/)
[NAPALM FTP Indexer](https://www.searchftps.net/)


# Java脚本
将以下代码另存为书签，然后可以打开书签以运行所需的操作。

下载具有特定扩展名的所有文件：

```
javascript:!function(){var%20t=prompt("Enter%20filetype%20to%20download%20(format:%20.mp3)");if(null!==t)for(var%20e=document.querySelectorAll('[href$="'+t+'"]'),o=0;o<e.length;o++)e[o].setAttribute("download",""),e[o].click();else%20alert("No%20format")}();
```

调整OD中“文件名”列的大小，以使整个文件名可见：

```
javascript:!function(){function e(e){var o,n,r=e.href;e.textContent=(n=(o=r).split("/").filter(Boolean).reverse()[0],console.log(n),o.lastIndexOf("/")==o.lenght-1&&(n+="/"),n=n.indexOf(" ")>=0?decodeURI(n):decodeURIComponent(n))}anchors=document.body.querySelectorAll("a"),anchors=Array.from(anchors).slice(1),anchors.map(e)}();
```

将图片显示为缩略图：

```
javascript:(function(){function%20I(u){var%20t=u.split('.'),e=t[t.length-1].toLowerCase();return%20{gif:1,jpg:1,jpeg:1,png:1,mng:1}[e]}function%20hE(s){return%20s.replace(/&/g,'&amp;').replace(/>/g,'>').replace(/</g,'<').replace(/"/g,'&quot;');}var%20q,h,i,z=open().document;z.write('<p>Images%20linked%20to%20by%20'+hE(location.href)+':</p><hr>');for(i=0;q=document.links[i];++i){h=q.href;if(h&&I(h))z.write('<p>'+q.innerHTML+'%20('+hE(h)+')<br><img%20src="'+hE(h)+'">');}z.close();})()
```

将图片显示为缩略图库：

```
javascript:var%20sHTML=%22<html><head><title>gallery</title><body><center><table%20border=0>%22;var%20y=0;for(x=0;x<document.links.length;x++){a=document.links[x].href;%20if%20(a.match(/jpe|jpeg|jpg|bmp|tiff|tif|bmp|gif|png/i)){sHTML+='<td%20style=%22border-style:solid;border-width:1px%22><a%20target=%22_new%22%20href=%22'+a+'%22><img%20border=%220%22%20width=%22100%22%20src=%22'+a+'%22></a></td>';%20if%20(!((x+1)%5))%20sHTML+=%22</tr><tr>%22}};this.innerHTML=sHTML+%22</table></center></body></html>%22;
```

眼睛图像查看器(The-Eye Image Viewer) :：

```
javascript:void(window.open('https://fusker.the-eye.eu/url.php?url='+encodeURIComponent(document.URL).replace(/\./g,'%25252E')));
```