### イベントをソースに

```javascript
Rx.Observable.fromEvent($('#input', 'input'))
  // 連続で打鍵している間は後続を呼び出さない
  .throttle(300)
  // テキストボックスが空の場合も後続を呼び出さない
  .filter(text => text.length > 0)
  // 前回と値が変わらない時も後続を呼び出さない
  .distinctUntilChanged()
  // 購読する
  .subscribe(text => console.log(text));
````

* これに Ajax リクエストを組み合わせれば、リアルタイム検索ができる
  - 打鍵の感覚が 300ms 開くまでイベントを無視する
