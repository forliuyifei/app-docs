---
title: 搜索 Lite
type: docs
date: 2020-12-26 23:18:15
update: 2020-12-26 23:18:15
description: Search the world !
---

### 安装
[前往酷安下载](https://www.coolapk.com/apk/com.orekie.search)

### URL 收集

A. **跳转浏览器搜索**
1. 搜索引擎
   - 夸克
   https://quark.sm.cn/s?q=%s
   - Magi
   https://magi.com/search?q=%s
   - 秘迹搜
   https://m.mijisou.com/?q=%s

2. 翻译引擎
   - 金山词霸
   http://www.iciba.com/%s
   - 欧路词典
   https://dict.eudic.net/mdicts/en/%s

3. 内网查找
   - 百度百科
   https://wapbaike.baidu.com/search/none?word=%s
   - 豆瓣
   https://m.douban.com/search/?query=%s
   - 知乎
   https://www.zhihu.com/search?type=content&q=%s



B. **直接跳转 app 搜索**
[预览效果](https://www.helloimg.com/images/2020/12/27/8b2ec927c45286431fa5c6cdb07d.gif)，图大慎入。

1. 欧路词典
   eudic://dict/%s
2. 应用市场
   market://search?q=%s
3. 高德地图 *[高德开放平台](https://lbs.amap.com/api/amap-mobile/summary)*
   androidamap://poi?sourceApplication=softname&keywords=%s
   搜索周边
   androidamap://arroundpoi?sourceApplication=softname&keywords=%s&dev=0
4. 微博国际版
   weibointernational://search?keyword=%s
5. 哔哩哔哩
   bilibili://search?keyword=%s
6. 有道词典
   yddict://dict/query?q=%s
7. Share微博
   sinaweibo://searchall/?q=%s

---

### 一些高级搜索技巧
参考：
[如何使用好搜索引擎（尤其是谷歌）2015.03.07](https://www.xmind.net/m/Qzus/)

- [site](https://www.google.com/search?newwindow=1&domains=xmind.net&sxsrf=ALeKk02mgOka8Vyuob6xilcJhPD4DsEaJw%3A1609002777639&ei=GW_nX7K7JtT_wAPTvJvwDA&q=%E5%AE%89%E5%8D%93+site%3Aloafing.cn&oq=%E5%AE%89%E5%8D%93+site%3Aloafing.cn&gs_lcp=ChNtb2JpbGUtZ3dzLXdpei1zZXJwEANQ4uUHWLjnB2D76gdoAHAAeACAAZ4BiAGSA5IBAzAuM5gBAKABAcABAQ&sclient=mobile-gws-wiz-serp)
- 双引号
- 减号 -
- 星号 *

---

### 自己动手 丰衣足食

@哎哟屁嘞

直接发现更多url scheme的方法，反编译想要找scheme的app的apk，打开AndroidMainifest.xml（最好是能格式化代码的编辑器，editplus一类的)，查找字段android:scheme=即可，附近有构成url scheme的其他字段，例如host等

具体组成格式是

`<scheme>://<host>:<port>/<path>?<query>`

例如：

xl://goods:8888/goodsDetail?goodsId=10011002

注意：并非所有字段一定会出现，一定会出现的只有scheme和host


### 你可能没有注意的小功能

在输入框输入空格可以浏览剪切板和历史搜索记录

搜索框输入“一行白鹭上西天”（西天！不是青天）可以开启隐藏的设置项，输入“日照香炉生紫烟”可以隐藏掉该设置

Android N以上系统可以通过添加通知栏瓷块在任意页面使用搜索和OCR功能

搜索lite提供了四种样式的小部件，并且可以在设置里进一步自定义，满足你对桌面美化的需求

