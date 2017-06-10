# VUE-SSR----------NUXT

基于vuejs开发的nuxt库实现服务服务器端渲染
可以去[官网](https://nuxtjs.org/)，选择中文文档，比较详细，

**注意必须是基于vue2.0，
  注意必须是基于vue2.0，
  注意必须是基于vue2.0**
 
如果项目是用vue1.x的小伙伴，查看如何从1.x迁移到2.x，官方提供的`vue-migration-helper`迁移助手,使用npm install vue-migration-helper下载安装，方便快捷

（**使用时需要将配置文件里面找到eslint相关配置项注释掉，不然报错会一片飙红，反正我是这样的**）

下面是一个nuxt的开发模版
|-project
|--pages : 各页面组件，用于生成对应路由，支持嵌套，支持动态路由
|--components ：各组件，用于你自己管理公共组件或非公共组件
|--layouts ：宿主布局页面模板组件，用于你可以把不同的页面指定使用不同的布局
|--assets ：用于webpack编译的各类资源，通常是一些小的资源，如代替雪碧图之类的图片等东西
|--middleware ：中间件，首屏渲染和路由跳转前均执行对应中间件，可以返回promise或直接next（很实用！）
|--plugins ：插件，SPA中用的各类第三方组件和一些node模块都可以在这引入，甚至可以引入自己编写的第三方库
|--store ：内置了vuex，可以直接返回数据模块或返回一个自建vuex根对象，具体要翻文档
|--package.json 
|--nuxt.config.js ：配置如下
|----build ：主要对应Webpack中的各配置项，可以对默认的webpack配置进行扩展
|----cache ：主要对应内置的组件缓存模块 lru-cache 的配置对象，有默认值，可选关闭
|----css ：对应我们在SPA随处引用样式文件的 require 语句
|----dev ：用于自定义配置环境变量，对应之前 webpack.config.js 相关文件中的变量语句
|----env ：同上息息相关
|----generate ：对 generate 命令执行时的行为做一些定制
|----head ：对应 vue-meta 插件的全局配置， vue-meta 用于VUE/SSR程序的文档元信息的管理
|----loading ：用于定制化Nuxt.js内置的进度条组件
|----performance ：用于配置Node.js服务器性能上的配置
|----plugins ：用于管理和应用对应 plugins 文件夹中的插件
|----rootdir ：用于设置 Nuxt.js 应用的根目录（这俩api有很大合并的意义）
|----srcdir ：用于设置 Nuxt.js 应用的源码目录（这俩api有很大合并的意义）
|----router ：用于对 vue-router 的扩展和定制，其中还包括了中间件的配置，但并不完美（后面说）
|----transition ：用于定制Nuxt.js内置的页面切换过渡效果的默认属性值
|----watchers ：用于定制Nuxt.js内置的文件监听模块 chokidar 和webpack的相关配置项
