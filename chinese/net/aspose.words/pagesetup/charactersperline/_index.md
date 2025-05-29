---
title: PageSetup.CharactersPerLine
linktitle: CharactersPerLine
articleTitle: CharactersPerLine
second_title: Aspose.Words for .NET
description: 使用 PageSetup CharactersPerLine 属性控制文档布局。轻松调整每行字符数，以获得最佳的可读性和设计感。
type: docs
weight: 100
url: /zh/net/aspose.words/pagesetup/charactersperline/
---
## PageSetup.CharactersPerLine property

获取或设置文档网格中每行的字符数。

```csharp
public int CharactersPerLine { get; set; }
```

## 评论

该属性的最小值为 1。最大值取决于 Normal 样式的页面宽度和字体大小。最小字符间距为字体大小的 90%。例如，边距为 1 英寸的 Letter 页面每行的最大字符数为 43 个。

默认情况下，该属性有一个值，该值字符间距等于 Normal 样式的字体大小。

## 例子

展示如何指定每行可能包含的字符数。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 启用间距，然后使用它来设置本节每行的字符数。
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// 字符数也取决于字体的大小。
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

### 也可以看看

* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
