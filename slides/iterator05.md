### for...in (余談)

昔からある `for...in` は `foreach` と挙動が違う!

```javascript
// 0 1 2
var list = ['今日', 'は', '寒い'];
for (var i in list) {
  console.log(i);
}

// 0 1 2 name
list.name = '発言';
for (var i in list) {
  console.log(i);
}

// 0 1 2 name keyName
Object.prototype.keyName = 'name';
for (var i in list) {
  console.log(i);
}
```

JavaScript の闇の一つ... <!-- .element: class="fragment" data-fragment-index="1" -->
