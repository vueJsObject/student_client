# 学生选课管理系统-客户端

#### 介绍
vue 2.6.11 学生选课管理系统
#### 配置环境
1. Nvm1.1.10
2. Node 8.12.0
#### 开发工具
1. IntelliJ IDEA 2022.3.2
2. Git 2.24.1
#### 开发环境
Windows
#### 安装教程
+ 你可以在package.json的父目录执行下如命令 或者 直接在IDEA里点击也可运行 值得一提的是醉后一个命令是打包命令
```
npm install
```
```
npm run serve
```
```
npm run build
```
#### 包的结构
```agsl
 +- student_client
     +- public -- 公共的静态资源文件夹 不需要经过 Webpack 打包处理
        +- favicon.ico -- 网站的图标
        +- index.html -- 项目的默认页面 整个应用的入口页面
     +- src
        +- assets -- 静态资源文件 如图片、字体等
        +- components -- Vue 组件
        +- plugins -- 插件
        +- router -- 路由配置
        +- store -- Vuex 状态管理模式
        +- views -- 页面级组件
        +- App.vue -- 根组件 协调整个应用程序的视图和管理应用程序的状态
        +- main.js -- 项目的入口文件
     +- .gitignore -- 指定需要 Git 忽略的文件或目录
     +- babel.config.js -- 配置 Babel 编译器的 JavaScript 配置文件
     +- LICENSE -- 开源软件的授权协议
     +- packge.json -- 项目元数据的文件 用于描述 Node.js 应用程序或模块的属性
     +- packge-lock.json -- 锁定当前安装的包的版本号和依赖关系
     +- READE.md -- 项目的相关信息文档
```

#### 拓展知识

1. babel.config.js的作用
```
babel.config.js 是用来配置 Babel 编译器的 JavaScript 配置文件，主要用于将新版本的 JavaScript 代码转换为低版本的 JavaScript 代码，从而实现浏览器兼容性。在 Vue 项目中，Babel 被用来转换 ES6/ES2015+ 代码到 ES5 代码，这样浏览器就可以支持这些新的 JavaScript 特性。

在 babel.config.js 文件中，可以配置 Babel 的插件和预设，以及其他选项，如：

presets：指定一组预设，用来转换代码。
plugins：指定一组插件，用来扩展 Babel 的功能。
include：指定需要进行 Babel 转换的文件目录。
exclude：指定不需要进行 Babel 转换的文件目录。
总之，babel.config.js 的作用是帮助开发者在项目中使用最新的 JavaScript 特性，同时确保代码可以在大多数浏览器中运行。

```
2. packge.json的作用

```
package.json 是一个包含项目元数据的文件，用于描述 Node.js 应用程序或模块的属性。它通常位于项目的根目录下，并且是每个 Node.js 项目的必备文件之一。其主要作用包括：

1. 用于记录应用程序或模块的名称、版本、描述、作者、许可证等元数据信息。
2. 定义项目的依赖项和开发依赖项，以及它们的版本号和版本范围。
3. 定义脚本命令，以便于在项目中使用 npm 执行一些常见的任务，例如测试、构建、运行等。
4. 允许其他人轻松地了解你的项目，并根据其信息进行安装、使用、修改或贡献。
在一个 Vue 项目中，package.json 文件通常会包含有关 Vue.js 的相关依赖以及其他与项目相关的依赖信息。
通常情况下，你可以通过修改 package.json 文件中的依赖项来安装新的依赖项或更新现有的依赖项。同时，
你也可以在其中定义一些自定义的脚本命令来运行你的 Vue.js 项目的不同构建任务，例如打包、测试等。
```
3. packge-lock.json

```
package-lock.json 文件是 npm5+ 版本引入的一种新的文件，用于锁定当前安装的包的版本号和依赖关系，确保团队中每个人在使用相同的依赖版本时，构建的结果始终一致。它记录了包的版本、依赖关系和下载地址等信息，防止因为依赖关系不一致而导致的构建失败、安装包版本不一致等问题。

package-lock.json 文件会在 npm install 命令执行时自动生成和更新。当安装依赖时，npm会查找 package.json 中所列出的依赖包和版本，然后将这些依赖包及其依赖包的依赖包下载并安装到本地的 node_modules 目录中，并在生成 package-lock.json 文件时记录这些依赖包的版本和依赖关系。当其他开发者下载这个项目时，只需要运行 npm install 命令就可以安装相同版本的依赖包，以保证开发环境的一致性。
```