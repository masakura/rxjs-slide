### `iterable` が扱える

```javascript
var sequence = {
  [Symbol.iterator]: function* () {
    for (var i = 0; i < 3; i++) {
      yield i;
    }
  }
};

// 1
// 9
Rx.Observable.from(sequence)
  .filter(i => i % 2)
  .map(i => i * i)
  .subscribe(i => console.log(i));
```

* LINQ と違い `subscribe` 関数で結果を受け取る (購読)
