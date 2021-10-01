# 常用命令

以下命令都可以通过shell或者cmd来执行 通过`gitbook -V`命令查看是否安装成功。

命令`()`内的部分表示一般省略

**通过npm安装**

```bash
npm install gitbook-cli -g
```

**初始化** 新建一个文件夹，例如新建 mygitbook ，然后在该目录下执行命令：

```bash
gitbook init
```

会自动生成两个必要的文件`README.md`和`SUMMARY.md`

**预览** 执行命令：

```bash
gitbook serve (./{book_name})
```

gitbook会启动一个4000端口用于预览，可以在浏览器打开网址： [http://localhost:4000](http://localhost:4000/) 预览效果。

**编译** 执行命令：

```bash
gitbook build (./{book_name} --output=./{outputFolder})
```

运行该命令后会在根文件夹生成一个`_book`文件夹，包含了书籍的所有 html 文件。可以使用该命令来生成网页而不开启服务器，也可以将`_book`文件夹部署到服务器上。

