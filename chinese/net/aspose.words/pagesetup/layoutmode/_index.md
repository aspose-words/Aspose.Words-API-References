---
title: PageSetup.LayoutMode
linktitle: LayoutMode
articleTitle: LayoutMode
second_title: 用于 .NET 的 Aspose.Words
description: PageSetup LayoutMode 财产. 获取或设置此部分的布局模式 在 C#.
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

演示如何指定每行可以包含的字符数。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 启用间距，然后用它来设置此部分中每行的字符数。
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// 字符数还取决于字体的大小。
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

演示如何指定每页可以拥有的行数限制。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 启用间距，然后用它来设置此部分中每页的行数。
// 足够大的字体大小会将某些行向下推到下一页，以避免字符重叠。
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
