---
title: HeaderFooter.IsHeader
second_title: Aspose.Words for .NET API 参考
description: HeaderFooter 财产. 如果这个为真 页眉页脚对象是一个标题
type: docs
weight: 30
url: /zh/net/aspose.words/headerfooter/isheader/
---
## HeaderFooter.IsHeader property

如果这个为真 **页眉页脚**对象是一个标题。

```csharp
public bool IsHeader { get; }
```

### 例子

显示如何创建页眉和页脚。

```csharp
Document doc = new Document();

// 创建一个标题并在其上附加一个段落。该段中的文字
// 将出现在本节每一页的顶部，主体文本上方。
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// 创建一个页脚并向其附加一个段落。该段中的文字
// 将出现在本节每一页的底部，主体文本下方。
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
* 命名空间 [Aspose.Words](../../headerfooter/)
* 部件 [Aspose.Words](../../../)


