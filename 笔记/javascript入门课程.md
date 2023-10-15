一、javascript简介

```
javascript的基本特点：
1. 轻量级；
2. 是一门解释性脚本语言（代码不进行预编译）；
3. 可插入html页面；
4. 插入html页面后，可以由浏览器执行代码；
```

```
javascript的组成部分：
1. ES，描述了该语言的语法和基本对象；
2. DOM（文档对象模型），描述处理网页内容的方法和接口；
3. BOM（浏览器对象模型），描述与浏览器进行交互的方法和接口；
```



二、javascript用法

```js
//javascript输出：
//1. console.log()：打印到控制台；
//2. window.alert()：弹出警告框；
//3. document.write()：将内容写到html页面；
//4. innerHTML写到html页面；
document.write('hello js!')
```

```js
// 格式化文本
document.write('<h1>hello js!</h1>')
```



三、语句

```
const a = 1 + 3;
表达式（expression）：为了得到返回值的计算式，1 + 3；一定会返回值；
语句（statement）：为了进行某种操作，如赋值；不需要返回值；
```



四、变量

```
变量命名规则：
1. 由字母、数字、下划线、$符号组成；不能以数字开头；
2. 不能是关键字和保留字，如：for、while等；
3. 区分大小写；
4. 不能是算数运算符；

变量命名规范：
1. 变量名必须要有意义；
2. 遵守驼峰命名法；
3. 不建议使用$作为变量名；
```



四、js数据类型

```js
// 注意：在js中变量是没有数据类型的，值才有；ts可以为变量做类型声明；

// typeof 运算符
typeof undefined === 'undefined'	// true
typeof true === 'boolean'			// true
typeof 42 === 'number'				// true     
typeof '42' === 'string'			// true
typeof {a: 1} ===  'object'			// true
typeof null === 'object'			// true
typeof Symbol() === 'symbol'		// true
```

```js
// undefined和null
undefined == null		// true
Number(null)			// 0
Number(undefined)		// NaN

```

```js
// 转化为false的值：
undefined => false
null => false
0 => false
NaN => false
'' => false
// 注意：[]和{}不表示false，而是true
```

```js
// 注意：字符串使用“+”，只会进行拼接，即便是字符串是数字；
const x = '1';
const y = '2';
const z = x + y;	// 12
```

```js
// 字符串的不可变性
var fruit = 'apple';
fruit[0] = 'b'
// 这时候，fruit不会变成'bpple'，因为字符串不可变，只能重新赋值；
```

```js
// 获取字符串的倒数第二个字符；
const name = 'petter park';
const targetLetter = name[name.length - 2];		// r
```



五、使用“==”（相等运算符）时的自动类型转换

```js
// 一、原始类型比较：

1 == true // true
// 等同于 1 === Number(true)

0 == false // true
// 等同于 0 === Number(false)

2 == true // 重点：false
// 等同于 2 === Number(true)

2 == false // 重点：false
// 等同于 2 === Number(false)

'true' == true // 重点：false
// 等同于 Number('true') === Number(true)
// 等同于 NaN === 1

'' == 0 // true
// 等同于 Number('') === 0
// 等同于 0 === 0

'' == false  // true
// 等同于 Number('') === Number(false)
// 等同于 0 === 0

'1' == true  // true
// 等同于 Number('1') === Number(true)
// 等同于 1 === 1

'\n  123  \t' == 123 // 重点：true
// 因为字符串转为数字时，省略前置和后置的空格
```

```js
// 二、对象与原始类型比较：
[1] == 1	// true => Number([1]) == 1;

[1] == '1'	// true => Number([1]) == Number('1');

[1] == true // true => Number([1]) == Number(true);
```

```js
// 三、undefined和null的比较：undefined、null与其他类型的值1比较时，结果都是false；
false == null	// false;
false == undefined	// false;

0 == null	// false;
0 == undefined	// false;

undefined == null	// true;
```

```js
// 四、相等运算符的缺点：违反直觉；
// 注意：“==”和if()中的，是两套比较逻辑；
0 == ''		// true;
0 == '0'	// true;

2 == true	// false;
2 == false 	// false;

false == 'false'	// false;
false == '0'		// true;

false == undefined	// false;
false == null		// false;
null == undefined	// true;

'\t\r\n' == 0		// true;
```



六、自增和自减

```js
let x = 1;
let y = 2;
let z = x++;	// 相当于 x 先赋值给z，然后再执行x = x + 1；
let m = ++y;	// 相当于 y 先执行 y = y + 1，然后再赋值给m；
// z: 1; m: 3;
```























