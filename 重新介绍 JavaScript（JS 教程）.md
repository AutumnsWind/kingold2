引言EDIT
为什么会有这一篇“重新介绍”呢？因为 JavaScript 堪称世界上被人误解最深的编程语言。虽然常被嘲为“玩具语言”，但在它看似简洁的外衣下，还隐藏着强大的语言特性。 JavaScript 目前广泛应用于众多知名应用中，对于网页和移动开发者来说，深入理解 JavaScript 就尤有必要。

先从这门语言的历史谈起是有必要的。在1995 年 Netscape 一位名为 Brendan Eich 的工程师创造了 JavaScript，随后在 1996 年初，JavaScript 首先被应用于 Netscape 2 浏览器上。最初的 JavaScript 名为 LiveScript，后来因为 Sun Microsystem 的 Java 语言的兴起和广泛使用，Netscape 出于宣传和推广的考虑，将它的名字从最初的 LiveScript 更改为 JavaScript——尽管两者之间并没有什么共同点。这便是之后混淆产生的根源。

几个月后，Microsoft 随着 IE 3 推出了一个与之基本兼容的语言 JScript。又几个月后，Netscape 将 JavaScript 提交至 Ecma International（一个欧洲标准化组织）， ECMAScript 标准第一版便在 1997 年诞生了，随后在 1999 年以 ECMAScript 第三版的形式进行了更新，从那之后这个标准没有发生过大的改动。由于委员会在语言特性的讨论上发生分歧，ECMAScript 第四版尚未推出便被废除，但随后于 2009 年 12 月发布的 ECMAScript 第五版引入了第四版草案加入的许多特性。第六版标准已经于2015年六月发布。

注意： 为熟悉起见，从这里开始我们将用 “JavaScript” 替代 ECMAScript 。
与大多数编程语言不同，JavaScript 没有输入或输出的概念。它是一个在宿主环境（host environment）下运行的脚本语言，任何与外界沟通的机制都是由宿主环境提供的。浏览器是最常见的宿主环境，但在非常多的其他程序中也包含 JavaScript 解释器，如 Adobe Acrobat、Photoshop、SVG 图像、Yahoo! 的 Widget 引擎，以及 Node.js 之类的服务器端环境。JavaScript 的实际应用远不止这些，除此之外还有 NoSQL 数据库（如开源的 Apache CouchDB）、嵌入式计算机，以及包括 GNOME （注：GNU/Linux 上最流行的 GUI 之一）在内的桌面环境等等。
