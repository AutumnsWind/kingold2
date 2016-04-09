引言EDIT
为什么会有这一篇“重新介绍”呢？因为 JavaScript 堪称世界上被人误解最深的编程语言。虽然常被嘲为“玩具语言”，但在它看似简洁的外衣下，还隐藏着强大的语言特性。 JavaScript 目前广泛应用于众多知名应用中，对于网页和移动开发者来说，深入理解 JavaScript 就尤有必要。

先从这门语言的历史谈起是有必要的。在1995 年 Netscape 一位名为 Brendan Eich 的工程师创造了 JavaScript，随后在 1996 年初，JavaScript 首先被应用于 Netscape 2 浏览器上。最初的 JavaScript 名为 LiveScript，后来因为 Sun Microsystem 的 Java 语言的兴起和广泛使用，Netscape 出于宣传和推广的考虑，将它的名字从最初的 LiveScript 更改为 JavaScript——尽管两者之间并没有什么共同点。这便是之后混淆产生的根源。

几个月后，Microsoft 随着 IE 3 推出了一个与之基本兼容的语言 JScript。又几个月后，Netscape 将 JavaScript 提交至 Ecma International（一个欧洲标准化组织）， ECMAScript 标准第一版便在 1997 年诞生了，随后在 1999 年以 ECMAScript 第三版的形式进行了更新，从那之后这个标准没有发生过大的改动。由于委员会在语言特性的讨论上发生分歧，ECMAScript 第四版尚未推出便被废除，但随后于 2009 年 12 月发布的 ECMAScript 第五版引入了第四版草案加入的许多特性。第六版标准已经于2015年六月发布。

注意： 为熟悉起见，从这里开始我们将用 “JavaScript” 替代 ECMAScript 。
与大多数编程语言不同，JavaScript 没有输入或输出的概念。它是一个在宿主环境（host environment）下运行的脚本语言，任何与外界沟通的机制都是由宿主环境提供的。浏览器是最常见的宿主环境，但在非常多的其他程序中也包含 JavaScript 解释器，如 Adobe Acrobat、Photoshop、SVG 图像、Yahoo! 的 Widget 引擎，以及 Node.js 之类的服务器端环境。JavaScript 的实际应用远不止这些，除此之外还有 NoSQL 数据库（如开源的 Apache CouchDB）、嵌入式计算机，以及包括 GNOME （注：GNU/Linux 上最流行的 GUI 之一）在内的桌面环境等等。

概览EDIT
JavaScript 是一种面向对象的动态语言，它包含类型、运算符、标准内置（ built-in）对象和方法。它的语法来源于 Java 和 C，所以这两种语言的许多语法特性同样适用于 JavaScript。需要注意的一个主要区别是 JavaScript 不支持类，类这一概念在 JavaScript 通过对象原型（object prototype）得到延续（有关 ES6 类的内容参考这里Classes）。另一个主要区别是 JavaScript 中的函数也是对象，JavaScript 允许函数在包含可执行代码的同时，能像其他对象一样被传递。

先从任何编程语言都不可缺少的组成部分——“类型”开始。JavaScript 程序可以修改值（value），这些值都有各自的类型。JavaScript 中的类型包括：

Number（数字）
String（字符串）
Boolean（布尔）
Function（函数）
Object（对象）
Symbol (第六版新增)
…哦，还有看上去有些…奇怪的 undefined（未定义）类型和 null（空）类型。此外还有Array（数组）类型，以及分别用于表示日期和正则表达式的 Date（日期）和 RegExp（正则表达式），这三种类型都是特殊的对象。严格意义上说，Function（函数）也是一种特殊的对象。所以准确来说，JavaScript 中的类型应该包括这些：

Number（数字）
String（字符串）
Boolean（布尔）
Symbol（符号）（第六版新增）
Object（对象）
Function（函数）
Array（数组）
Date（日期）
RegExp（正则表达式）
Null（空）
Undefined（未定义）
JavaScript 还有一种内置Error（错误）类型，这个会在之后的介绍中提到；现在我们先讨论下上面这些类型。

数字EDIT
根据语言规范，JavaScript 采用“IEEE 754 标准定义的双精度64位格式”（"double-precision 64-bit format IEEE 754 values"）表示数字。据此我们能得到一个有趣的结论，和其他编程语言（如 C 和 Java）不同，JavaScript 不区分整数值和浮点数值，所有数字在 JavaScript 中均用浮点数值表示，所以在进行数字运算的时候要特别注意。看看下面的例子：

0.1 + 0.2 = 0.30000000000000004
在具体实现时，整数值通常被视为32位整型变量，在个别实现（如某些浏览器）中也以32位整型变量的形式进行存储，直到它被用于执行某些32位整型不支持的操作，这是为了便于进行位操作。进一步的详细资料可参考 The Complete JavaScript Number Reference。

JavaScript 支持标准的算术运算符，包括加法、减法、取模（或取余）等等。还有一个之前没有提及的内置对象 Math（数学对象），用以处理更多的高级数学函数和常数：
