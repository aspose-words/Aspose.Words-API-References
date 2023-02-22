---
title: Shading.Texture
second_title: Aspose.Words for .NET API 参考
description: Shading 财产. 获取或设置着色纹理
type: docs
weight: 30
url: /zh/net/aspose.words/shading/texture/
---
## Shading.Texture property

获取或设置着色纹理。

```csharp
public TextureIndex Texture { get; set; }
```

### 例子

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

* enum [TextureIndex](../../textureindex/)
* class [Shading](../)
* 命名空间 [Aspose.Words](../../shading/)
* 部件 [Aspose.Words](../../../)


