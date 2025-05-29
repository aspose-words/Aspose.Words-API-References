---
title: MarkdownLoadOptions
linktitle: MarkdownLoadOptions
articleTitle: MarkdownLoadOptions
second_title: Aspose.Words for .NET
description: 发现 MarkdownLoadOptions 构造函数，轻松初始化 MarkdownLoadOptions 实例，以增强文档处理和定制。
type: docs
weight: 10
url: /zh/net/aspose.words.loading/markdownloadoptions/markdownloadoptions/
---
## MarkdownLoadOptions constructor

初始化一个新的实例[`MarkdownLoadOptions`](../)类.

```csharp
public MarkdownLoadOptions()
```

## 评论

自动设置[`LoadFormat`](../../../aspose.words/loadformat/)到Markdown.

## 例子

展示如何在加载文档时保留空行。

```csharp
string mdText = $"{Environment.NewLine}Line1{Environment.NewLine}{Environment.NewLine}Line2{Environment.NewLine}{Environment.NewLine}";
using (MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(mdText)))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { PreserveEmptyLines = true };
    Document doc = new Document(stream, loadOptions);

    Assert.AreEqual("\rLine1\r\rLine2\r\f", doc.GetText());
}
```

### 也可以看看

* class [MarkdownLoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
