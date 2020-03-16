# 构建的琐事杂记


## [webpack](https://www.webpackjs.com/concepts/)


### Node Interface


compiler.run / watch ...

https://webpack.js.org/api/node/#run


### less-loader

https://webpack.js.org/loaders/less-loader/#root
注：css module 特性属于css-loader的功能，在css-loader中配置
https://webpack.js.org/loaders/css-loader/#root


### babel-loader

https://webpack.js.org/loaders/babel-loader/#root

babel文档：https://www.babeljs.cn/docs/

### 代码库的构建

output-traget: https://webpack.js.org/configuration/output/#module-definition-systems

#### package.json

https://docs.npmjs.com/files/package.json

注意配置main入口文件.

中添加 module 字段，打包给在 module 目录下给出分文件打出的代码.
以便tree-shaking. 该字段由webpack支持，不在package.json中.

#### 库中的宿主环境依赖

1、webpack配置中添加externals: https://webpack.js.org/configuration/externals/#externals

2、package.json中添加 peerDependencies

### 依赖包的版本管理

https://docs.npmjs.com/configuring-npm/shrinkwrap-json.html

发布的包所依赖的三方包版本锁定 npm-shrinkwrap.json

项目的依赖包版本锁定 package-lock.json

仅限使用npm命令有效（yarn cnpm 有着自己的缓存与版本更新机制）

## eslint


## typescript

1、直接使用ts-loader: https://webpack.js.org/guides/typescript/#loader

2、使用babel的presets： https://babeljs.io/docs/en/presets#docsNav
好处是可以使用ts同时，使用bale的三方插件, 如：react-hot-loader

## hot load

react-hot-loader : https://www.npmjs.com/package/react-hot-loader

### 可能会用到的 webpack plugin

EnvironmentPlugin

ProgressPlugin

CopyWebpackPlugin 文件的拷贝

HtmlWebpackPlugin

DllPlugin + DefinePlugin

I18nWebpackPlugin





