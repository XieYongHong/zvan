# 前端代码规范
> 为了让你更加愉快的工作，我们要规范你的代码书写
## Vue 代码规范
---
### **1. 组件命名规范**

>通过 *import* 声明组件时，使用 *PascalCase*（单词字母首写大写命名）

```bash
import MonitoringData from './enterprise_btn/monitoring_data'
components: { MonitoringData }
```
>使用组件时，使用 *kebab-case*（短横线分割命名）

```
<monitoring-data></monitoring-data>
```
### **2. 结构化规范**
>基于vue-cli脚手架的结构化基础划分
```
├── build                             webpack 构建脚本目录
├── config                            webpack 配置目录
├── mock                              mock 数据目录
|   └── data.js
├── src                               项目源码目录
│   ├── main.js                         入口js文件
│   ├── App.vue                         根组件
│   ├── components                      公共组件目录
│   │   └── title.vue
│   ├── assets                          资源目录，这里的资源会被wabpack构建
│   │   ├── css                             公共样式文件目录
│   │   ├── js                              公共js文件目录
│   │   └── img                             图片存放目录
│   ├── routes                          前端路由
│   │   └── index.js
│   ├── store                           应用级数据(state)
│   │   └── index.js
│   └── views                           页面目录
│       ├── hello.vue
│       └── sys                         (针对同模块下,多个文件情况)
|           ├── index.vue
|           └── index2.vue
|
├── static                          纯静态资源，不会被wabpack构建
└── test                            测试文件目录(unit&e2e)
    └── unit                            单元测试
```
### **3. vue文件方法声明顺序**

\- components   
\- props    
\- data     
\- created  
\- mounted  
\- activited    
\- update   
\- beforeRouteUpdate    
\- metods       
\- filter   
\- computed     
\- watch

### **4. 注释规范**

> 代码注释在一个项目的后期维护中显的尤为重要，所以我们要为每一个被复用的组件编写组件使用说明，为组件中每一个方法编写方法说明
>以下情况，务必添加注释

1.公共组件使用说明  
2.各组件中重要函数或者类说明    
3.复杂的业务逻辑处理说明    
4.特殊情况的代码处理说明,对于代码中特殊用途的变量、存在临界值、函数中使用的hack、使用 了某种算法或思路等需要进行注释描述    
5.注释块必须以/\*\*（至少两个星号）开头\*\*/；  
6.单行注释使用//；

* 多行注释
```
<!--公用组件：数据表格
    /**
    * 组件名称
    * @module 组件存放位置
    * @desc 组件描述
    * @author 组件作者
    * @date 2017年12月05日17:22:43
    * @param {Object} [title]    - 参数说明
    * @param {String} [columns] - 参数说明
    * @example 调用示例
    *  <hbTable :title="title" :columns="columns" :tableData="tableData"></hbTable>
      */
    --> 
```

### **5. 编码规范**

> 尽量按照ESLint格式要求编写代码（详细规范在下面JS规范中查看）  
1.使用ES6风格编码源码   
2.组件 props 原子化     
    - 提供默认值    
    - 使用 type 属性校验类型    
    - 使用 props 之前先检查该 prop 是否存在     
3.避免 this.$parent 
4.谨慎使用 this.$refs       
5.无需将 this 赋值给 component 变量     
6.调试信息console.log() debugger 使用完及时删除

## JS规范

