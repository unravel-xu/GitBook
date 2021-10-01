# Node.js安装

![Node.js](https://evariste-xu.oss-cn-beijing.aliyuncs.com/node.js.png)

## 参考文章

[win10下安装node.js的步骤](https://segmentfault.com/a/1190000038318834)

## 简单介绍：

> Node.js 是一个开源与跨平台的 JavaScript 运行时环境。 它是一个可用于几乎任何项目的流行工具。

## 官方下载：

[https://nodejs.org/zh-cn/download/](https://nodejs.org/zh-cn/download/)

根据配置选择下载并安装，如果为使用GitBook首次下载，推荐下载**10.21.0**版本

安装后可以在进入cmd输入`node -v`进行验证，结果应该会显示出安装的`node.js`版本号

## 修改镜像源

如果是国内用户建议修改镜像源

```bash
npm config set registry https://registry.npm.taobao.org
```

查看修改结果

```bash
npm config list
```





