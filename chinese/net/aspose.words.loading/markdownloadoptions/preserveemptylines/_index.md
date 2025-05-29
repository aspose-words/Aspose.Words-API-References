---
title: MarkdownLoadOptions.PreserveEmptyLines
linktitle: PreserveEmptyLines
articleTitle: PreserveEmptyLines
second_title: Aspose.Words for .NET
description: 了解 MarkdownLoadOptions PreserveEmptyLines 属性如何通过保留空行来提高可读性，从而增强 Markdown 文档的加载。
type: docs
weight: 30
url: /zh/net/aspose.words.loading/markdownloadoptions/preserveemptylines/
---
## MarkdownLoadOptions.PreserveEmptyLines property

获取或设置一个布尔值，指示是否在加载时保留空行Markdowndocument. 默认值为`错误的`.

通常情况下，Markdown 中块级元素之间的空行会被忽略。文档开头和结尾的空行也会被忽略。此选项允许导入此类空行。

```csharp
public bool PreserveEmptyLines { get; set; }
```

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
