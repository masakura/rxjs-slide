### ジェネレーター関数

* イテレーター関数を書くのは面倒なので、`yield` があります!
  - ジェネレーター関数は `function*` と `*` をつけます 

```javascript
var sequence = {
  // <1> イテレーター関数には Symbol.iterator を使う
  [Symbol.iterator]: function* () {
    for (var i = 0; i < 3; i++) {
      yield i;
    }
  }
};
```
