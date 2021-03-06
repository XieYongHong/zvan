# 背景

* 从业务角度看，公司业务已经成长到一定的规模，共性的地方很多，需要复用，原有的技术不足以支撑业务复用；
* 从产品角度看，在之后的产品设计中，产品会遵循一定的规范设计，需要保证公司产品的一致性；
* 从开发效率角度看，需要快速响应业务开发；
* 从维护角度看，统一的代码规范管理；
* 从技术角度看，统一的技术栈，利于跨项目开发；
# 前端技术栈
> vue 2.0 + ES6/7 + axios + element-ui + echarts +  sass + openlayers5
# 组件的设计

##  设计原则

### 就近原则

* 依赖的静态资源，在static中放入同名文件夹
* 先关子组件放在同级目录

### 高复用性

* 标签级别的复用
* 业务级别的复用

### 分层设计思想

* 通过分层设计思想设计复杂的组件

### 灵活拓展

* 组件设计要尽量灵活可拓展，除了提供丰富的props，还可以利用slot插槽完成用户个性化定制需求
* render函数 && jsx

## 开发规范


### 目录设计
````````

├── zvan_ep_ui                  // 项目名称
    ├── packages                // 组件文件
    │    ├── src                // vue组件
    │    └── xxx.js             // vue组件注册
    └── util                    // 公共js

````````
### 代码编写规范

* 尽量使用语义化标签(按钮就是用button标签，别使用div等其它标签)
* js规范([airbnbJS 代码规范](https://www.jianshu.com/p/221d55a9170c)、ESLint)
* [css规范](https://www.cnblogs.com/makai/p/9002898.html)(sass、less、stylus)
* vue组件规范(mixin函数、vuex、router等；组件样式使用scope或者BEM命名规范)
* 遇到相同的结构考虑抽象组件
* 方法以及变量加注释

### 文档和测试

单元测试是为了保证组件库在后续的开发维护的稳定性，降低人工测试的成本

* 每个组件要有详细的使用文档以及示例
* 需要完整的单元测试
* 测试工具 [karma](https://www.jianshu.com/p/49707d15c529)
* 测试框架 [mocha](https://www.liaoxuefeng.com/wiki/001434446689867b27157e896e74d51a89c25cc8b43bdb3000/00147203593334596b366f3fe0b409fbc30ad81a0a91c4a000)
* 断言工具 [chai](https://www.jianshu.com/p/ad59cfd158d4)
* 编写测试脚本

