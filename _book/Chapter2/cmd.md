# GitBook命令

这里将介绍GitBook的一些命令

**输出gitbook的帮助信息**

```bash
gitbook --help
```

**输出gitbook-cli的帮助信息**

```bash
gitbook help
```

**生成静态网页并运行服务器**

```bash
gitbook serve
```

**生成静态网页**

```bash
gitbook build
```

**生成静态网页时指定gitbook的版本，如果本地没有将先下载**

```bash
gitbook build --gitbook=3.2.3
```

**列出所有的gitbook版本**

```bash
gitbook ls
```

**列出远程可用的gitbook版本**

```bash
gitbook ls-remote
```

**更新到gitbook的最新版本**

```bash
gitbook update
```

**卸载对应的gitbook版本**

```bash
gitbook uninstall 3.2.3
```

**安装依赖**

```bash
gitbook install
```

**指定log的级别**

```bash
gitbook build --log=debug
```

**输出错误信息**

```bash
gitbook builid --debug
```

