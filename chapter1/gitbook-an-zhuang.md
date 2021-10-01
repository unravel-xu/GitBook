# GitBook安装

## 参考文章

[GitBook文档\(中文版\)](https://chrisniael.gitbooks.io/gitbook-documentation/content/index.html)

[GitBook使用入门](https://tonydeng.github.io/gitbook-zh/gitbook-howtouse/index.html)

[基于GitBook搭建个人博客](https://www.cnblogs.com/levywang/p/13569619.html)

[新版gitbook+github+Typora使用方法](https://www.wumingx.com/tools/gitbook-github-typora.html)（个人认为typora的markdown写作体验原优于vscode）

## 安装

```bash
npm install gitbook-cli -g
```

安装完成后，使用如下命令检验，如果是第一次使用，`gitbook-cli`将自动安装`gitbook`，安装时间视网络情况而定

```bash
gitbook -V
```

如果出现报错，没关系当时我也遇了，查了查大概是如下原因：

node版本不匹配，不建议卸载原环境降版本，推荐的解决方法是使用`nvm`版本管理，测试的匹配组合是：

`CLI version` : 2.3.2

`GitBook version` : 3.2.3

`node`: 10.21.0

推荐参考链接：

* [win10安装nvm踩坑实录](https://segmentfault.com/a/1190000020112650)
* [nvm使用切换环境](https://love2wind.cn/archives/2201.html)

## 卸载

使用如下命令卸载`gitbook-cli`：

```bash
npm uninstall gitbook-cli-g
```

## 初始化

选择一个要放置GitBook的文件夹，然后在这个文件夹中打开命令行输入命令：

```bash
gitbook init
```

该命令会初始化项目，如果你有`git`基础，那么就容易明白了

初始化后，你会发现该文件夹中自动多出了两个文件

* README.md：用于介绍该GitBook，会固定在目录顶部
* SUMMARY.md：该GitBook的目录，左侧栏显示出章节

**注意：这两个文件是项目所必须的**，如何编辑将在使用中介绍

