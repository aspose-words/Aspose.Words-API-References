---
title: PageSetup.LayoutMode
linktitle: LayoutMode
articleTitle: LayoutMode
second_title: Aspose.Words for .NET
description: 探索 PageSetup LayoutMode 属性，轻松自定义文档布局。灵活的分区选项助您提升设计体验！
type: docs
weight: 190
url: /zh/net/aspose.words/pagesetup/layoutmode/
---
## PageSetup.LayoutMode property

获取或设置此部分的布局模式。

```csharp
public SectionLayoutMode LayoutMode { get; set; }
```

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

展示如何指定每页行数的限制。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 启用间距，然后使用它来设置本节每页的行数。
// 足够大的字体大小会将一些行推到下一页以避免字符重叠。
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### 也可以看看

* enum [SectionLayoutMode](../../sectionlayoutmode/)
* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
