### ということは...

配列で使える map や filter 関数が、iterable でも使えそう! <!-- .element: class="fragment" data-fragment-index="1" -->

```javascript
var list = sequence.filter(i => i % 2).map(i => i * i);
```
<!-- .element: class="fragment" data-fragment-index="2" -->

まんま LINQ や! <!-- .element: class="fragment" data-fragment-index="3" -->
