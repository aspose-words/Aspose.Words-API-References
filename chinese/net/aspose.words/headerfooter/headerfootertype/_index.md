---
title: HeaderFooter.HeaderFooterType
linktitle: HeaderFooterType
articleTitle: HeaderFooterType
second_title: Aspose.Words for .NET
description: 发现 HeaderFooterType 属性可以轻松访问和管理文档的页眉和页脚类型，以增强格式控制。
type: docs
weight: 20
url: /zh/net/aspose.words/headerfooter/headerfootertype/
---
## HeaderFooter.HeaderFooterType property

获取此页眉/页脚的类型。

```csharp
public HeaderFooterType HeaderFooterType { get; }
```

## 例子

展示如何创建页眉和页脚。

```csharp
Document doc = new Document();

// 创建标题并在其后附加一个段落。该段落中的文本
// 将出现在本节每一页的顶部，正文上方。
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// 创建页脚并在其后附加一个段落。该段落中的文本
// 将出现在本节每一页的底部，正文下方。
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

* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooter](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
