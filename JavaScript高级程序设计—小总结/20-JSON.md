# JSON

### 小结：

JSON 是一个轻量级的数据格式，可以简化表示复杂数据结构的工作量。JSON 使用 JavaScript 语法
的子集表示对象、数组、字符串、数值、布尔值和 null 。即使 XML 也能表示同样复杂的数据结果，但
JSON 没有那么烦琐，而且在 JavaScript 中使用更便利。

ECMAScript 5 定义了一个原生的 JSON 对象，可以用来将对象序列化为 JSON 字符串或者将 JSON
数据解析为 JavaScript 对象。 JSON.stringify() 和 JSON.parse() 方法分别用来实现上述两项功能。
这两个方法都有一些选项，通过它们可以改变过滤的方式，或者改变序列化的过程。

原生的 JSON 对象也得到了很多浏览器的支持，比如 IE8+、Firefox 3.5+、Safari 4+、Opera 10.5 和
Chrome。