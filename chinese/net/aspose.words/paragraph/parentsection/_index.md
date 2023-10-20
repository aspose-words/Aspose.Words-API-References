---
title: Paragraph.ParentSection
linktitle: ParentSection
articleTitle: ParentSection
second_title: 用于 .NET 的 Aspose.Words
description: Paragraph ParentSection 财产. 检索父级Section该段落的 在 C#.
type: docs
weight: 200
url: /zh/net/aspose.words/paragraph/parentsection/
---
## Paragraph.ParentSection property

检索父级[`Section`](../../section/)该段落的.

```csharp
public Section ParentSection { get; }
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

* class [Section](../../section/)
* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
