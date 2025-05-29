---
title: Shading.Texture
linktitle: Texture
articleTitle: Texture
second_title: Aspose.Words for .NET
description: 探索“阴影纹理”属性，提升您的设计。轻松自定义和设置纹理，为您的项目打造惊艳的视觉效果。
type: docs
weight: 70
url: /zh/net/aspose.words/shading/texture/
---
## Shading.Texture property

获取或设置阴影纹理。

```csharp
public TextureIndex Texture { get; set; }
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

* enum [TextureIndex](../../textureindex/)
* class [Shading](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
