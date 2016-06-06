# aries-design
- ver 1.0

## 样例
- http://gametob.github.io/aries-design/
- http://gametob.github.io/aries-design/dist/uielement.html

## CHANGELOG

[CHANGELOG.md]

##分支
* | - master 【左右结构的后台系统元素及场景分类，皮肤：后台蓝】


## 目录结构
* | - conf  目前包含开发机环境所需的nginx配置文件
* | - src / 源代码包
* | -  | -  *.html 单例页面
* | -  | -  _layout.tpl 页面框架模板
* | -  | -  partial /  页面单例模板
* | -  | -  static  /  静态资源
* | - dist / 编译后的成品 用于调试及发布
* | - vendor / 第三方资源包
* | - node_modules / npm install 生成


## 使用说明

- NPM包安装

````
npm install
````
安装完成后会自动执行 gulp vendor 任务。

- Gulp任务
````
gulp (default)
```` 
>开发时做调试而用 默认会开启watch任务

````
gulp deploy
```` 
> 将dist目录下所有文件发布至分支:gh-pages 即更新 [gametob.github.io/ui-css](http://gametob.github.io/ui-css/)

````
gulp vendor
```` 
> 将package.json中指定的资源包(dependencies) 从 /node_modules 中拷贝至 /vendor

## LESS分类

*｜--- bootstrap 第三方
*｜---｜---variabels mixins（variabels）
*｜---｜---mixins（import mixins）
*｜---｜---theme（主题LESS）
*｜---｜---base（基础类）
*｜---｜---mixins（mixins）
*｜---｜---normalize（normalize）
*｜---｜---utility（responsive/theme/utility）
*｜---｜---components（组件类）
*｜---｜---print（排版）
*｜--- platform
*｜---｜---layout（system layout）
*｜---｜---platform-variables（自定义变量）
*｜---｜---re-panel（自定义面板）
*｜---｜---animation（特殊场景动画）
*｜--- bootstrap.less（import less）最终编译文件