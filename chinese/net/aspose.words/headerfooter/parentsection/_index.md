---
title: HeaderFooter.ParentSection
linktitle: ParentSection
articleTitle: ParentSection
second_title: Aspose.Words for .NET
description: 发现 HeaderFooter ParentSection 属性可以轻松访问故事的父部分，增强文档的结构和组织。
type: docs
weight: 60
url: /zh/net/aspose.words/headerfooter/parentsection/
---
## HeaderFooter.ParentSection property

获取此故事的父部分。

```csharp
public Section ParentSection { get; }
```

## 评论

`ParentSection`相当于[`ParentNode`](../../node/parentnode/)投放到[`Section`](../../section/)。

## 例子

展示如何链接各部分之间的页眉和页脚。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

// 移动到第一部分并创建页眉和页脚。默认情况下，
// 页眉和页脚只会出现在包含它们的部分的页面上。
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// 我们可以将一个部分的页眉/页脚链接到前一部分的页眉/页脚
// 允许链接部分显示被链接部分的页眉/页脚。
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// 每个部分仍将拥有自己的页眉/页脚对象。当我们链接部分时，
// 链接部分将显示链接部分的页眉/页脚，同时保留其自己的页眉/页脚。
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// 将第三部分的页眉/页脚链接到第二部分的页眉/页脚。
// 第二部分已经链接到第一部分的页眉/页脚，
// 因此链接到第二部分将创建一个链接链。
// 第一、第二和现在的第三部分都将显示第一部分的标题。
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// 我们可以在调用 LinkToPrevious 方法时传递“false”来取消链接前一节的页眉/页脚。
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// 我们还可以使用此方法仅选择特定类型的页眉/页脚进行链接。
// 第三部分现在将具有与第二部分和第一部分相同的页脚，但没有页眉。
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// 第一节的页眉/页脚无法链接到任何内容，因为没有前一节。
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// 所有第二部分的页眉/页脚都链接到第一部分的页眉/页脚。
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// 在第三部分中，只有页脚通过第二部分链接到第一部分的页脚。
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### 也可以看看

* class [Section](../../section/)
* class [HeaderFooter](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
