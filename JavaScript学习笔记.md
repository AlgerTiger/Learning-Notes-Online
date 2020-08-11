[跳转到文章尾](#end)
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
30.   Array：
* push方法用于在数组的末端添加一个或多个元素，并返回添加新元素后的数组长度；pop方法用于删除数组的最后一个元素，并返回该元素；shift()方法用于删除数组的第一个元素，并返回该元素；unshift()方法用于在数组的第一个位置添加元素，并返回添加新元素后的数组长度。
* push和pop结合使用，就构成了“后进先出”的栈结构（stack）；push()和shift()结合使用，就构成了“先进先出”的队列结构（queue）。
* slice()方法的一个重要应用，是将类似数组的对象转为真正的数组。
* splice()方法用于删除原数组的一部分成员，并可以在删除的位置添加新的数组成员，返回值是被删除的元素。
* map方法将数组的所有成员依次传入参数函数，然后把每一次的执行结果组成一个新数组返回。
* reduce方法和reduceRight方法依次处理数组的每个成员，最终累计为一个值。
* indexOf()，lastIndexOf()
31. Boolean 函数的类型转换作用
* Boolean(undefined) // false
* Boolean(null) // false
* Boolean(0) // false
* Boolean('') // false
* Boolean(NaN) // false
---
* Boolean(1) // true
* Boolean('false') // true
* Boolean([]) // true
* Boolean({}) // true
* Boolean(function () {}) // true
* Boolean(/foo/) // true
32. 使用双重的否运算符（!）也可以将任意值转为对应的布尔值。(例：!!undifined  //false)
33. toString方法只能将十进制的数，转为其他进制的字符串。如果要将其他进制的数，转回十进制，需要使用parseInt方法。
34. Number：
* Number.prototype.toFixed();先将一个数转为指定位数的小数，然后返回这个小数对应的字符串。
* Number.prototype.toExponential();将一个数转为科学计数法形式。
* Number.prototype.toPrecision();将一个数转为指定位数的有效数字。
* Number.prototype.toLocaleString(); 返回一个字符串，表示当前数字在该地区的当地书写形式。
35. 在对象的prototype对象上面自定义方法，从而被对象的实例继承。
36. Stirng：
* 静态方法：String.fromCharCode()；该方法的参数是一个或多个数值，代表 Unicode 码点，返回值是这些码点组成的字符串。
* 实例属性：String.prototype.length；
* 实例方法：
  * String.prototype.charAt()；
  * String.prototype.charCodeAt()；（相当于String.fromCharCode()的逆操作。）
  * String.prototype.concat()；
  * String.prototype.slice()；从原字符串取出子字符串并返回，不改变原字符串。
  * String.prototype.substring()；返回字串，不推荐使用，因为若第一个参数大于第二个参数，参数位置会自动互换，违反直觉。
  * String.prototype.substr()；返回字串，第二个参数是字串长度。
  * String.prototype.indexOf()，String.prototype.lastIndexOf()；
  * String.prototype.trim()；
  * String.prototype.toLowerCase()，String.prototype.toUpperCase()；
  * String.prototype.search()，String.prototype.replace();
  * String.prototype.split();
37. 其他对象求值的时候，都是默认调用.valueOf()方法，但是Date实例求值的时候，默认调用的是toString()方法。
38. Date构造函数的参数：
  * 年：使用四位数年份，比如2000。如果写成两位数或个位数，则加上1900，即10代表1910年。如果是负数，表示公元前。
  * 月：0表示一月，依次类推，11表示12月。
  * 日：1到31。
  * 小时：0到23。
  * 分钟：0到59。
  * 秒：0到59
  * 毫秒：0到999。
39. 正则表达式
  * 元字符：.、^、|、\、*、+、?、()、[]、{}
  * 点字符（.）匹配除回车（\r）、换行(\n) 、行分隔符（\u2028）和段分隔符（\u2029）以外的所有字符。注意，对于码点大于0xFFFF字符，点字符不能正确匹配，会认为这是两个字符。
  * 位置字符
    * ^ 表示字符串的开始位置
    * $ 表示字符串的结束位置
  * 选择符（|）：或关系
  * ^：脱字符
  * -：连字符
  * 字符类：所有可供选择的字符都放在方括号内，比如[xyz] 表示x、y、z之中任选一个匹配。
  * 预定义模式
    * \d 匹配0-9之间的任一数字，相当于[0-9]。
    * \D 匹配所有0-9以外的字符，相当于[^0-9]。
    * \w 匹配任意的字母、数字和下划线，相当于[A-Za-z0-9_]。
    * \W 除所有字母、数字和下划线以外的字符，相当于[^A-Za-z0-9_]。
    * \s 匹配空格（包括换行符、制表符、空格符等），相等于[ \t\r\n\v\f]。
    * \S 匹配非空格的字符，相当于[^ \t\r\n\v\f]。
    * \b 匹配词的边界。
    * \B 匹配非词边界，即在词的内部。
  * 重复类：模式的精确匹配次数，使用大括号（{}）表示。{n}表示恰好重复n次，{n,}表示至少重复n次，{n,m}表示重复不少于n次，不多于m次。
  * 量词符用来设定某个模式出现的次数。
    * ?问号表示某个模式出现0次或1次，等同于{0, 1}。
    * *星号表示某个模式出现0次或多次，等同于{0,}。
    * +加号表示某个模式出现1次或多次，等同于{1,}。
  * 非捕获组：（？：x）,不单独输出括号内不得内容。
  * 
  
  
   
[跳转到文章开头](#home)
<span id="end"></span>
