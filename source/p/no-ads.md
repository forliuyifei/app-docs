---
title: no-ads
type: docs
date: 2020-12-25 13:59:57
update: 2020-12-25 13:59:57
description: 以尽可能简单无伤的方式摆脱广告
---

实例见后文，有待补充 📝

## 原则
1. 可用可不用的：
   清除数据、卸载！能找到更良心的替代品就用替代品，不要惯着流氓软件。
2. 没得选的：
   **尽量在官方版应用的基础上做些小修改。**
   少用各类良莠不齐的 
   *「高级、pj、plus、pro、mod」版。*
   与「账号、金钱、隐私」相关的 app，尽量使用官方发布的软件版本，使用非官方签名的应用，可能碰到各种各样的问题：
   - 限制登录，封号，盗号。
   - 部分功能不可用，比如分享到 QQ、微信。
   - 其它潜在风险。
   
  可以完全离线使用的工具，也要考虑后续更新，签名不一致无法覆盖安装，要是没有配置导出导入功能，卸载重装重新进行配置是很浪费时间的一件事。（要是有核心破解当我没说🙄）
3. 修改不要贪多，可能触发奇奇怪怪的 bug，反而导致卡顿、后台占用增加、耗电更快。影响正常使用，得不偿失。
4. 如果你确实喜欢某样工具，在支付能力范围内选择入正，是值得鼓励的，市场上的劣币已经够多，优秀的产品不应该被它们淹没。
   说句资本家附体的话：
   > **你花的每一分钱，都将世界往你喜欢的方向推进一步。**


## 可能用到的工具
（通常相同类型的工具选一个就够，碰到力有未逮的时候再换另一个）

- 文件管理
  - **MT 管理器**
  - Solid Explorer
  - 第三方 rec 内置的文件管理

- 组件控制
  - **App Manager**
  - MyAndroidTools
  - Watt
  
- ~~切断连接~~
  - AdGuard
  - Adaway
  *不是很推荐。规则太少看不出效果，规则太多容易误杀，影响正常使用。*

## 实例
测试环境：Android 11

### QQ 音乐
*推荐版本 9.7.0.4*

去除开屏广告和部分弹窗。

1. 删除文件夹中的广告缓存，然后去除这两个文件夹的写入权限。
   ```
   /data/media/0/qqmusic/splash（活动图）
   /data/media/0/Android/data/com.tencent.qqmusic/files/cache/ad_source/images（广告图）
   ```
  
2. 禁用带有 `ads.` 的所有活动（Activity）
   ```
   com.qq.e.ads.ADActivity
   com.qq.e.ads.LandscapeADActivity
   com.qq.e.ads.PortraitADActivity
   com.qq.e.ads.RewardvideoLandscapeADActivity
   com.qq.e.ads.RewardvideoPortraitADActivity
   com.tencent.ads.canvasad.AdCanvasActivity
   com.tencent.tads.splash.AdLandingPageActivity
   ```

3. 使用 AdGuard 拦截开屏广告
   添加规则：
   ```
   ||pgdt.gtimg.cn/gdt/0^$app=com.tencent.qqmusic
   ```
   （需要清除应用数据，光清缓存似乎不管用）

### 网易云音乐
*推荐 4.3.1 play 版，新版未测试。*

1. 去除启动页广告
   删除下列文件夹内部广告缓存，将文件夹的读写权限设为空（要是修改失败，进 rec 改，权限管够）
   ```
   /data/media/0/netease/cloudmusic/AD/
   /data/media/0/Android/data/com.netease.cloudmusic/cache/Ad/
   ```
   删除文件夹后，创建一个同名空白「文件」也可防止后续广告缓存的生成。（部分流氓中的战斗机仍能恢复，所以最好还是有 root 一劳永逸）
2. 去除评论区广告
   AdGuard 规则：
   ```
   ||music.163.com/eapi/ad^
   ```


### 酷安
*推荐版本 9.6.3*

禁用活动关键词 `ads.`
```
com.qq.e.ads.ADActivity
com.qq.e.ads.LandscapeADActivity
com.qq.e.ads.PortraitADActivity
```

### 照片编辑器

禁用活动关键词 `ads.`
```
com.google.android.gms.ads.AdActivity
```

### 百度网盘
禁用活动关键词 `advertise`
```
com.baidu.netdisk.platform.business.incentive.advertise.ui.AdvertiseActivity
com.baidu.netdisk.platform.business.incentive.advertise.ui.AdvertiseFinishPageActivity
com.baidu.netdisk.ui.advertise.AdvertiseContentActivity
com.baidu.netdisk.ui.advertise.FlashAdvertiseActivity
com.baidu.netdisk.ui.advertise.PlayerAdvertiseActivity
com.baidu.searchbox.novel.reader.ad.ReaderAdvertisementActivity
```
*`除了被动下载他人只在百度网盘分享的文件以外，在任何情况下都不推荐使用百度网盘，除非你有受虐倾向。`*

---

#### 网盘怎么选？
请尽量选用
**「低客户端依赖、把用户当人看、对得起你家带宽」**
的网络存储服务：
- [坚果云](https://www.jianguoyun.com/)
  适合存放小文件，如学习、工作文档，不主打分享功能，定位是同步盘。
  最良心的是支持 webdav，国内少有。
- [蓝奏云](https://lanzous.com)
  应该是这几年大家最喜欢的分享盘，暂无存储空间限制说明，单文件 100 MB 以下，有文件类型限制，不过可以打包分卷予以解决。
- [奶牛快传](https://cowtransfer.com/?lx_guid=5a2ab9bf-d49d-4654-9ac2-5f00e1d35edd)
  方便临时分享大文件，也可注册获取存储空间，无过多限制。
  >1024GB超大云盘空间
  支持多达20GB超大文件上传
  体验极速的上传下载，永不限速
  自定义文件有效期和下载次数
- [文叔叔](https://wenshushu.cn/i/Z2RA5H)
  上传和下载速度很快，分享文件便于管理，有下载次数（流量）限制策略，自行衡量。
  >免费空间 40GB ⭐ 高级别加密
- 欢迎补充……
