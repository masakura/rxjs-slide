### イベントをソースに

* ボタンのクリックのような繰り返しっぽいものも扱える
* 入力するたびにコンソールに内容が出力される

```html
<input id="input" type="text">
```

```javascript
Rx.Observable.fromEvent($('#input', 'input'))
  .subscribe(text => {
    // テキストボックスに入力があるたびにここが呼び出される
    console.log(text);
  });
```
