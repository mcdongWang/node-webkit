#[英文原版](./README_us.md)

> 译者: [王东(mcdongWang)](github.com/mcdongWang)
> 译者: [方玉昕(bereniceFang)](github.com/bereniceFang)

## 介绍

node-webkit 是一个基于 `Chromium` 和 `node.js` 的本地应用软件运行时. 你可以通过 node-webkit , 使用 HTML 和 JavaScript 来编写本地应用软件. 它也可以让你直接从 DOM 调用 Node.js 的模块. 是一个新的允许用所有 Web 技术来编写本地应用软件的方法.

node-webkit 是由英特尔开源技术中心建立并开发的.

[node-webkit 介绍(PPT)](https://speakerdeck.com/u/zcbenz/p/node-webkit-app-runtime-based-on-chromium-and-node-dot-js)   
[使用 node-webkit 开发桌面应用](http://strongloop.com/strongblog/creating-desktop-applications-with-node-webkit/)     
[用 node-webkit 从 WebApp 到 DesktopApp(PPT)](http://oldgeeksguide.github.io/presentations/html5devconf2013/wtod.html)

## 特性

* 用流行的 HTML5, CSS3, JS 和 WebGL 来编写本地应用软件.
* 完全支持[Node.js APIs](http://nodejs.org/api/) 和所有的 [第三方npm模块](https://npmjs.org).
* 高性能: Node and WebKit 运行在同一个线程: 函数调用会非常的简单; 对象是在同一个堆中, 可以相互调用;
* 方便的打包和发布应用.
* Linux, Mac OSX 和 Windows 全平台支持

## Downloads
[v0.9.2 版本说明](https://groups.google.com/d/msg/node-webkit/qpBhcWr-hSc/caGjhtl8cEgJ)

预编译二进制文件 (v0.9.2 - Feb 20, 2014):

* Linux: [32bit](http://dl.node-webkit.org/v0.9.2/node-webkit-v0.9.2-linux-ia32.tar.gz) / [64bit] (http://dl.node-webkit.org/v0.9.2/node-webkit-v0.9.2-linux-x64.tar.gz)
* Windows: [win32](http://dl.node-webkit.org/v0.9.2/node-webkit-v0.9.2-win-ia32.zip)
* Mac: [32bit, 10.7+](http://dl.node-webkit.org/v0.9.2/node-webkit-v0.9.2-osx-ia32.zip)

**如果你本地的 Node 模块工作在 Node v0.10 环境下. 那本你需要使用 node-webkit v0.8.x版本. If your native Node module works only with Node v0.10, then you should use node-webkit v0.8.x, 它也是一个维护的版本分支. [更多信息](https://groups.google.com/d/msg/node-webkit/2OJ1cEMPLlA/09BvpTagSA0J)**  
[v0.8.6 版本说明](https://groups.google.com/d/msg/node-webkit/CLPkgfV-i7s/hwkkQuJ1kngJ)

预编译二进制文件 (v0.8.6 - Apr 18, 2014):

* Linux: [32bit](http://dl.node-webkit.org/v0.8.6/node-webkit-v0.8.6-linux-ia32.tar.gz) / [64bit](http://dl.node-webkit.org/v0.8.6/node-webkit-v0.8.6-linux-x64.tar.gz)
* Windows: [win32](http://dl.node-webkit.org/v0.8.6/node-webkit-v0.8.6-win-ia32.zip)
* Mac: [32bit, 10.7+](http://dl.node-webkit.org/v0.8.6/node-webkit-v0.8.6-osx-ia32.zip)

[更旧版本](https://github.com/rogerwang/node-webkit/wiki/Downloads-of-old-versions)

###apps 示例
你可能会对 [我们的 demo 库](https://github.com/zcbenz/nw-sample-apps)感兴趣. 还有 [使用 node-webkit 的软件和公司列表](https://github.com/rogerwang/node-webkit/wiki/List-of-apps-and-companies-using-node-webkit).

## 快速入门

创建 `index.html`:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Hello World!</title>
  </head>
  <body>
    <h1>Hello World!</h1>
    We are using node.js <script>document.write(process.version)</script>.
  </body>
</html>
```

创建 `package.json`:

```json
{
  "name": "nw-demo",
  "main": "index.html"
}
```

将 `index.html` 和 `package.json` 压缩到一个 zip 格式的压缩包中, 并重命名为 `app.nw`:

````bash
$ zip app.nw index.html package.json
````

文件结构如下所示:

```
app.nw
|-- package.json
`-- index.html
```

下载你所用系统的预编译二进制文件, 并用它打开 `app.nw` 文件:

````bash
$ ./nw app.nw
````

备注: 在 Windows 下, 你可以使用将 `app.nw` 拖到 `nw.exe` 的方法去运行你的 App.

## 文档

更多关于如何 编写/打包/运行 你本地程序的文章:

* [如何去运行 apps](https://github.com/rogerwang/node-webkit/wiki/How-to-run-apps)
* [如何去打包和发布你的 apps](https://github.com/rogerwang/node-webkit/wiki/How-to-package-and-distribute-your-apps)
* [如何在 node-webkit 中使用 Node.js 模块](https://github.com/rogerwang/node-webkit/wiki/Using-Node-modules)

[Wiki地址](https://github.com/rogerwang/node-webkit/wiki).

## 社区

我们使用 [node-webkit group](http://groups.google.com/group/node-webkit) 作为我们的邮件列表(仅英文). 订阅连接 [node-webkit+subscribe@googlegroups.com](mailto:node-webkit+subscribe@googlegroups.com).
Issues的追踪就在这个GitHub.

你可以通过 [IRC](http://irc.freenode.net) 的 ##node-webkit 频道与我们进行沟通

译者注:
Gitter.im 的交流平台
[nw.js](https://gitter.im/nwjs/nw.js)

## License

`node-webkit`'s code in this repo uses the MIT license, see our `LICENSE` file. To redistribute the binary, see [How to package and distribute your apps](https://github.com/rogerwang/node-webkit/wiki/How-to-package-and-distribute-your-apps)

[![Analytics](https://ga-beacon.appspot.com/UA-27805459-2/node-webkit/index)](https://github.com/igrigorik/ga-beacon)
