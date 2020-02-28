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
