<span id="home"><span/>
1.  JavaScript 程序的执行单位为行（line），也就是一行一行地执行。
2.	var用来声明变量（可不写但不提倡），如果只是声明变量而没有赋值，则该变量的值是undefined。undefined是一个特殊的值，表示“无定义”。
3.	JavaScript 是一种动态类型语言，也就是说，变量的类型没有限制，变量可以随时更改类型。
4.	变量提升：JavaScript 引擎的工作方式是，先解析代码，获取所有被声明的变量，然后再一行一行地运行（隐式全局变量不提升）。
5.	JavaScript 使用大括号，将多个相关的语句组合在一起，称为“区块”（block）。对于var命令来说，JavaScript 的区块不构成单独的作用域（scope）。
6.	==：相等运算符，不建议使用；===：严格相等运算符，不会发生类型转换。
7.	JavaScript中的if、switch、for、while、do…while、break、continue语句结构及作用与C++一致。标签通常与break语句和continue语句配合使用，跳出特定的循环。
8.	数据类型：数值（number）、字符串（string）、布尔值（boolean）、undefined、null、对象（object）。对象又分为：狭义的对象（object）、数组（array）、函数（function）。
9.	JavaScript 有三种方法，可以确定一个值到底是什么类型：
    *	typeof运算符
    *	instanceof运算符
    *	Object.prototype.toString方法
10.	JavaScript 内部，所有数字都是以64位浮点数形式储存，即使整数也是如此。
11.	NaN不等于任何值，包括它本身。NaN与任何数（包括它自己）的运算，得到的都是NaN。
12.	字符串内部的单个字符无法改变和增删，这些操作会默默地失败。
13.	属性的查看：Object.keys(obj);
14.	判断某个属性是否为对象自身的属性：obj.hasOwnProperty(key);
15.	with语句：操作同一个对象的多个属性时，提供一些书写的方便。（不建议使用，推荐用一个临时变量代替with）。
16.	原始类型的值（数值、字符串、布尔值），传递方式是传值传递（passes by value）；复合类型的值（数组、对象、其他函数），传递方式是传址传递（pass by reference）。（注意，如果函数内部修改的，不是参数对象的某个属性，而是替换掉整个参数，这时不会影响到原始值。）
17.	JavaScript允许函数又不定数目的参数，arguments对象包含了函数运行时的所有参数;它不是数组；严格模式下（use strict），修改arguments对象不会影响到实际的函数参数。
18.	可以把闭包简单理解成“定义在一个函数内部的函数”。在本质上，闭包就是将函数内部和函数外部连接起来的一座桥梁。闭包的最大用处有两个，一个是可以读取函数内部的变量，另一个就是让这些变量始终保持在内存中，即闭包可以使得它诞生环境一直存在，闭包还有一个用处，就是封装对象的私有属性和私有方法。
19.	“立即调用的函数表达式”（Immediately-Invoked Function Expression），简称 IIFE。它的目的有两个：一是不必为函数命名，避免了污染全局变量；二是IIFE内部形成了一个单独的作用域，可以封装一些外部无法读取的私有变量。
20.	如果使用严格模式（use strict），eval内部声明的变量，不会影响到外部作用域，但是依然可以读写当前作用域的变量。
21.	关于三次异或交换值的底层原理：交换两个数，就是它们的二进制数不一样的位数，只要各自取反(0变1，1变0)就行了。
22.	虽然在JavaScript内部，数值都是以64位浮点数的形式储存，但是做位运算的时候，是以32位带符号的整数进行运算的，并且返回值也是一个32位带符号的整数。
23.	void运算符的作用是执行一个表达式，然后不返回任何值，或者说返回undefined。主要用途是浏览器的书签工具（Bookmarklet），以及在超级链接中插入代码防止网页跳转。
24.	逗号运算符用于各表达式求值，并返回最后一个表达式的值。
25.	除了以下五个值，其他都是自动转为true。
    * undefined
    *	null
    *	+0或-0
    *	NaN
    *	''（空字符串） 
26.	catch代码块之中，触发转入finally代码块的标志，不仅有return语句，还有throw语句。
27.	建议switch…case结构可以用对象结构代替。
28.	configurable为false时，value、writable、enumerable和configurable都不能被修改了。configurable还决定了目标属性是否可以被删除（delete）。
29.	有时需要冻结对象的读写状态，防止对象被改变。JavaScript 提供了三种冻结方法，最弱的一种是Object.preventExtensions，其次是Object.seal，最强的是Object.freeze。

[跳转到文章开头](#home)
