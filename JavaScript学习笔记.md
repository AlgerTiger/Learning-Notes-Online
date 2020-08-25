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
30. Array：
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
    * 先行断言x（？=y）、先行否定断言x（？！y）
40. JSON对象的严格规定：
    * 复合类型的值只能是数组或对象，不能是函数、正则表达式对象、日期对象。
    * 原始类型的值只有四种：字符串、数值（必须以十进制表示）、布尔值和null（不能使用NaN, Infinity, -Infinity和undefined）。
    * 字符串必须使用双引号表示，不能使用单引号。 
    * 对象的键名必须放在双引号里面。
    * 数组或对象最后一个成员的后面，不能加逗号。
41. JSON对象的方法
    * JSON.stringify()；将一个值转为 JSON 字符串。该字符串符合 JSON 格式，并且可以被JSON.parse方法还原。
    * JSON.parse()；将 JSON 字符串转换成对应的值。
42. JavaScript面向对象编程
    * JavaScript语言的对象体系，不是基于“类”的，而是基于构造函数（constructor）和原型链（prototype）。
    * JavaScript语言使用构造函数（constructor）作为对象的模板。
    * 构造函数的两个特点：
        * 函数体内部使用了this关键字，代表了所要生成的对象实例。
        * 生成对象的时候，必须使用new命令。
    * 构造函数内部使用严格模式时，直接调用构造函数就会报错。
    * new命令的原理：
        * 创建一个空对象，作为将要返回的对象实例。
        * 将这个空对象的原型，指向构造函数的prototype属性。
        * 将这个空对象赋值给函数内部的this关键字。
        * 开始执行构造函数内部的代码。
    * new.target：用于判断函数调用的时候，是否使用new命令。
    * this就是属性或方法“当前”所在的对象。
    *. 关于this的总结：JavaScript 语言之中，一切皆对象，运行环境也是对象，所以函数都是在某个对象之中运行，this就是函数运行时所在的对象（环境）。这本来并不会让用户糊涂，但是 JavaScript 支持运行环境动态切换，也就是说，this的指向是动态的，没有办法事先确定到底指向哪个对象，这才是最让初学者感到困惑的地方。
    * 绑定this的方法：
        * Function.prototype.call()； 另外，call方法的一个应用是调用对象的原生方法。
        * Function.prototype.apply()；接收一个数组作为函数执行时的参数
        * Function.prototype.bind()；将函数体内的this绑定到某个对象，然后返回一个新函数。
    * prototype：JavaScript 继承机制的设计思想就是，原型对象的所有属性和方法，都能被实例对象共享。
    * Object.prototype对象有没有它的原型呢？回答是Object.prototype的原型是null。null没有任何属性和方法，也没有自己的原型。因此，原型链的尽头就是null。
    * instanceof 运算符：返回一个布尔值，表示对象是否为某个构造函数的实例。
    * 封装私有变量：立即执行函数（Immediately-Invoked Function Expression，IIFE）。
    * 获取实例对象obj的原型对象，有三种方法：
        * obj.__proto__
        * obj.constructor.prototype
        * Object.getPrototypeOf(obj)（推荐）
    * 在改变原型对象时，一般要同时设置constructor属性。
    * Object.getOwnPropertyNames方法返回所有键名，不管是否可以遍历。只获取那些可以遍历的属性，使用Object.keys方法。
    * hasOwnProperty方法返回一个布尔值，用于判断某个属性定义在对象自身，还是定义在原型链上。hasOwnProperty方法是 JavaScript 之中唯一一个处理对象属性时，不会遍历原型链的方法。
    * in 运算符和 for...in 循环
    * 严格模式下：
        * 只读属性不可写、不可配置属性不可删除
        * 只设置了取值器的属性不可写
        * 禁止扩展的对象不可扩展
        * eval、arguments不可用作标识名
        * 函数不能有重名的参数
        * 禁止八进制的前缀0表示法
        ---
        * 全局变量显式声明
        * 禁止this关键字指向全局对象
        * 禁止使用fn.callee、fn.caller、fn.arguments,这意味着不能在函数内部得到调用栈了
        * 禁止使用arguments.callee、arguments.caller
        * 禁止删除变量（只有对象的属性，且属性的描述对象的configurable属性设置为true，才能被delete命令删除。）
        * 禁止使用with语句
        * 创设eval作用域
        * arguments不在追踪参数的变化
        ---
        * 非函数代码块不得声明函数（ES6是允许的）
        * 保留字：implements、interface、let、package、private、protected、public、static、yield等
