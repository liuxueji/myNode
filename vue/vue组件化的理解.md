主要从组件定义、组件化优点、使用场景来介绍

### 组件定义

组件化是vue的核心特性之一，就是把一些独立的功能单独提取出来，有独立的函数，方便复用

定义方式有两种：

- 全局定义

  ```
  Vue.component('comp',{
  	template:'<div> children component </div>'
  })
  ```

- 单文件组件定义

  ```
  <template>
  	<div>
  		children component
  	</div>
  </template>
  ```

  

## 组件化优点

提高代码的 复用性、可维护性，使代码结构更清晰、更易于阅读，提高了开发效率

### 组件化使用场景

组件可以分为：页面组件、业务组件、通用组件

组件使用到的技术：属性prop、自定义事件、插槽；主要用于组件通信、扩展

