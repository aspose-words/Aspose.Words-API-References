---
title: PageSetup.Orientation
second_title: Aspose.Words for .NET API 参考
description: PageSetup 财产. 返回或设置页面的方向
type: docs
weight: 290
url: /zh/net/aspose.words/pagesetup/orientation/
---
## PageSetup.Orientation property

返回或设置页面的方向。

```csharp
public Orientation Orientation { get; set; }
```

### 评论

改变`Orientation`掉期[`PageWidth`](../pagewidth/)和[`PageHeight`](../pageheight/)。

### 例子

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

演示如何将页面设置设置应用和恢复到文档中的各个部分。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 修改构建器当前部分的页面设置属性并添加文本。
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// 如果我们使用文档生成器开始一个新部分，
// 它将继承构建器的当前页面设置属性。
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// 我们可以使用“ClearFormatting”方法将其页面设置属性恢复为其默认值。
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### 也可以看看

* enum [Orientation](../../orientation/)
* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../pagesetup/)
* 部件 [Aspose.Words](../../../)


