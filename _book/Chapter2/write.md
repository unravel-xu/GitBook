# 相关文件编写

## README.md文件编写

使用`Markdown`编写介绍内容

在每个目录中都会有一个`README.md`文件用于描述该章节的说明

## SUMMARY.md文件编写

如下所示：

```markdown
# Summary

* [xxx](README.md)
* [xxx](xxx/README.md)
   * [xxx](xxx/xxx.md)
   * [xxx](xxx/xxx.md)
* [xxx](end/README.md)
```

`SUMMARY.md`基本上是列表加链接的语法。链接中可以使用目录，也可以使用了链接，通过缩进表示目录章节层次结构。

可以先在SUMMARY.md中预先定义好所有文件结构，然后输入`gitbook init`命令，会自动创建定义文件结构中的文件

