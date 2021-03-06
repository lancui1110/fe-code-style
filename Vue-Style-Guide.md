# Vue-Style-Guide

### 1 Vue属性书写顺序

```javascript
export default {
  mixins,
  data,
  props,
  store，
  computed，
  route,
  created，
  ready，    // => 生命周期顺序不赘述
  event,
  watch,
  components,
  methods
}
```



### 2 组件

#### 2.1 命名

组件以驼峰命名

```html
<template>
  <my-components></my-components>
</template>
<script>
  import myComponents from './myComponents.vue'

  export default {
  components: {
  	  myComponents
    }
  }
</script>

```
#### 2.2 Vue组件的书写顺序
建议：template script style 的顺序书写
```vue
<template></template>
<script></script>
<style></style>
```
#### 2.3 组件引用

```javascript
  import myComponentsA from './myComponentsA.vue'  
  import myComponentsB from './myComponentsB.vue'
  import myComponentsC from './myComponentsC.vue'
  import myComponentsD from './myComponentsD.vue'
  export default {
    components: {
  	  myComponentsA,
      myComponentsB,
      myComponentsC,
      myComponentsD,
    }
  }
```

### 3 事件

```html
<!-- bad -->
<a v-on:click="pass()">pass</a>

<!-- good -->
<a @click="pass">pass</a>
```

### 4 开发命名规则:
```
1、文件夹：驼峰，首字母小写，如：siteAddress，尽量简洁
2、.js文件规则：驼峰，首字母小写，如：siteAddress.js，尽量简洁
3、.vue文件：大驼峰，首字母大写，如：SiteAddress
4、方法名：驼峰，首字母小写，如：handleAdd
```