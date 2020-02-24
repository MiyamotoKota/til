## Vue の超簡単な構成

### HTML
```html
<!-- ↓↓でVueがインストールされる -->
<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>

<div id="app">
  <p>
    {{message}}
  </p>
</div>
```

### JavaScript（Vueインスタンス）
```javascript

new Vue({
	el: '#app',
  data: {
    message: 'HelloWorld!'
   }
})

```

#app がHTMLで指定したid="app"のところに紐づけれる。

