---
title: ParagraphFormat.Shading
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words for .NET
description: 探索 ParagraphFormat Shading 属性，增强文本样式。访问 Shading 对象，轻松提升段落的视觉吸引力。
type: docs
weight: 290
url: /zh/net/aspose.words/paragraphformat/shading/
---
## ParagraphFormat.Shading property

返回[`Shading`](../../shading/)引用段落阴影格式的对象。

```csharp
public Shading Shading { get; }
```

## 例子

展示如何使用边框和阴影装饰文本。

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
