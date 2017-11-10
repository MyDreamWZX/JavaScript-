# JavaScript 与 XML

### 小结：

JavaScript 对 XML 及其相关技术有相当大的支持。然而，由于缺乏规范，共同的功能却存在一些不
同的实现。DOM2 级提供了创建空 XML 文档的 API，但没有涉及解析和序列化。既然规范没有对这些
功能作出规定，浏览器提供商就各行其是，拿出了自己的实现方案。IE 采取了下列方式。

  通过 ActiveX 对象来支持处理 XML，而相同的对象也可以用来构建桌面应用程序。

  Windows携带了 MSXML 库，JavaScript 能够访问这个库。

  这个库中包含对基本 XML 解析和序列化的支持，同时也支持 XPath 和 XSLT 等技术。

Firefox 为处理 XML 的解析和序列化，实现了两个新类型，简介如下。

 DOMParser 类型比较简单，其对象可以将 XML 字符串解析为 DOM 文档。

 XMLSerializer 类型执行相反的操作，即将 DOM 文档序列化为 XML 字符串。

由于 Firefox 中的类型比较简单，用户众多，IE9、Opera、Chrome 和 Safari 都相继实现了相同的类
型。因此，这些类型也就成为了 Web 开发中的事实标准。

DOM3 级引入了一个针对 XPath API 的规范，该规范已经由 Firefox、Safari、Chrome 和 Opera 实现。
这些 API 可以让 JavaScript 基于 DOM 文档运行任何 XPath 查询，并且能够返回任何数据的结果。IE 以
自己的方式实现了对 XPath 的支持；具体来说，就是两个方法： selectSingleNode() 和
selectNodes() 。虽然与 DOM3 级 API 相比还存在诸多限制，但使用这两个方法仍然能够执行基本的
XPath 功能，即在 DOM 文档中查找节点或节点集合。

与 XML 相关的最后一种技术是 XSLT，没有公开发布的标准针对这种技术的功能定义相应的 API。
Firefox 为通过 JavaScript 处理转换创建了 XSLTProcessor 类型；此后不久，Safari、Chrome、和 Opera
也都实现了同样的类型。IE 则针对 XSLT 提供了自己的方案，一个是简单的 transformNode() 方法，
另一个是较为复杂的模板/处理器手段。
目前，IE、Firefox、Chrome 和 Opera 都能够较好地支持 XML。虽然 IE 的实现与其他浏览器相比差
异比较大，但仍然还是有较多的公共功能可供我们实现跨浏览器的方案。