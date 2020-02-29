# v-for を使うときは Key 属性をつける

v-for の問題点は、要素の色を最小限に抑えるアルゴリズムを使用し、可能な限り同じタイプの要素を再利用しようとする。

key を付与しておくことで、グループごと削除したりできる、  
ただし、template タグでは key 属性はつかえないので、div を使う。
とにかく、v-for を使うときは、必ず Key 属性を使用するようにする！

```html
<script src="https://cdn.jsdelivr.net/npm/vue@2.6.7/dist/vue.js"></script>

<div id="app">
  <ul>
    <li v-for="(fruit, i) in fruits">({{ i }}){{ fruit }}</li>
  </ul>
  <ul>
    <template v-for="fruit in fruits">
      <li>{{fruit}}</li>
      <hr />
    </template>
  </ul>
  <ul>
    <li v-for="n in 10">{{n}}</li>
  </ul>
</div>
```

```javascript
new Vue({
  el: "#app",
  data: {
    fruits: ["りんご", "ばなな", "ぶどう"]
  },
  methods: {
    remove: function() {
      this.fruits.shift();
    }
  }
});
```
