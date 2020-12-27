# app-docs
[应用说明书](https://doc.loafing.cn) 的 hexo 源码。

**为方便访问，同时存放在 [GitHub](https://github.com/forliuyifei/app-docs) 和 [Coding](https://forzqx.coding.net/p/app-docs/d/app-docs/git)（国内速度很快）**

欢迎任何热爱 Android 的玩家改进此文档。

## 改进方式
### 网页端
直接在浏览器修改此仓库的某个文件并提交 Pull requests

如果你没有相关经验，可以参考这篇 [从零到 PR](https://ld246.com/article/1589724003386)，图文并茂，很容易理解。


### 使用终端 GIT 命令
适合长篇大论。

**步骤**
1. 将此项目 fork 到你自己的仓库
2. 将你自己的仓库使用 `git clone` 命令拉取至本地，进入该文件夹完成后续操作
3. 修改完毕后，使用以下命令上传至你自己的仓库
   ```
   git add .
   git commit -m "文档补充"
   git push
   ```
4. 发起 Pull requests

---

~~#### 获取文章列表~~
~~cd ~/app-docs~~
~~#!/bin/bash~~
~~echo `date +"%Y-%m-%d %H:%M:%S"` > source/Archive.txt~~
~~tree "source/p" "source/apps" >> source/Archive.txt~~
~~tree "public/p" "public/apps" >> source/Archive.txt~~
