# Vue-drag-2.0
 适用于vue2.0


## 使用方法
```

NPM
  npm install vue-drag-2.0

页面调用
  import Vue from 'vue'
  import vueDrag from 'vue-drag-2.0'

  Vue.use(vueDrag)
```

## 例子
```
new Vue({
  el: 'body',
  data: {
    list: ['Foo', 'Bar', 'Baz']
  },
  methods: {
    onUpdate: function (event) {
      this.list.splice(event.newIndex, 0, this.list.splice(event.oldIndex, 1)[0])
    }
  }
});
<ul v-sortable="{ onUpdate: onUpdate }">
    <li v-for="item in list">{{ item }}</li>
 </ul>
```
