---
title: Border.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: 用于 .NET 的 Aspose.Words
description: Border LineWidth 财产. 获取或设置边框宽度以磅为单位 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words/border/linewidth/
---
## Border.LineWidth property

获取或设置边框宽度（以磅为单位）。

```csharp
public double LineWidth { get; set; }
```

## 评论

当线型为无时，如果设置线宽大于零，则线型 is 自动更改为单线。

## 例子

演示如何将边框包围的字符串插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

### 也可以看看

* class [Border](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
