---
title: 类原生补全计划
type: docs
date: 2020-12-26 01:14:40
update: 2020-12-26 01:14:40
description: 良心应用推荐
---

> **值得加入「电池未优化」列表的应用。**

搜集低内存设备也能流畅使用的实用工具😋

拳打 MIUI、脚踢魔趣，跟臃肿卡顿说拜拜。

我的手机我作主！

---

添加一些不必常驻后台也能快速响应的良心应用。
归档下载见文末。

---

当前使用系统环境：
- `Pixel Extended, Android 11, Magisk 21.1`

  [![xbtcd16318e7ea82013593a7ee120469f4fd](https://cdn.jsdelivr.net/gh/forliuyifei/img@mater/img/Cover/1608918577383.jpg)](https://pixelextended.me/)

  ![IMG_20201226_215921](https://cdn.jsdelivr.net/gh/forliuyifei/img@mater/img/2020/12/1608991188961.webp)

## *电池未优化列表*
### [流体手势导航](https://play.google.com/store/apps/details?id=com.fb.fluid)
Fluid Navigation Gestures

比自带的手势导航好用，支持二级手势。
（Android 11 暂时无法隐藏导航栏，期待后续更新）

*有xposed框架或者太极的可以用 edge pro 模块，更强大，自定义更丰富，玩法更多。*
*xp 对性能的影响很容易感知，渣机伤不起。*

### [搜索 Lite](https://www.coolapk.com/apk/com.orekie.search)
配合流体手势的长滑动作，快速启动搜索，非常方便。
快速跳转 app、不需离开当前界面即可翻译单词、扫码获取链接直接跳转浏览器、网络通畅时优先使用谷歌搜索……
（可进缓存）

### [网络速度 - 网速 - Network Speed](https://www.coolapk.com/apk/com.evozi.network)
状态栏网速显示，非常准确。

### [全局复制](https://play.google.com/store/apps/details?id=com.camel.corp.universalcopy)
Universal Copy

突破应用限制，强行复制文字，配合自定义动作（如长按最近任务键）更方便唤出。（类似锤子的 bigang）
（可自动待机）

### [Authenticator](https://www.coolapk.com/apk/com.azure.authenticator)
微软出品的二次验证工具。
即使加入电池未优化，它也不会后台常驻，碰到需要验证的情况，仍然极速响应。
新版（6.2012.8446）支持「自动填充」帐号密码，可替代 Google 自家的自动填充，方便网络不通畅的用户使用。
（可走 FCM ）

### [几何天气](https://www.coolapk.com/apk/wangdaye.com.geometricweather)
Geometric Weather

简洁优雅，省电流畅，可设置随重力感应的动态壁纸。
不使用小部件，仅添加状态栏通知，不需常驻后台，也能隔一段时间自动刷新天气信息。
（可进缓存）

### [App Ops](https://www.coolapk.com/apk/rikka.appops)
碰到不得不用的流氓软件，少给点权限。
（心理安慰 😌）

---

## *基础限制*
> *以下是不必刻意后台保活的应用。*

### [翻译](https://www.coolapk.com/apk/com.google.android.apps.translate)
谷歌自家的工具，对原生系统的支持自然不会差，长按选中文字进行快速翻译。
（可进缓存）

### [欧路词典](https://www.coolapk.com/apk/com.qianyan.eudic)
碰到稍复杂、专业的翻译情景，替代谷歌翻译。
可导入专业词典。

### [黑阈](https://jianyu.io/)
对我而言，最主要的功能其实是监控 app 运行状态，过于流氓的软件添加为「临时应用」。
不要用它处理 微信、QQ，与其黑阈它们，不如直接找找合适的流畅省电版本。



### [nian-单机记本](https://www.coolapk.com/apk/sa.nian.so)
完全本地化的良心应用，不只是「笔记」，还能添加 「清单、记账、计时、打卡」，不怕跑路，不怕小公司资料泄露。
配合 FolderSync 随意备份至 坚果云 webdav / One Drive 或其它存储空间。
配合 流体手势 - 快捷方式 - Nova 活动 - nian.so.view.NewStepA
快速新建笔记：nian.so.view.NewStepA
少有的支持 GIF 动图封面和背景的笔记 app。
还有 GitHub 那样的 “绿墙”，督促你好好记录别偷懒。
（可进缓存）

### [FolderSync](https://play.google.com/store/apps/details?id=dk.tacit.android.foldersync.lite)
花点时间登录各家云存储服务帐户（坚果云webdav、One Drive、Google Drive…），配置完备，开启某些重要文件夹的计划同步，偶尔手动同步，大大降低文件丢失的风险。（软件本身耗电量微乎其微。）
非 Pro 版也够用，功能不缺，广告可关。


### [屏幕录制](https://play.google.com/store/apps/details?id=com.kimcy929.screenrecorder)
安卓版本越高越好用的录屏工具，支持高帧率录屏（最高120fps）、立体声道音频内录（无须root）、H.265编码……下拉通知栏使用磁贴开始录制。（以前玩VG的时候，留在 MIUI 就为了音频内录）

不要黑阈，如果录制过程中被杀后台，可加入电池未优化列表

### [Gmail](https://www.coolapk.com/apk/com.google.android.gm)
（可进缓存，可走 FCM ）

QQ 邮箱客户端其实也不错，甚至可以直接代收 Gmail。只是它不支持 Chrome 的 CustomTaps，跳转链接的时候不够舒服。

**使用 Gmail 客户端登录 QQ 邮箱：**
1. 确保 QQ 邮箱已设置独立密码，并已开启 POP3/SMTP/IMAP 功能，具体路径为电脑网页版 QQ 邮箱—设置—帐户；

2. 在添加帐户中选择其它，填入 QQ 邮箱帐户，下一步选择 个人 PO3，输入密码（前面获取的一个非永久乱码），服务器 pop.qq.com ，端口 995 ，安全类型 SSL/TLS ；

3. 外发设置 SMTP 服务器 smtp.qq.com ，端口 465 ，安全类型 SSL/TLS ；

4. 其它同步、删除之类的设置按个人喜好；

5. 在不科学的情况下对这个 QQ 帐户进行收发邮件测试。



---

下载地址：[蓝奏云](https://lanzous.com/b00o5bsod)
验证码：良心

---

感谢小编提供的 py 交易 <img src="https://cdn.jsdelivr.net/gh/forliuyifei/emoticon@master/weibo/d_touxiao.png" alt="d_touxiao.png" title="d_touxiao"/>

![py](https://cdn.jsdelivr.net/gh/forliuyifei/img@mater/img/2020/12/1609387610950.webp)

[![点击前往酷安](https://cdn.jsdelivr.net/gh/forliuyifei/img@mater/img/2020/12/1609387610951.webp)](https://www.coolapk.com/album/23618598)
