### Collection utility for ES6 iterator

https://github.com/masakura/iterable-collection

```
var iterable = require('iterable-collection');

var result = iterable(sequence)
  .map(i => i * 2)
  .filter(i => i > 5);
```

* まだ `map` `filter` `some` `every` のみ
* バグたくさんあるけど!
  - 構造的にパフォーマンスが悪い
* まだリリースしてないけど!
