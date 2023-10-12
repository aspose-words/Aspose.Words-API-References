---
title: PageSetup.BottomMargin
second_title: Aspose.Words for .NET API 参考
description: PageSetup 财产. 返回或设置页面底部边缘与正文底部边界之间的距离以磅为单位
type: docs
weight: 80
url: /zh/net/aspose.words/pagesetup/bottommargin/
---
## PageSetup.BottomMargin property

返回或设置页面底部边缘与正文底部边界之间的距离（以磅为单位）。

```csharp
public double BottomMargin { get; set; }
```

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

### 也可以看看

* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../pagesetup/)
* 部件 [Aspose.Words](../../../)


