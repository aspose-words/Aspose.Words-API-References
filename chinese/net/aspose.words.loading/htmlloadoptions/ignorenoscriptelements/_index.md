---
title: HtmlLoadOptions.IgnoreNoscriptElements
linktitle: IgnoreNoscriptElements
articleTitle: IgnoreNoscriptElements
second_title: Aspose.Words for .NET
description: 了解 HtmlLoadOptions IgnoreNoscriptElements 属性如何通过控制 noscript 元素来增强 HTML 解析。立即提升您的 Web 性能！
type: docs
weight: 40
url: /zh/net/aspose.words.loading/htmlloadoptions/ignorenoscriptelements/
---
## HtmlLoadOptions.IgnoreNoscriptElements property

获取或设置一个值，指示是否忽略 &lt;noscript&gt; HTML 元素。 默认值为`错误的`.

```csharp
public bool IgnoreNoscriptElements { get; set; }
```

## 评论

与 MS Word 类似，Aspose.Words 不支持脚本，默认情况下会将 &lt;noscript&gt; 元素 的内容加载到生成的文档中。然而，大多数浏览器都支持脚本，因此 &lt;noscript&gt; 的内容不可见。将此属性设置为`真的`强制 Aspose.Words 忽略所有 &lt;noscript&gt; 元素 并帮助生成更接近浏览器中所见的文档。

## 例子

展示如何忽略 &lt;noscript&gt; HTML 元素。

```csharp
const string html = @"
    <html>
      <head>
        <title>NOSCRIPT</title>
          <meta http-equiv=""Content-Type"" content=""text/html; charset=utf-8"">
          <script type=""text/javascript"">
            alert(""Hello, world!"");
          </script>
      </head>
    <body>
      <noscript><p>Your browser does not support JavaScript!</p></noscript>
    </body>
    </html>";

HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions();
htmlLoadOptions.IgnoreNoscriptElements = ignoreNoscriptElements;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), htmlLoadOptions);
doc.Save(ArtifactsDir + "HtmlLoadOptions.IgnoreNoscriptElements.pdf");
```

### 也可以看看

* class [HtmlLoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
