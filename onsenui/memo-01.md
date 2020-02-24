数日前に初めて monaca で Onsen UI を触ってみましたので、ほんの少しだけタグ中心のメモ

## Onsen UI とは
アプリ開発の際に画面を作成するためのフレームワークだそうな。

## 各種タグや処理の説明
### <ons-navigator>
複数のHTML ファイルを操作する役割を持つ。画面上には表示されない。また、次ページ前ページへのページ遷移機能も持っている。

```html
<ons-navigator page="初期表示ページ"></ons-navigator>
```

### <ons-page>
Onsen UI でページを定義するために必要なタグとなる。
```html
<ons-page>
  ・
  　・
  　・
  ・
</ons-page>
```

### <ons-toolbar>
画面上部に表示されるツールバー。
```html
    <ons-toolbar>
        <div class="center">画面１</div>
    </ons-toolbar>
```

### <ons-button>
画面に表示されるボタン。
```html
        <ons-button> OKボタン</ons-button>
```

OKボタン押下でページ遷移する場合
```html
<ons-button onclick="document.getElementById('id').pushPage('B.html')">
OKボタン
</ons-button>
```

TOP画面に戻る。内部で保持していたページの履歴もリセットされる。
```html
<ons-button onclick="document.getElementById('id').resetToPage('TOP.html')">
TOPボタン
</ons-button>
```

### <ons-back-button>
前の画面に戻るボタン。
```html
<ons-back-button>Back</ons-back-button>
```


### <ons-list>と<ons-listi-tem>
リスト形式でデータを一覧表示するためのタグ。リスト内のデータを1件ずつ扱う場合は、<ons-listitem>。

```html
<ons-list>
 <ons-list-item>項目１</ons-list-item>
 <ons-list-item>項目２</ons-list-item>
 <ons-list-item>項目３</ons-list-item>
</ons-list>
```

### 初期処理
Onsen UI でのInit処理。
```javascript
document.addEventListener("init", function(event) {
 if (event.target.id == "ページの ID") {
 //ページの初期処理
 }
});
```

