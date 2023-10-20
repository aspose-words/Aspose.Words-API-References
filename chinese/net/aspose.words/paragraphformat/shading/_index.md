---
title: ParagraphFormat.Shading
linktitle: Shading
articleTitle: Shading
second_title: 用于 .NET 的 Aspose.Words
description: ParagraphFormat Shading 财产. 返回一个 Shading 对象该对象引用段落的阴影格式 在 C#.
type: docs
weight: 280
url: /zh/net/aspose.words/paragraphformat/shading/
---
## ParagraphFormat.Shading property

返回一个 Shading 对象，该对象引用段落的阴影格式。

```csharp
public Shading Shading { get; }
```

## 例子

展示如何用边框和底纹装饰文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

BorderCollection borders = builder.ParagraphFormat.Borders;
borders.DistanceFromText = 20;
borders[BorderType.Left].LineStyle = LineStyle.Double;
borders[BorderType.Right].LineStyle = LineStyle.Double;
borders[BorderType.Top].LineStyle = LineStyle.Double;
borders[BorderType.Bottom].LineStyle = LineStyle.Double;

Shading shading = builder.ParagraphFormat.Shading;
shading.Texture = TextureIndex.TextureDiagonalCross;
shading.BackgroundPatternColor = Color.LightCoral;
shading.ForegroundPatternColor = Color.LightSalmon;

builder.Write("This paragraph is formatted with a double border and shading.");
doc.Save(ArtifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
```

### 也可以看看

* class [Shading](../../shading/)
* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
