# v-if

条件付きレンダリングをするもの。
v-if は IF 文と思えばよい。条件分岐ができる。

```html
<script src="https://cdn.jsdelivr.net/npm/vue@2.6.7/dist/vue.js"></script>

<div id="app">
  <p v-if="OK">OK!</p>
</div>
```

```javascript
new Vue({
  el: "#app",
  data: {
    OK: true
  }
});
```

# v-else

v-if のあとにすぐ v-else を入れると組み合わせて使える

```html
<script src="https://cdn.jsdelivr.net/npm/vue@2.6.7/dist/vue.js"></script>

<div id="app">
  <p v-if="OK">OK!</p>
  <p v-else>Not OK....</p>
</div>
```

# v-else-if

普通にこういった使い方もできる

```html
<p v-if="OK">OK!</p>
<p v-else-if="maybeOk">maybe OK!</p>
<p v-else>Not OK....</p>
```
