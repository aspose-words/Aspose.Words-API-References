---
title: LinkToPrevious
second_title: Aspose.Words for .NET API 参考
description: 将所有页眉和页脚链接或取消链接到上一节中相应的 页眉和页脚
type: docs
weight: 20
url: /zh/net/aspose.words/headerfootercollection/linktoprevious/
---
## LinkToPrevious(bool) {#linktoprevious_1}

将所有页眉和页脚链接或取消链接到上一节中相应的 页眉和页脚。

```csharp
public void LinkToPrevious(bool isLinkToPrevious)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| isLinkToPrevious | Boolean | True 将页眉和页脚链接到上一节； false 取消链接。 |

### 评论

如果任何页眉或页脚不存在，则自动创建它们。

### 例子

显示如何在节之间链接页眉和页脚。

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

* class [HeaderFooterCollection](../../headerfootercollection)
* 命名空间 [Aspose.Words](../../headerfootercollection)
* 部件 [Aspose.Words](../../../)

---

## LinkToPrevious(HeaderFooterType, bool) {#linktoprevious}

将指定的页眉或页脚链接或取消链接到上一节中相应的 页眉或页脚。

```csharp
public void LinkToPrevious(HeaderFooterType headerFooterType, bool isLinkToPrevious)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| headerFooterType | HeaderFooterType | A[`HeaderFooterType`](../../headerfootertype)值 指定要链接/取消链接的页眉或页脚。 |
| isLinkToPrevious | Boolean | True 将页眉或页脚链接到上一节； false 取消链接。 |

### 评论

如果指定类型的页眉或页脚不存在，则自动创建。

### 例子

显示如何在节之间链接页眉和页脚。

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

* enum [HeaderFooterType](../../headerfootertype)
* class [HeaderFooterCollection](../../headerfootercollection)
* 命名空间 [Aspose.Words](../../headerfootercollection)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
