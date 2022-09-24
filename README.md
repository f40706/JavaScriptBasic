# JavaScriptBasic

:::info
## Chrome
<font color = green>
更多工具 -> 開發人員工具 -> Console
輸入第一個JS指令</br>
    
```javascript!
let js = 'data'
if(js === 'data')
    alert("Hello world!")
```
:::

:::info
## JavaScript版本
ES5</br>
ES=ECMAScript</br>
5巨大改版的第一版</br></br>
ES6 = 2015年發布</br>
2015年後，每年更新一版</br>
ES11 = 2020年發布</br>
ES13 = 2022年發布</br>
:::

:::info
## 在HTML內執行JavaScript
<font color = red>
    不推薦這樣使用，對於維護極為不易，沒有分離關注點
</font>

```htmlembedded=
<!DOCTYPE html>
<html lang="en">

<head>
  
    /*此處是JavaScript*/
  <script>
    let data = '123';
    if (data === '123')
      alert("Hi");
  </script>
</head>

<body>
  <h1>This is body</h1>
</body>

</html>
```
:::

:::info
## 將HTML與JavaScript分離
<font color = red>
    推薦這樣使用，對於維護方便，分離關注點</br>
    HTML呼叫js
</font>
<font color = green>
以下為index_script.js
</font>

```javascript=
const now = 2037;
const ageJonas = now - 1991;
const ageSarah = now - 2018;

console.log(now - 1991 > now - 2018);
alert(century)
```
<font color = green>
以下為index.html
</font>

```htmlembedded=
<!DOCTYPE html>
<html lang="en">

<head>
  ...
</head>

<body>
  <h1>This is body</h1>

  <script src="index_script.js"></script>
</body>

</html>
```
:::

:::info
## 打印方法
console.log(123)</br>
<font color = red>
可以在Chrome開發人員Console內看到打印值
</font>
:::

## 基本語法
:::info
檢查型態</br>
```javascript=
console.log(typeof true)
回傳boolen(原始型態)

//允許宣告不聲明型態
let number;
console.log(typeof number)
回傳undefined

//null回傳為object，應該避開null，是個bug
console.log(typeof null)
回傳object
```

let允許中途轉型態
```javascript=
let data = 123
console.log(typeof data)
data = '34A'
console.log(typeof data)

回傳
number
string
```
</br>
:::

:::info
let、const於ES6開始提供使用
var是舊版本就提供的，應避免使用此，改使用let

```javascript=
const year = 1991;
// year = 1990; //const不能夠中途變更參數
```

<font color=red>
應避免使用var的原因</br>
1. var作用愈是function</br>
    let作用愈是block</br>
    作用愈越大，越不方便檢查
2. 如下程式碼</br>
</font>

```javascript=
//var允許重複宣告這是一個很嚴重的問題
var month = 12;
var month = 11;
console.log(month);

//let不允許重複宣告
let day = 20;
// let day = 23;
console.log(day);
```

不宣告直接使用的變數，作用愈是全域，應避免此方法使用
```javascript=
work = '123'
console.log(work)
```
:::

:::info
js的運算符包含</br>
+加</br>
-減</br>
*乘</br>
/除</br>
**次方</br>
%餘數</br>

比較符</br>
< > <= >= == === != !==</br>

== 與 ===差異是</br>
== 僅需數值相等即可</br>
=== 必須要object也相同(記憶體位置相等的意思)</br>

```javascript=
const age = '18'
if (age == 18) {
    console.log("OK1")
}
if (age === 18) {
    console.log("OK2")
}
//輸出 OK1

if (age != 18) {
    console.log("! OK1")
}
if (age !== 18) {
    console.log("! OK2")
}
//輸出 ! OK2
```

邏輯操作符

!反向，0以外的!後變false，!0會等於true</br>
!-2 = false， !20=false</br>
!0 = true</br>
&&</br>
||</br>

字串運用
```javascript=
let string = "123 " + " 456";
console.log(string);
```

字串引入值方法
```javascript=
let name1 = 'apple';
//使用``
console.log(`string = ${name1}`);
```

字串換行與串接
```javascript=
//\是字串與下一行串接用
//\n是輸出時的換行符號
let string = "1234\n\
2345\n\
3456\n";
console.log(string);

```

允許將結果給予多個變數
```javascript=
let x;
let y;
let z;
z = x = y = 10 + 20 + 30;
console.log(x, y, z);
//輸出60 60 60
```

5個在js判斷為false
```javascript=
// 0, undefined, null, NaN, ''
console.log(Boolean(0))
console.log(Boolean(undefined))
console.log(Boolean(null))
console.log(Boolean(NaN))
console.log(Boolean(''))
```
:::

:::info
String轉Number
```javascript=
const year = '1991'
console.log(typeof Number(year))
console.log(Number(year))
console.log(typeof year)
//輸出 number 1991 string

//轉型失敗會回傳NaN
const fileName = "123.mov"
console.log(Number(fileName))
console.log(typeof NaN)
//輸出 NaN number

//檢查是否是NaN
if (isNaN(Number(fileName))) {
    console.log("is NaN")
}
//輸出is NaN
```
:::

:::info
判斷式用法與Java一樣
if、switch</br>
`let data = xxx > 10 ? true : false`
:::

###### tags: `JavaScript`