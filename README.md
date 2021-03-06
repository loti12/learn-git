2017.05.22

## git 下载安装

* [下载 git OSX](http://code.google.com/p/git-osx-installer/downloads/list?can=3)
* [下载 git WINDOWS](http://msysgit.github.io/)

## 创建新仓库

创建新文件夹，执行 `git init` , 来创建新仓库

## 检出仓库

执行命令 `git clone /path/to/repository`

## git 三种状态

本地仓库模型有三种状态。第一个是你的 工作目录，它持有实际文件；第二个是 暂存区（Index），它像个缓存区域，临时保存你的改动；最后是 HEAD，它指向你最后一次提交的结果。

![git 仓库模型](http://rogerdudler.github.io/git-guide/img/trees.png)

### 相应的检入与检出命令如图：

![git 三种状态之间的转换](https://segmentfault.com/img/bVs6Ae)

### 相关命令的简要说明如下：

* `git add files`：把当前工作文件拷贝到暂存区域。
* `git commit`：在暂存区域生成文件快照并提交到本地仓库。
* `git reset -- files`：用来撤销最后一次 git add files，也可以用 git reset 撤销所有暂存区域文件。
* `git checkout -- files`：把文件从暂存区域覆盖到工作目录，用来丢弃本地修改。

## 推送改动

现在你的代码已经提交到本地仓库了，可以使用 `git push origin master` 推送到远程仓库

如果还没有克隆，可以使用 `git remote add origin server`

## 分支管理

master 是“默认的”分支。创建一个叫做“feature_x”的分支，并切换过去：

`git checkout -b feature_x`

切换回主分支：

`git checkout master`

要合并其他分支到你的当前分支，执行：

`git merge <branch>`

## 参考资料

* [git 中文文档](https://git-scm.com/book/zh/v2)
* [git 指南](http://rogerdudler.github.io/git-guide/index.zh.html)
* [常用 Git 命令清单](http://www.ruanyifeng.com/blog/2015/12/git-cheat-sheet.html)
* [git-flow 备忘清单](http://danielkummer.github.io/git-flow-cheatsheet/index.zh_CN.html)
* [Git提交的正确姿势：Commit message 和 Change log 编写指南](https://mp.weixin.qq.com/s?__biz=MzA4MjU5NTY0NA==&mid=401840568&idx=1&sn=051879b73f32ab7bcbcfc2e3cdd85f07&scene=1&srcid=0107l8avY4frKW3kfhaIUoNY&key=41ecb04b0511100344d280ce4225cc8c4d97599af475ef134186f7df3a7b8ace7e0e2eebc59d96ca00d6c9abf1ebf9e2&ascene=0&uin=MjAyNzY1NTU%3D&devicetype=iMac+MacBookPro12%2C1+OSX+OSX+10.11.2+build(15C50)&version=11020201&pass_ticket=ymbjwf7oU6CeUuxBIkhi0U6TOA5EP5ZWHXbpm6NVy%2FY%3D)