43. 异步操作的模式：
    * 回调函数
    * 事件监听
    * 发布/订阅
44. 异步操作的流程控制：
    * 串行执行
    * 并行执行
    * 并行与串行的结合
45. 定时器：
    * setTimeout()；指定某个函数或某段代码，在多少毫秒之后执行。它返回一个整数，表示定时器的编号，以后可以用来取消这个定时器。
    * setInterval()；指定某个任务每隔一段时间就执行一次，也就是无限次的定时执行。  
    *注意：为了确保两次执行之间有固定的间隔，可以不用setInterval，而是每次执行结束后，使用setTimeout指定下一次执行的具体时间。*
     * clearTimeout()、clearInterval()；传入计数器编号。
46. debounce：防抖动
47. Promise 对象：
   * JavaScript 的异步操作解决方案，为异步操作提供统一接口。它起到代理作用（proxy），充当异步操作与回调函数之间的中介，使得异步操作具备同步操作的接口。Promise 可以让异步操作写起来，就像在写同步操作的流程，而不必一层层地嵌套回调函数。
    * Promise对象的状态：
        * 异步操作未完成（pending）
        * 异步操作成功（fulfilled）
        * 异步操作失败（rejected）
    * Promise 对象的报错具有传递性。
    * Promise 的回调函数属于异步任务，会在同步任务之后执行。但是，Promise 的回调函数不是正常的异步任务，而是微任务（microtask）。它们的区别在于，正常任务追加到下一轮事件循环，微任务追加到本轮事件循环。这意味着，**微任务的执行时间一定早于正常任务**。
