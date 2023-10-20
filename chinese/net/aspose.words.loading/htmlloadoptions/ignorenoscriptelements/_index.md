---
title: HtmlLoadOptions.IgnoreNoscriptElements
linktitle: IgnoreNoscriptElements
articleTitle: IgnoreNoscriptElements
second_title: 用于 .NET 的 Aspose.Words
description: HtmlLoadOptions IgnoreNoscriptElements 财产. 获取或设置一个值指示是否忽略 noscript HTML 元素 默认值为错误的 在 C#.
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

与 MS Word 一样，Aspose.Words 不支持脚本，默认情况下会将 &lt;noscript&gt; elements 的内容加载到生成的文档中。然而，在大多数浏览器中，脚本是受支持的，并且来自 &lt;noscript&gt; 的内容是不可见的。将此属性设置为`真的`强制 Aspose.Words 忽略所有 &lt;noscript&gt; 元素 并帮助生成看起来更接近浏览器中所见内容的文档。

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
