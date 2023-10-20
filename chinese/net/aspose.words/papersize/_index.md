---
title: PaperSize Enum
linktitle: PaperSize
articleTitle: PaperSize
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.PaperSize 枚举. 指定纸张大小 在 C#.
type: docs
weight: 4380
url: /zh/net/aspose.words/papersize/
---
## PaperSize enumeration

指定纸张大小。

```csharp
public enum PaperSize
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| A3 | `0` | 297 x 420 毫米. |
| A4 | `1` | 210 x 297 毫米. |
| A5 | `2` | 148 x 210 毫米. |
| B4 | `3` | 250 x 353 毫米. |
| B5 | `4` | 176 x 250 毫米. |
| Executive | `5` | 7.25 x 10.5 英寸。 |
| Folio | `6` | 8.5 x 13 英寸。 |
| Ledger | `7` | 17 x 11 英寸。 |
| Legal | `8` | 8.5 x 14 英寸。 |
| Letter | `9` | 8.5 x 11 英寸。 |
| EnvelopeDL | `10` | 110 x 220 毫米. |
| Quarto | `11` | 8.47 x 10.83 英寸。 |
| Statement | `12` | 8.5 x 5.5 英寸。 |
| Tabloid | `13` | 11 x 17 英寸。 |
| Paper10x14 | `14` | 10 x 14 英寸。 |
| Paper11x17 | `15` | 11 x 17 英寸。 |
| Number10Envelope | `16` | 4.125 x 9.5 英寸。 |
| Custom | `17` | 自定义纸张尺寸。 |

## 例子

显示如何调整纸张大小、方向、边距以及部分的其他设置。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

显示如何设置页面大小。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 我们可以将当前页面的大小更改为预定义的大小
// 通过使用此部分的 PageSetup 对象的“PaperSize”属性。
builder.PageSetup.PaperSize = PaperSize.Tabloid;

Assert.AreEqual(792.0d, builder.PageSetup.PageWidth);
Assert.AreEqual(1224.0d, builder.PageSetup.PageHeight);

builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

// 每个部分都有自己的 PageSetup 对象。当我们使用文档构建器创建一个新部分时，
// 该部分的 PageSetup 对象继承了上一个部分的所有 PageSetup 对象的值。
builder.InsertBreak(BreakType.SectionBreakEvenPage);

Assert.AreEqual(PaperSize.Tabloid, builder.PageSetup.PaperSize);

builder.PageSetup.PaperSize = PaperSize.A5;
builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

Assert.AreEqual(419.55d, builder.PageSetup.PageWidth);
Assert.AreEqual(595.30d, builder.PageSetup.PageHeight);

builder.InsertBreak(BreakType.SectionBreakEvenPage);

// 设置此部分页面的自定义大小。
builder.PageSetup.PageWidth = 620;
builder.PageSetup.PageHeight = 480;

Assert.AreEqual(PaperSize.Custom, builder.PageSetup.PaperSize);

builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

doc.Save(ArtifactsDir + "PageSetup.PaperSizes.docx");
```

展示如何手动构建 Aspose.Words 文档。

```csharp
Document doc = new Document();

// 一个空白文档包含一个部分、一个正文和一个段落。
// 调用“RemoveAllChildren”方法来移除所有这些节点，
// 最后得到一个没有子节点的文档节点。
doc.RemoveAllChildren();

// 这个文档现在没有我们可以添加内容的复合子节点。
// 如果我们想编辑它，我们需要重新填充它的节点集合。
// 首先，创建一个新部分，然后将其作为子节点附加到根文档节点。
Section section = new Section(doc);
doc.AppendChild(section);

// 为该部分设置一些页面设置属性。
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// 一个section需要一个body，它将包含并显示它的所有内容
// 在节的页眉和页脚之间的页面上。
Body body = new Body(doc);
section.AppendChild(body);

// 创建一个段落，设置一些格式属性，然后将其作为子项附加到正文中。
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// 最后，添加一些内容来做文档。创建运行，
// 设置其外观和内容，然后将其作为子项附加到段落中。
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
