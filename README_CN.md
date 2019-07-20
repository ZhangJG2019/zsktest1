## 技术栈和主要框架

📦 Vue 全家桶：vue2 + vuex + vue-router + webpack  
📌 ES6     
📡 网络请求：axios  
🎈 页面相应式框架：bootstrap，element-ui  
✏️ 后台：express  
📝 代码高亮：highlight.js  
🗄 数据库：lowdb  
📖 Markdown解析器：vue-markdown  
🔖 表单验证：vee-validate  
🏆 跨平台框架：Electron  



我利用 Express 把后台搭建在 8081 端口上，并写好路由，请求会转到 8080，开启服务器的时候也会自动开启后台。

我当前的开发环境是 node v6.11.0 ，npm v3.10.10（npm v5.3.0 也可以，再高一点的版本没有测试过，应该也没多大问题），Vue.js v2.8.2 

``` bash

# install dependencies 安装依赖
npm install

# serve with hot reload at localhost:8080
npm run dev

# serve with hot reload at localhost:8080
npm run start

# build for production with minification 打包
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test

# 打包 Mac 应用
npm run build:mac

# 打包 Linux 应用
npm run build:linux

# 打包 Win 应用
npm run build:win

# 打包 Cordova 应用
npm run build:app

```

这里要单独说一下 Cordova 的打包方式，它比桌面端的稍微特殊一点。

首先把 src/main.js 文件中关于 Coredova 的三行注释打开，Coredova 库的初始化需要包在生成 Vue 实例 的外面。打开注释以后，再执行接下来的步骤。

我在项目中放了一个 Makefile，可以根据这个来做。

1. 首先全局安装 cordova 命令
> npm install -g cordova 

2. 再输入下面的命令，生成 app 项目目录
> cordova create app com.vueobjccn vueobjccn

3. 进入到 app 文件夹中
> cd app

4. 添加对应的平台
> cordova platform add ios  
> cordova platform add android

5. 运行项目
> cordova run ios  
> cordova run android

Cordova 只生成了一个壳的 app，里面具体的内容还是读取的网页，在生成的对应的应用里面有一个 www 的文件夹，这个文件夹里面就是要加载页面。JavaScript 打包之后是会生成 www 的文件夹，只要去替换 Cordova 对应平台里面的 www 文件夹里面的内容即可。

额外说几句，在 app 发展到现在这么成熟的时代，如果构建一个大的 app，用 Cordova 框架去做，不用原生，不做任何优化，用户体验确实不如原生的快。我这次就专门打包体验了 Cordova app，没有做任何优化，打包出来就用，如果是挑剔的用户，放在当今各大 app 接近完美的体验度相比来说，确实会感到满足感略低。如果真的要前端开发 app ，给2个建议，如果是用 Cordova 框架，一定要尽量优化优化，不然性能不如原生。如果想有接近原生的体验，那么可以考虑用 React Native 或者 Weex。

## 🚀 跨平台开发

JavaScript 跨平台开发打包成桌面级应用，主要用 Electron 框架。这里需要在 devDependencies 里面安装好 "electron"、"electron-builder"、"electron-packager" 这三个。其他的路径配置在 webpack 里面配置好即可。

关于 Cordova 的安装，确实可以吐槽一点网络的问题。如果你在一个翻墙环境很差的地方，真的很痛苦。比如之前在一个翻墙环境很差的情况下全局安装 Cordova ，各种报错，就算是换了 cnpm 完全安装了以后，添加 iOS 平台以后以后会报一个 co 文件找不到的问题，感觉是 cnpm 没有把命令安装完整。后来我回到家里，翻墙网络很好，npm install 一下子就安装好了。不过有个小插曲：Cordova iOS 4.4.0 template 如果报错，就多安装几次，原因还是翻墙的原因，没有 catch 到。

还有可能会遇到下面这个错误：

> "Error: Cannot find module 'config-chain'" when running 'ionic start'

这个错误就用 sudo 命令重新尝试一遍原命令就好了。

最终打包完成会在 dist 的文件夹中。