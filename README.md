# development-complex
開発に関する要点
```js
```
共通関数。
```
共通関数は大きく二つ。
fn.xxx:頻度の高い操作
is.xxx:判定も関数化する。
```
全体オブジェクト。
```
外部に一つが望ましい。
let app={}
```
全体オブジェクトへの追加。
```
一つの全体オブジェクトに対して追加を行う。
機能単位でクロージャーで囲う。
初期化が必要な場合はもう一つ関数が増える。
HTMLを使う表示部分と計算部分は別の関数とし、表示部から計算関数を呼ぶ。
;(function(app){

 app.xyzcalc=()=>{ ...Dont DOM }
 app.xyz=()=>{ ... }
 app.xyzInit=()=>{ ... }
})(app);
```
開始関数
```
開始関数は一つのみ。asyncを付けるとネストの深さを緩和できる。
app.init=async ()=>{
 await xxxx
 await xxxx
}
app.init();////////////////
```
エラー表示
```
throw new TypeErrorかreturn console.logを使う。
前者推奨
 throw new TypeError('xyz');
 return console.log('xyz');
```
要素
```
要素は必ずラッパーを被せる。特にimgのようなafter要素を使用出来ない要素は必ずである。
.wrap
 .ed
.wrap
 img
```
