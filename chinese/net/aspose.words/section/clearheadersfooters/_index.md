---
title: Section.ClearHeadersFooters
second_title: Aspose.Words for .NET API 参考
description: Section 方法. 清除本节的页眉和页脚
type: docs
weight: 120
url: /zh/net/aspose.words/section/clearheadersfooters/
---
## Section.ClearHeadersFooters method

清除本节的页眉和页脚。

```csharp
public void ClearHeadersFooters()
```

### 评论

所有页眉和页脚的文本均已清除，但是[`HeaderFooter`](../../headerfooter/)对象本身不会被删除。

这使得本节的页眉和页脚链接到上一节的页眉和页脚。

### 例子

演示如何清除节中所有页眉和页脚的内容。

```csharp
Document doc = new Document();

Assert.AreEqual(0, doc.FirstSection.HeadersFooters.Count);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("This is the primary header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("This is the primary footer.");

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual("This is the primary header.", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("This is the primary footer.", doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());

// 清空本节中所有页眉和页脚的所有内容。
// 页眉和页脚本身仍然存在，但没有任何内容可显示。
doc.FirstSection.ClearHeadersFooters();

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());
```

### 也可以看看

* class [Section](../)
* 命名空间 [Aspose.Words](../../section/)
* 部件 [Aspose.Words](../../../)