48.DOM
    * DOM 是 JavaScript 操作网页的接口，全称为“文档对象模型”（Document Object Model）。它的作用是将网页转为一个 JavaScript 对象，从而可以用脚本进行各种操作（比如增删内容）。
    * 节点（node）的七种类型：
        * Document：整个文档树的顶层节点
        * DocumentType：doctype标签（比如<!DOCTYPE html>）
        * Element：网页的各种HTML标签（比如<body>、<a>等）
        * Attr：网页元素的属性（比如class="right"）
        * Text：标签之间或标签包含的文本
        * Comment：注释
        * DocumentFragment：文档的片段
    * Node属性：
        * Node.prototype.nodeType
        * Node.prototype.nodeName
        * Node.prototype.nodeValue
        *只有文本节点（text）、注释节点（comment）和属性节点（attr）有文本值*
        * Node.prototype.textContent
        * Node.prototype.baseURI
        * Node.prototype.ownerDocument
        * Node.prototype.nextSibling
        * Node.prototype.previousSibling
        * Node.prototype.parentNode
        *一个节点的父节点只可能是三种类型：元素节点（element）、文档节点（document）和文档片段节点（documentfragment）。*
        * Node.prototype.parentElement
        * Node.prototype.firstChild，Node.prototype.lastChild
        * Node.prototype.childNodes
        * Node.prototype.isConnected
    * Node方法：
        * Node.prototype.appendChild()
        * Node.prototype.hasChildNodes()
        * Node.prototype.cloneNode()
        * Node.prototype.insertBefore()
        * Node.prototype.removeChild()
        * Node.prototype.replaceChild()
        * Node.prototype.contains()
        * Node.prototype.compareDocumentPosition()
        * Node.prototype.isEqualNode()，Node.prototype.isSameNode()
        * Node.prototype.normalize()
        * Node.prototype.getRootNode()
    * NodeList可以包含各种类型的节点，HTMLCollection只能包含 HTML 元素节点。
    * 目前，只有Node.childNodes返回的是一个动态集合，其他的 NodeList 都是静态集合。
    * 与NodeList接口不同，HTMLCollection没有forEach方法，只能使用for循环遍历。HTMLCollection实例都是动态集合，节点的变化会实时反映在集合中。
    * ParentNode接口：
        * ParentNode.children
       * ParentNode.firstElementChild
        * ParentNode.lastElementChild
        * ParentNode.childElementCount
        * ParentNode.append()，ParentNode.prepend()
    * ChildNode接口：
        * ChildNode.remove()；从父节点移除当前节点。
        * ChildNode.before()，ChildNode.after()；插入一个或多个同级节点。两者拥有相同的父节点。
        * ChildNode.replaceWith()
    * doucument对象的获取方法：
        * 正常的网页，直接使用document或window.document。
        * iframe框架里面的网页，使用iframe节点的contentDocument属性。
        * Ajax 操作返回的文档，使用XMLHttpRequest对象的responseXML属性。
        * 内部节点的ownerDocument属性。 
    * 有些 HTML 属性名是 JavaScript 的保留字，转为 JavaScript 属性时，必须改名。主要是以下两个：
        * for属性改为htmlFor
        * class属性改为className
    * 文本节点（Text）代表元素节点（Element）和属性节点（Attribute）的文本内容。
    * Text 节点的方法
        * appendData(); deleteData(); insertData()；replaceData()；subStringData()；
        * remove()；
        * splitText()；父元素的normalize方法可以实现逆操作，将它们合并。
    * CSSStyleDeclaration 接口用来操作元素的样式。三个地方部署了这个接口：
        * 元素节点的style属性（Element.style）
        * CSSStyle实例的style属性
        * window.getComputedStyle()的返回值
    * CSS对象的两个静态方法：
        * CSS.escape();用于转移CSS选择器里面的特殊字符。
        * CSS.supports();判断当前环境是否支持某一句CSS规则。
    * window.getComputedStyle()；获取浏览器计算后得到的最终规则。伪元素的样式可以通过此方法获取。
    * CSSRule.type属性返回一个整数值，表示当前规则的类型。最常见的类型有以下几种:
        * 1：普通样式规则（CSSStyleRule 实例）
        * 3：@import规则
        * 4：@media规则（CSSMediaRule 实例）
        * 5：@font-face规则
    * Mutation Observer API 用来监视 DOM 变动。其特点：
        * 它等待所有脚本任务完成后，才会运行（即异步触发方式）。
        * 它把 DOM 变动记录封装成一个数组进行处理，而不是一条条个别处理 DOM 变动。
        * 它既可以观察 DOM 的所有类型变动，也可以指定只观察某一类变动。 
49. DOM 的事件操作（监听和触发），都定义在EventTarget接口。所有节点对象都部署了这个接口，其他一些需要事件通信的浏览器内置对象（比如，XMLHttpRequest、AudioNode、AudioContext）也部署了这个接口。该接口主要提供三个实例方法:
    * addEventListener：绑定事件的监听函数
    * removeEventListener：移除事件的监听函数
    * dispatchEvent：触发事件
50. 事件的传播
   一个事件发生后，会在子元素和父元素之间传播（propagation）。这种传播分成三个阶段：
    * 第一阶段：从window对象传导到目标节点（上层传到底层），称为“捕获阶段”（capture phase）。
    * 第二阶段：在目标节点上触发，称为“目标阶段”（target phase）。
    * 第三阶段：从目标节点传导回window对象（从底层传回上层），称为“冒泡阶段”（bubbling phase）。
    这种三阶段的传播模型，使得同一个事件会在多个节点上触发。
51. Event对象
    * 实例属性
        * Event.bubbles，Event.eventPhase
        * Event.cancelable，Event.cancelBubble，event.defaultPrevented
        * Event.currentTarget，Event.target
        * Event.type
        * Event.timeStamp
        * Event.isTrusted。该事件是否由真实的用户行为产生。
        * Event.detail
    * 实例方法
        * Event.preventDefault()。取消浏览器对当前事件的默认行为。
        * Event.stopPropagation()
        * Event.stopImmediatePropagation()
        * Event.composedPath()
52. throttle是“节流”，确保一段时间内只执行一次，而debounce是“防抖”，要连续操作结束后再执行。
53. Location对象是浏览器提供的原生对象，提供 URL 相关的信息和操作方法。

   
[跳转到文章开头](#home)
<span id="end"></span>
