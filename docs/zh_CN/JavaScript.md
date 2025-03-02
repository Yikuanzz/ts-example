## 介绍

### 关于 JavaScript

**JavaScript** 是一门跨平台、面向对象的脚本语言，它能使网页可交互（例如，拥有复杂的动画、可点击的按钮、弹出菜单等）。

- ***客户端 JavaScript*** 通过提供控制浏览器及其***文档对象模型*（DOM）**的对象对核心语言进行扩展。
- ***服务器端 JavaScript*** 则通过提供和在服务器上运行 JavaScript 有关的对象对核心语言进行扩展。



### ECMAScript 规范

JavaScript 的标准化组织是 [Ecma 国际](https://ecma-international.org/)——这个欧洲标准化信息与通信系统协会提供基于 Javascript 的标准化、国际化编程语言（ECMA 原先是欧洲计算机制造商协会的首字母缩写）。这个名为 ECMAScript 的 JavaScript 标准化版本，在所有支持该标准的应用程序中以相同的方式工作。公司可以使用开放标准语言来开发其 JavaScript 实现。ECMAScript 标准的文档位于 ECMA-262 规范中。



## 语法与数据类型

### 语法规则

1、JavaScript 是**区分大小写**的，并使用 **Unicode** 字符集。

2、**注释**语法和 C++ 以及许多其他语言的注释语法一样。

3、在 JavaScript 中，指令被称为[语句](https://developer.mozilla.org/zh-CN/docs/Glossary/Statement)，并用分号（;）进行分隔。



### 声明

`var`：声明一个变量，可选择将其初始化为一个值。

`let`：声明一个块级作用域的局部变量，可选择将其初始化为一个值。

`const`：声明一个块级作用域的只读命名常量。



### 变量作用域

**全局作用域**：在脚本模式中运行的所有代码的默认作用域。

**模块作用域**：在模块模式中运行的代码的作用域。

**函数作用域：**由[函数](https://developer.mozilla.org/zh-CN/docs/Glossary/Function)创建的作用域。

此外，用 `let` 或 `const` 声明的变量属于另一个作用域：

- 块级作用域：用一对花括号创建的作用域（块）。



### 变量提升

用 `var` 声明的变量会被提升，可以在该变量所在的任意地方引用。所谓提升，就像是被提升到函数或全局作用域的顶部，因此在声明前访问该变量，值会是 `undefined`。如果是 `let` 或 `const`，那么值会是 `ReferenceError` 引用错误。

```js
console.log(x === undefined); // true
var x = 3;
```

这个代码是没有提升的样子，提升后就是下面的样子：

```js
var x;
console.log(x === undefined); // true
x = 3;
```



### 数据类型

**七种基本数据类型**：`Boolean`、`null`、`undefined`、`Number`、`BigInt`、`String`、`Symbol`、`Object`。

**数字 -> 字符串**：在使用 `+` 运算符的表达式中涉及数字和字符串，JavaScript 会把数字转换成字符串。如果使用其他运算符，则仍然是数字。

**字符串 -> 数字**：`parseInt()`、`parseFloat()` ，另一种方法是使用 `+`（一元加）运算符。比如 `+"1.1"`。



### 字面量

**字面量类型**：数组字面量、布尔字面量、数字字面量、对象字面量、RegExp 字面量、字符串字面量。



**数组字面量** ( 数组字面量创建 `Array` 对象。)

```js
let array = ["Hello", "world"]
const finsh =  ["Lion", , "Angel"];
console.log(finsh);    // [ 'Lion', <1 empty item>, 'Angel' ]
```



**布尔字面量**

```js
let yes = true;
let no = false;
```



**数字字面量**

```js
let decimal = 123	// 十进制由数字组成
let octal = 0232	// 八进制以 0 或 0o、0O 开头
let binary = 0b10101  // 二进制以 0b 或 0B 开头
let hexadecimal = 0xa97   // 十六进制以 0x 或 0X 开头
let bigInt = 0o123n    // 结尾加 n 不允许前缀 0 的八进制
```



**浮点数字面量**

```js
left float1 = 3.1415926
left float2 = .123456789
left float3 = 3.1E+12
left float4 = .1e-23
```



**对象字面量**

```js
// 用花括号括起来
const student = {
    id: 321,
    age: 18,
    name: "小明"
}

// 高级对象
```



**RegExp字面量**

```js
const re = /ab+c/
```



**字符串字面量**

```js
// 字符串个数
console.log("John 的猫".length); // 结果为：7

// 模板字面量
const name = 'Lev', time = 'today';
let template = `你好 ${name}，${time} 过得怎么样？`
```



## 控制流与错误处理

### if...else

```js
if (condition1) {
  statement1;
} else if (condition2) {
  statement2;
} else if (conditionN) {
  statementN;
} else {
  statementLast;
}
```



### swtich

```js
switch (expression) {
  case label1:
    statements1;
    break;
  case label2:
    statements2;
    break;
  // …
  default:
    statementsDefault;
}
```



### try/catch/throw

```js
function doSomethingErrorProne() {
  if (ourCodeMakesAMistake()) {
    throw new Error("消息");
  } else {
    doSomethingToGetAJavaScriptError();
  }
}

try {
    monthName = getMonthName(myMonth); // 可能抛出异常的函数
} catch(e) {
  monthName = "未知";
  logMyErrors(e); // 将异常对象传递给错误处理器（例如，你写的函数）
  // throw e;
} finally {
  closeMyFile(); // 总是关闭资源
}
```



## 循环与迭代

### for

```js
for ([initialExpression]; [condition]; [incrementExpression]){
  statement    
}
```



### do...while

```js
do{
    statement
} while(condition)
```



### while

```js
while (condition){
    statement
}
```



### for...in

```js
for (variable in object){
    statement
}
```



### for...of

```js
for (variable of object){
    statement
}
```



## 函数

### 函数定义

一个**函数定义**（也称为**函数声明**，或**函数语句**）由 `function` 关键字，并跟随以下部分组成：

- 函数名称；
- 函数参数列表，包围在括号中并由逗号分隔。
- 定义函数的 JavaScript 语句，用大括号括起来，`{ /* … */ }`。

> 函数的默认参数是 `undefined`。

参数本质上是**按值**传递给函数的——因此，即使函数体的代码为传递给函数的参数赋了新值，**这个改变也不会反映到全局或调用该函数的代码中**。

但如果参数是**对象**，而函数改变了这个对象的属性，这样的改变对函数外部是可见的。

```js
function myFunc(theArr) {
  theArr[0] = 30;
}

const arr = [45];

console.log(arr[0]); // 45
myFunc(arr);
console.log(arr[0]); // 30
```



### 匿名函数

```js
const square = function(number){
    return number * number;
};

console.log(square(4)); 	// 16
```



### 函数提升

函数提升仅适用于 **函数*声明***，而不适用于函数*表达式*。

下面的代码会报错：

```js
console.log(square(5));

const square = function (n){
    return n * n;
};
```



### 函数作用域

在函数内定义的变量不能在函数之外的任何地方访问，因为变量仅仅在该函数的作用域内定义。相对应的，一个函数可以访问定义在其范围内的任何变量和函数。

```js
// 嵌套函数示例
function getScore() {
  const num1 = 2;
  const num2 = 3;

  function add() {
    return `${name} 的得分为 ${num1 + num2}`;
  }

  return add();
}

console.log(getScore()); 
```



### 闭包

闭包是 JavaScript 中最强大的特性之一。JavaScript 允许函数嵌套，并且内部函数具有定义在外部函数中的所有变量和函数（以及外部函数能访问的所有变量和函数）的完全访问权限。

```js
const createPet = function (name) {
  let sex;

  const pet = {
    // 在这个上下文中：setName(newName) 等价于 setName: function (newName)
    setName(newName) {
      name = newName;
    },

    getName() {
      return name;
    },

    getSex() {
      return sex;
    },

    setSex(newSex) {
      if (
        typeof newSex === "string" &&
        (newSex.toLowerCase() === "male" || newSex.toLowerCase() === "female")
      ) {
        sex = newSex;
      }
    },
  };

  return pet;
};

const pet = createPet("Vivie");
console.log(pet.getName()); // Vivie

pet.setName("Oliver");
pet.setSex("male");
console.log(pet.getSex()); // male
console.log(pet.getName()); // Oliver
```



### 剩余参数

将不确定数量的参数表示为数组：

```js
function multiply(multiplier, ...theArgs){
    return theArgs.map((x)=> multiplier * x)
}

const arr = multiply(2, 1, 2, 3);
console.log(arr); // [2, 4, 6]
```



### arguments 对象

函数的实际参数会被保存在一个类似数组的 arguments 对象中。在函数内，你可以按如下方式找出传入的参数：

```js
arguments[i];
```



### 箭头函数

```js
const a = ["Hydrogen", "Helium", "Lithium", "Beryllium"];

const al = a.map((s) => s.length)

console.log(al); // [8, 6, 7, 9]
```



### 预定义函数

`eval()`：计算以字符串表示的 JavaScript 代码。



## 表达式和运算符





## 数字与字符串





## 日期与时间





## 正则表达式





## 索引集合







## 带键集合



## 处理对象





## Promise





## 迭代器与生成器





## 国际化



## 元编程



## 模块





