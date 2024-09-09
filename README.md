# 开飞机文档

本仓库从[nolebase](https://github.com/nolebase/nolebase/)修改而来，内容由[原文档](https://github.com/We-Fly/doc)迁移而来，原文档由于缺乏维护，已经弃用。

>本文档采用 `署名-非商业性使用-相同方式共享 4.0 国际` [CC-BY-NC-SA-4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.zh)许可证进行许可。

你可以对本创作进行转载、节选、混编、二次创作，但不得运用于商业目的，且使用时须进行署名，采用本创作的内容必须同样采用本协议进行授权。

## 贡献指南

正如你所看到，本站所有内容都是开源的。任何人都可以向[本仓库](https://github.com/We-Fly/doc)贡献教程、文章。并采用[CC-BY-NC-SA-4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)许可证进行许可。

不得不承认，由于技术原因，本文档的页面在更新后会有一段时间的延迟，更改才会同步到网页上，请尝试清除浏览器缓存或者等待一段时间，参考这个[issue](https://github.com/We-Fly/doc/issues/26)

注意，每次在`doc/wefly`分支提交的更改都会触发网页更新，请提交`Pull Requests`到`doc/wefly`分支，通过检查后再进行合并。

如果你没有仓库的访问权限，请自行`fork`仓库然后提交`Pull Requests`到`doc/wefly`分支。

```bash
git clone -b doc/wefly https://github.com/We-Fly/nolebase.git  # 使用https克隆
git clone -b doc/wefly git@github.com:We-Fly/nolebase.git      # 使用ssh克隆
```

本文档采用了`Nólëbase`强力驱动。请参考 [Nólëbase](https://nolebase.ayaka.io/)

文档相关页面均采用`Markdown`语法编写

若您希望为本站贡献内容，请确保您的系统已安装 [node.js](https://nodejs.org/zh-cn/) 及 [pnpm](https://pnpm.io/zh/installation)。

以下为本项目的相关命令：

```bash
pnpm install # 安装
pnpm docs:dev # dev模式,本地查看文档
pnpm docs:build # 构建网站发布所需要的资源, build之后在 .vitepress/dist 下, 保证在本地能构建成功后再发布比较好
```
