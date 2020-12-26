---
title: Magisk
description: “无 root，不安卓。”
type: docs
date: 2020-12-24 21:27:02
update: 2020-12-24 21:27:02
---

[Magisk 源码仓库](https://github.com/topjohnwu/Magisk)

## 当前版本
![lastest apk](https://camo.githubusercontent.com/6ea977814028c8d7eca513a23b2bc24caac1c3c9f3f5d20af1d317f45c1f4885/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4d616769736b2532304d616e616765722d76382e302e332d677265656e) ![lastest stable zip](https://camo.githubusercontent.com/865fa6c7f9cd8204da54458da2d14ebe5530272dded22138bf38de546b61fead/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4d616769736b2d7632302e342d626c7565) ![lastest beta zip](https://camo.githubusercontent.com/19e905743d069248edbb8f2bc8ca600126aabdd65a51419bc5ae99765b72df0d/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4d616769736b253230426574612d7632312e312d626c7565)

## 安装
通常只需解锁手机（BL锁）后在第三方 rec 里面刷入面具的 zip 包即可。

部分没有第三方 rec 的手机可以通过修补 boot.img 的方式安装面具。

### Android 11 踩坑
直刷 Magisk 20.4 和 21.1 都出现无法开机的情况，刷卸载包无效，不得不重刷 ROM。

**解决方案：**
先刷 [MagiskCU.zip](https://lanzoui.com/iS22wj1wqfi) 再刷 [Magisk-v21.1.zip](https://github.com/topjohnwu/Magisk/releases/download/v21.1/Magisk-v21.1.zip) 便可正常开机并获取 root 权限。
如果出现 “需要修复”，保证网络通畅，修复它即可。


### 部分应用出现问题
比如网易云音乐无法扫描本地音乐，表现为一直处于扫描状态。
还有静读天下无法使用。

**解决措施：**
在 Magisk hide 里面将对应的软件勾上。

**注意：**如果软件能正常使用，不要随意将其 hide，比如支付宝，在 Magisk hide 里面勾上支付宝，将导致支付宝变得异常卡顿。

## 其它相关教程
- [Magisk精通指南（小白向）-  Android爱好者 2020.04.11](https://www.coolapk.com/feed/17973123)
- [使用 Android Overlay 替换机制作 Magisk 汉化模块 - 幻夢清雨樓 2020.08.02](https://www.coolapk.com/feed/20614159)
