# template タグとは

全く表示されないもの、ただただグループさせるもの。
例えば、v-if を複数選択したい場合、template タグでグルーピングできる。
div タグでもできるけど、ソースに表示されるので、気軽に使うなら template の方が良い。

```html
<script src="https://cdn.jsdelivr.net/npm/vue@2.6.7/dist/vue.js"></script>

<div id="app">
  <template v-if="OK">
    <p>Hello</p>
    <p>Good Bye</p>
    <p>おはよう</p>
  </template>
  <button @click="OK = !OK">
    ボタン
  </button>
</div>
```

```javascript
new Vue({
  el: "#app",
  data: {
    OK: true,
    maybeOk: true
  }
});
```
