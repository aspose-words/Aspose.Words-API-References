---
title: Paragraph.IsEndOfHeaderFooter
linktitle: IsEndOfHeaderFooter
articleTitle: IsEndOfHeaderFooter
second_title: Aspose.Words for .NET
description: 探索段落的 IsEndOfHeaderFooter 属性。轻松判断某个段落是否是 HeaderFooter 中的最后一段，从而增强文档结构。
type: docs
weight: 70
url: /zh/net/aspose.words/paragraph/isendofheaderfooter/
---
## Paragraph.IsEndOfHeaderFooter property

如果此段是段落的最后一段，则为 True[`HeaderFooter`](../../headerfooter/) （正文故事）[`Section`](../../section/) ；否则为假。

```csharp
public bool IsEndOfHeaderFooter { get; }
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

* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
