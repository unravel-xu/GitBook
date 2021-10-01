# 配置文件

## 配置文件创建

**在项目的根目录创建book.json文件，与SUMMARY.md同级**，创建后自定义参数，下面将会对参数进行说明

## 参数说明

[GitBook的官方说明](https://github.com/GitbookIO/gitbook/blob/master/docs/config.md)

| 变量 | 描述 |
| :---: | :---: |
| root | 包含所有图书文件的根文件夹的路径，除了 book.json |
| structure | 指定自述文件，摘要，词汇表等的路径，参考 Structure paragraph |
| title | 您的书名，默认值是从 README 中提取出来的。在 GitBook.com 上，这个字段是预填的。 |
| description | 您的书籍的描述，默认值是从 README 中提取出来的。在 GitBook.com 上，这个字段是预填的。 |
| author | 作者名。在GitBook.com上，这个字段是预填的。 |
| isbn | 国际标准书号 ISBN |
| language | 本书的语言类型 —— ISO code 。默认值是 en |
| direction | 文本阅读顺序。可以是 rtl （从右向左）或 ltr （从左向右），默认值依赖于 language |
| gitbook | 应该使用的GitBook版本。使用 SemVer 规范，并接受类似于 “&gt; = 3.0.0” 的条件。 |
| links | 在左侧导航栏添加链接信息 |
| plugins | 要加载的插件列表 |
| pluginsConfig | 插件的配置 |

### root

包含所有图书文件的根文件夹的路径， book.json 文件除外。 例：

```bash
"root" : "./docs",
```

### structure

指定 Readme、Summary、Glossary 和 Languages 对应的文件名。

### title

电子书的书名，默认值是从 README 中提取出来的。在 GitBook.com 上，这个字段是预先填写的。 例：

```bash
"title" : "gitbook-notes",
```

### author

作者姓名，在GitBook.com上，这个字段是预先填写的。 例：

```bash
"author" : "victor zhang"
```

### description

电子书的描述，默认值是从 README 中提取出来的。在GitBook.com上，这个字段是预先填写的。

```bash
"description" : "Gitbook 教程"
```

### direction

文本的方向。可以是 rtl 或 ltr，默认值取决于语言的值。

```bash
"direction" : "ltr"
```

### gitbook

应该使用的GitBook版本。使用SemVer规范，接受类似于 &gt;=3.0.0 的条件。

```bash
"gitbook" : "3.0.0",
"gitbook" : ">=3.0.0"
```

### language

Gitbook使用的语言, 版本2.6.4中可选的语言如下： en, ar, bn, cs, de, en, es, fa, fi, fr, he, it, ja, ko, no, pl, pt, ro, ru, sv, uk, vi, zh-hans, zh-tw 例：

```bash
"language" : "zh-hans",
```

### links

在左侧导航栏添加链接信息 例：

```bash
"links" : {
    "sidebar" : {
        "Home" : "https://github.com/dunwu/gitbook-notes"
    }
}
```

### styles

自定义页面样式， 默认情况下各generator对应的css文件 例：

```bash
"styles": {
    "website": "styles/website.css",
    "ebook": "styles/ebook.css",
    "pdf": "styles/pdf.css",
    "mobi": "styles/mobi.css",
    "epub": "styles/epub.css"
}
```

例如要使 h1、h2 标签有下边框， 可以在 website.css 中设置

```bash
h1 , h2{
    border-bottom: 1px solid #EFEAEA;
}
```

## 默认插件包括

* highlight - 语法高亮插件
* search - 搜索插件，不支持中文
* sharing - 分享插件，对应页面右上角的分享功能
* font-settings - 字体设置插件
* livereload - 热加载插件

**特别说明：**系统自带插件可通过在插件名前加`-`的方式删除，如修改为`-sharing`

在添加或删除了插件后要加载使用插件，需要执行`gitbook install`命令来更新项目配置

插件需要先要在`book.json`文件里面`plugins`中才能生效，如果只是安装了插件，而没配置的话是不会生效的。

**tips：**`gitbook install`命令安装慢，而且是全部插件都安装一遍，网络环境不佳可能需要等待很长时间安装不下来，如果只安装一个插件的话建议使用NPM命令安装，之前介绍了如何修改npm的源，可以使用 `npm install gitbook-plugin-插件名`的方式进行安装。

