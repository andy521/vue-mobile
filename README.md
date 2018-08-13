# vue-mobile

> 用于native开发的通用脚手架，采用APICloud打包应用，APICloud打包目录是dist目录

## 特性

- 多入口打包：实现项目中遇到单页和多页同时存在的情况
- 通过命令快速生成模块代码：统一模块代码规范，一个module对应一个入口，不用在webpack单独配置入口
- 统一解决移动端点击延迟
- sass支持
- 自动添加浏览器前缀：autoprefixer
- 使用vw实现移动端适配： [查看文档](https://github.com/GavinZhuLei/vue-mobile/blob/v1.1/doc/vw.md)
- 处理移动端1px的解决方案
- 处理元素容器宽高比

## 代码目录

```js
+-- build/                ---webpack打包文件目录
|   --- entry.js               ---获取入口文件
|   --- module.js              ---生成module模块代码，一个module对应一个入口
|   --- plugins.js             ---开发环境webpack插件配置
|   --- plugins.prod.js        ---生产环境webpack插件配置
|   --- webpack.base.conf.js   ---webpack loader配置
|   --- ...
+-- config/               ---webpack打包配置目录
+-- src/                  ---源代码目录
|   +-- assets/                ---资源存放目录
|   +-- components/            ---公用组件
|   +-- modules/               ---项目模块目录
|   |   +-- moudule1                ---项目模块，对应一个入口，可以通过命令自动创建
|   |   |   --- App.vue                   ---根组件
|   |   |   --- main.js                   ---模块入口文件
+-- template/             ---模块模板文件目录
--- index.html            ---html模板文件
+-- static/
|   --- config.xml      --- APICloud打包配置文件
|   +-- script/        --- 本地js文件
|   +-- style/        ---本地样式文件
```

## 安装运行

``` bash
# 安装依赖
npm install

# 生产环境打包压缩
npm run build

# 创建模块，自动在src/modules/下生成模板代码和入口文件
npm run module
```
