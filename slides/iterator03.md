### イテレーター関数

```javascript
var sequence = {
  // <1> イテレーター関数には Symbol.iterator を使う
  [Symbol.iterator]: function() {
    var i = 0;

    // <2> イテレーター関数は next 関数を持つイテレーターオブジェクトを返す
    return {
      // <3> next 関数は value と done プロパティを持つ値を返す
      next: function () {
        if (i < 3) {
          return {value: i++, done: false}
        } else {
          return {done: true}
        }
      }
    }
  }
};

var seq = sequence[Symbol.iterator]();
console.log(seq.next()); // {value: 0, done: false};
console.log(seq.next()); // {value: 1, done: false};
console.log(seq.next()); // {value: 2, done: false};
console.log(seq.next()); // {done: true};
```

* イテレーター関数を持つオブジェクトを `iterable` と呼びます
