虽然前后端好处有很多，但是由于接口是暴露的，或多或少会存在一些安全性问题，但是还是有办法解决。

### 什么是XSS

Cross-Site-Scripting（跨站脚本攻击）简称XSS（为了和CSS区分，将C换成X），是一种代码注入。攻击者通过为目标网站恶意注入脚本，用户在浏览器中运行时，会执行该脚本，攻击者可以获取到用户敏感信息，如：Cookie、Session等。

> 上面的有些难理解。举个例子：我在掘金网站上对某一篇文章评论，但是评论的内容是一段脚本语句`<script src='http://www.baidu.com'></script>`，然后文章作者点开文章评论内容，然后浏览器检测到评论内容是可执行的脚本语句，会执行，然后就跳转到百度页面了。其中就用到了XSS。当然这只是打个比方

### XSS预防

刚刚我们举例中，XSS攻击有两个要素：

- 攻击者恶意提交代码
- 浏览器恶意执行代码

根据上面的两个要素，我们做相应预防处理：

将用户输入的内容，通过转义成文本，并且替换某些特殊字符（`<script>`等）

> 只需要保证用户输入的是不能被浏览器只需的脚本即可

