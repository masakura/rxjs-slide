### Angular2
* Angular2 では Ajax リクエストなどで Promise (Q) ではなく、RxJS が使われています
  - [Angular2のHttpモジュールを眺めてベストプラクティスを考える](http://qiita.com/laco0416/items/364c5923f77458c468ac)

```javascript
this.http.get('http://...')
  .retry(5)
  .map(response => response.json())
  .subscribe(data => {
    // ...
  });
```
