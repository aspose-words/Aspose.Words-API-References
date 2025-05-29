---
title: PageSetup.PaperSize
linktitle: PaperSize
articleTitle: PaperSize
second_title: Aspose.Words for .NET
description: 发现 PageSetup PaperSize 属性，轻松自定义和管理文档的纸张尺寸，以获得最佳打印效果。
type: docs
weight: 350
url: /zh/net/aspose.words/pagesetup/papersize/
---
## PageSetup.PaperSize property

返回或设置纸张尺寸。

```csharp
public PaperSize PaperSize { get; set; }
```

## 评论

设置此属性更新[`PageWidth`](../pagewidth/)和[`PageHeight`](../pageheight/)values. 将此值设置为Custom不会改变现有值。

## 例子

演示如何设置 JisB4 或 JisB5 的纸张尺寸。

```csharp
Document doc = new Document(MyDir + "Big document.docx");

PageSetup pageSetup = doc.FirstSection.PageSetup;
// 将纸张尺寸设置为 JisB4 (257x364mm)。
pageSetup.PaperSize = PaperSize.JisB4;
// 或者，将纸张尺寸设置为 JisB5。(182x257mm)。
pageSetup.PaperSize = PaperSize.JisB5;
```

展示如何调整纸张尺寸、方向、边距以及某个部分的其他设置。

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
//通过使用本节的 PageSetup 对象的“PaperSize”属性。
builder.PageSetup.PaperSize = PaperSize.Tabloid;

Assert.AreEqual(792.0d, builder.PageSetup.PageWidth);
Assert.AreEqual(1224.0d, builder.PageSetup.PageHeight);

builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

// 每个部分都有自己的 PageSetup 对象。当我们使用文档构建器创建新部分时，
// 该部分的 PageSetup 对象继承了所有前一部分的 PageSetup 对象的值。
builder.InsertBreak(BreakType.SectionBreakEvenPage);

Assert.AreEqual(PaperSize.Tabloid, builder.PageSetup.PaperSize);

builder.PageSetup.PaperSize = PaperSize.A5;
builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

Assert.AreEqual(419.55d, builder.PageSetup.PageWidth);
Assert.AreEqual(595.30d, builder.PageSetup.PageHeight);

builder.InsertBreak(BreakType.SectionBreakEvenPage);

// 为本节的页面设置自定义大小。
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
// 调用“RemoveAllChildren”方法删除所有节点，
// 并最终得到一个没有子节点的文档节点。
doc.RemoveAllChildren();

// 此文档现在没有可以添加内容的复合子节点。
// 如果我们想要编辑它，我们将需要重新填充它的节点集合。
// 首先，创建一个新的部分，然后将其作为子节点附加到根文档节点。
Section section = new Section(doc);
doc.AppendChild(section);

// 为该部分设置一些页面设置属性。
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// 一个部分需要一个主体，它将包含并显示其所有内容
// 位于页面部分页眉和页脚之间。
Body body = new Body(doc);
section.AppendChild(body);

// 创建一个段落，设置一些格式属性，然后将其作为子部分附加到正文中。
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// 最后，添加一些内容来执行文档。创建一个运行，
// 设置其外观和内容，然后将其作为子项附加到段落。
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### 也可以看看

* enum [PaperSize](../../papersize/)
* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
