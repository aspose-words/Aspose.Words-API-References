---
title: HeaderFooterCollection.Item
second_title: Aspose.Words for .NET API 参考
description: HeaderFooterCollection 财产. 检索一个 页眉页脚在给定的索引处
type: docs
weight: 10
url: /zh/net/aspose.words/headerfootercollection/item/
---
## HeaderFooterCollection indexer (1 of 2)

检索一个 **页眉页脚**在给定的索引处。

```csharp
public HeaderFooter this[int index] { get; }
```

| 范围 | 描述 |
| --- | --- |
| index | 集合中的索引。 |

### 评论

该索引从零开始。

允许使用负索引并指示从集合的背面进行访问。 例如 -1 表示最后一项，-2 表示倒数第二个，依此类推。

如果 index 大于或等于列表中的项目数，则返回空引用。

如果 index 为负且其绝对值大于列表中的项目数，则返回空引用。

### 例子

显示如何在部分之间链接页眉和页脚。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

// 移动到第一部分并创建页眉和页脚。默认，
// 页眉和页脚只会出现在包含它们的部分的页面上。
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// 我们可以将一个部分的页眉/页脚链接到前一个部分的页眉/页脚
// 允许链接部分显示链接部分的页眉/页脚。
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// 每个部分仍然有自己的页眉/页脚对象。当我们链接部分时，
// 链接部分将显示链接部分的页眉/页脚，同时保留其自己的。
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// 将第三部分的页眉/页脚链接到第二部分的页眉/页脚。
// 第二部分已经链接到第一部分的页眉/页脚，
// 所以链接到第二部分将创建一个链接链。
// 第一个、第二个和现在的第三个部分都将显示第一部分的标题。
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// 我们可以在调用 LinkToPrevious 方法时通过传递“false”来取消链接上一节的页眉/页脚。
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// 我们也可以使用此方法仅选择特定类型的页眉/页脚进行链接。
// 现在第三部分将具有与第二和第一部分相同的页脚，但不是页眉。
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// 第一部分的页眉/页脚无法链接到任何内容，因为没有前一部分。
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// 所有第二部分的页眉/页脚都链接到第一部分的页眉/页脚。
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// 在第三节中，只有页脚通过第二节链接到第一节的页脚。
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### 也可以看看

* class [HeaderFooter](../../headerfooter/)
* class [HeaderFooterCollection](../)
* 命名空间 [Aspose.Words](../../headerfootercollection/)
* 部件 [Aspose.Words](../../../)

---

## HeaderFooterCollection indexer (2 of 2)

检索一个 **页眉页脚**指定类型的.

```csharp
public HeaderFooter this[HeaderFooterType headerFooterType] { get; }
```

| 范围 | 描述 |
| --- | --- |
| headerFooterType | 一个[`HeaderFooterType`](../../headerfootertype/) value 指定要检索的页眉/页脚的类型。 |

### 评论

如果未找到指定类型的页眉/页脚，则返回 null。

### 例子

显示如何替换文档页脚中的文本。

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

显示如何从文档中删除所有页脚。

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// 遍历每个部分并删除各种页脚。
foreach (Section section in doc.OfType<Section>())
{
    // 共有三种页脚和页眉类型。
    // 1 - “第一个”页眉/页脚，仅出现在部分的第一页上。
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - “主要”页眉/页脚，出现在奇数页上。
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - “偶数”页眉/页脚，出现在偶数页上。
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

### 也可以看看

* class [HeaderFooter](../../headerfooter/)
* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooterCollection](../)
* 命名空间 [Aspose.Words](../../headerfootercollection/)
* 部件 [Aspose.Words](../../../)


