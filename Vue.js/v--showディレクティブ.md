# v-show ディレクティブとは

v-if とほぼほぼ一緒。
けど、ソースの検証をみると違いがわかる。
v-if は表示させないときは完全に消せるけど、v-show だと要素が残ってる。

## v-show の悪い特徴

template タグを使えない。
template タグに v-show 入れてしまうと、残ってしまう。
また、v-else 的なものがないということ。

## v-show の存在意義は？

v-show は初期描画が遅い。

# v-for ディレクティブについて

リストのように表示させたいときに使う。

```html
<script src="https://cdn.jsdelivr.net/npm/vue@2.6.7/dist/vue.js"></script>

<div id="app">
  <ul>
    <li v-for="fruits in fruits">{{ fruits }}</li>
  </ul>
</div>
```

```javascript
new Vue({
  el: "#app",
  data: {
    fruits: ["りんご", "ばなな", "ぶどう"]
  }
});
```

# v-for でインデックスとれる

こんな感じで定義すればインデックスがとれる。  
i の部分

```html
<script src="https://cdn.jsdelivr.net/npm/vue@2.6.7/dist/vue.js"></script>

<div id="app">
  <ul>
    <li v-for="(fruit, i) in fruits">({{ i }}){{ fruit }}</li>
  </ul>
</div>
```

# v-for でオブジェクトをレンダリング

object で定義した Key-Value の Value が取得できる

```html
<div id="app">
  <ul>
    <li v-for="(fruit, i) in fruits">({{ i }}){{ fruit }}</li>
  </ul>
  <ul>
    <li v-for="value in object">{{value}}</li>
  </ul>
</div>
```

```javascript
new Vue({
  el: "#app",
  data: {
    fruits: ["りんご", "ばなな", "ぶどう"],
    object: {
      firstName: "太郎",
      lastName: "田中",
      age: 21
    }
  }
});
```

# v-for のオブジェクトの引数

key や index を取得する方法

```html
<script src="https://cdn.jsdelivr.net/npm/vue@2.6.7/dist/vue.js"></script>

<div id="app">
  <ul>
    <li v-for="(fruit, i) in fruits">({{ i }}){{ fruit }}</li>
  </ul>
  <ul>
    <li v-for="(value, key, index) in object">{{index}}:{{key}}--{{value}}</li>
  </ul>
</div>
```

# v-for で template たぐ

例えばリストに 1 行ずつ線を引きたいときなど、template タグでグルーピングすることでできる。

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
</div>
```

# v-for から整数値を取得

v-for からただただた整数値をレンダリングすることも可能

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
