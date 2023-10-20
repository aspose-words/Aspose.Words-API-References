---
title: HeaderFooter.IsHeader
linktitle: IsHeader
articleTitle: IsHeader
second_title: 用于 .NET 的 Aspose.Words
description: HeaderFooter IsHeader 财产. 如果是这样则为真HeaderFooter对象是一个标头 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words/headerfooter/isheader/
---
## HeaderFooter.IsHeader property

如果是这样则为真[`HeaderFooter`](../)对象是一个标头。

```csharp
public bool IsHeader { get; }
```

## 例子

演示如何创建页眉和页脚。

```csharp
Document doc = new Document();

// 创建一个标题并向其附加一个段落。该段落中的文字
// 将出现在本节每个页面的顶部，主体文本上方。
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// 创建一个页脚并向其附加一个段落。该段落中的文字
// 将出现在本节每个页面的底部，主体文本下方。
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### 也可以看看

* class [HeaderFooter](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
